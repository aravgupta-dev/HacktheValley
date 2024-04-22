
# Brain ADK Installation

## PyPI version

### Install from pip [recommended]

**TIP**  
We strongly recommend running the brain SDK applications in a virtual environment to avoid conflicts with other packages / versions installed on your system. Though this is not a requirement and you are welcome to decide how/where to install.

## Setup environment

If you want to install farm-ng-amiga in a virtual environment:

### Install pip3 & virtualenv

#### Linux
#### MacOs
```
brew install python3
# to check if the installation was successful input command
pip --version
sudo pip3 install virtualenv
```

### Start a virtual environment

```
# assuming you're in the directory where you want to create your
# `venv`
python3 -m venv venv
source venv/bin/activate
```

**[optional]** when you want to exit / re-enter your venv

```
deactivate # exit
source venv/bin/activate # re-enter, assuming you're in the root
# containing `venv/`
```

## Package install

Now install the package with pip

**NOTICE**  
Currently the farm-ng-core wheel must be built from source on MacOS. Please use the correct tab for your OS. For Amiga Brains, please follow the Linux instructions.

#### Linux
#### MacOs
```
# Clone the farm-ng-core repo
git clone https://github.com/farm-ng/farm-ng-core.git

# Checkout the correct release and update submodules
cd farm-ng-core/
git checkout v2.0.0
git submodule update --init --recursive
cd ../

# [Optional] Upgrade some deps
pip install --upgrade pip
pip install --upgrade setuptools wheel

# Build farm-ng-core from source
cd farm-ng-core/
pip install .
cd ../

# Install farm-ng-amiga wheel, using farm-ng-core built from source
pip install --no-build-isolation farm-ng-amiga
```

## Check installed version

You can check the installed version

```
pip list | grep -E 'farm-ng|farm_ng'

# You should see something like:
# farm-ng-amiga      2.0.0
# farm-ng-core       2.0.0
# farm-ng-package    0.1.3
```

## Package updates

As new releases come out, you can keep your farm-ng packages up to date

```
pip3 install farm-ng-package --upgrade
pip3 install farm-ng-core --upgrade
pip3 install farm-ng-amiga --upgrade
```

### Install from source [advanced]

Clone the repository

To install the farm-ng-amiga package and test the available examples, start by cloning the repo

```
git clone https://github.com/farm-ng/farm-ng-amiga.git
cd farm-ng-amiga/
```

**TIP**  
If you want to clone with git instead of https:

```
git clone git@github.com:farm-ng/farm-ng-amiga.git
```

**NOTE:** This requires that you have an ssh key set up.
See farm-ng Github 101 - Set up an SSH key for more information and instructions.
Keep the repo up-to-date with:

```
# from farm-ng-amiga/ dir
git checkout main
git pull
```

### Build the package

Install pip3 & setup a virtualenv (shown above)  
Create and install the farm-ng-amiga Python package
```
# install to system
pip install --upgrade pip
pip install --upgrade setuptools
pip3 install .

# or for development mode
pip3 install -e .[dev]
```
