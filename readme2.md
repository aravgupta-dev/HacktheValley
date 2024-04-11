# Python Setup Guide

## Ensure Python 3 and pip are installed
MacOS comes with Python 2.7 installed by default, so you may need to install Python 3.x from the Python website or via Homebrew.
```bash
sudo pip3 install virtualenv
```

## Start a Virtual Environment

Navigate to the directory where you want your virtual environment to reside.

Create the virtual environment:
```bash
python3 -m venv venv
```

Activate the virtual environment:
```bash
source venv/bin/activate
```

[Optional] To exit or re-enter your virtual environment:
Exit:
```bash
deactivate
```

Re-enter (ensure you’re in the directory containing `venv/`):
```bash
source venv/bin/activate
```

## Clone and Setup Project

Clone the farm-ng repository:
```bash
git clone https://github.com/farm-ng/farm-ng-core.git
cd farm-ng-core/
```

Check out the branch containing the Streamlit application:
```bash
git checkout track-planner-app
```

## Package Installation and Management

Upgrade pip and setuptools:
```bash
pip install --upgrade pip setuptools
```

Install Required Packages:
Ensure your pip and setuptools are up-to-date:
```bash
pip install --upgrade pip
pip install --upgrade setuptools
```

For Linux & MacOS:
Install farm-ng-amiga:
```bash
pip3 install farm-ng-amiga
```

## Check Installed Version

Verify the installed versions of farm-ng packages:
```bash
pip list | grep -E 'farm-ng|farm_ng'
```

## Keep Packages Updated:
```bash
pip3 install farm-ng-package --upgrade
pip3 install farm-ng-core --upgrade
pip3 install farm-ng-amiga --upgrade
```
