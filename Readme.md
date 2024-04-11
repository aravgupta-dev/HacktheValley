
# Streamlit Application Setup Guide for `farm-ng`

## Objective
Prepare your system and run a Streamlit application related to the `farm-ng` project, utilizing best practices in Python environment management.

## Prerequisites
- Basic knowledge of terminal/command line usage.
- Git and Python installed on your system.

## Setup Environment

### Install pip3 & Virtualenv

**For Linux:**
```bash
sudo apt-get install python3-pip
sudo pip3 install virtualenv
```

**For MacOS:**
- Ensure Python 3 and pip are installed. MacOS comes with Python 2.7 installed by default, you may need to install Python 3.x from the Python website or via Homebrew.
- Install virtualenv using pip3:
  ```bash
  sudo pip3 install virtualenv
  ```

### Start a Virtual Environment
1. Navigate to the directory where you want your virtual environment to reside.
2. Create the virtual environment:
   ```bash
   python3 -m venv venv
   ```
3. Activate the virtual environment:
   ```bash
   source venv/bin/activate
   ```
   
**[Optional]** To exit or re-enter your virtual environment:
- Exit: `deactivate`
- Re-enter (ensure you're in the directory containing `venv/`): `source venv/bin/activate`

## Package Installation

### Install Required Packages
Ensure your pip and setuptools are up-to-date:
```bash
pip install --upgrade pip
pip install --upgrade setuptools
```

**For Linux & MacOS:**
Install `farm-ng-amiga`:
```bash
pip3 install farm-ng-amiga
```

## Check Installed Version
Verify the installed versions of `farm-ng` packages:
```bash
pip list | grep -E 'farm-ng|farm_ng'
```

## Package Updates
Keep your `farm-ng` packages up to date:
```bash
pip3 install farm-ng-package --upgrade
pip3 install farm-ng-core --upgrade
pip3 install farm-ng-amiga --upgrade
```

## Install from Source [Advanced]
1. Clone the `farm-ng-amiga` repository:
   ```bash
   git clone https://github.com/farm-ng/farm-ng-amiga.git
   # Or use SSH if you prefer:
   git clone git@github.com:farm-ng/farm-ng-amiga.git
   ```
2. Navigate into the cloned directory:
   ```bash
   cd farm-ng-amiga/
   ```
3. Build and install the package:
   - For a standard installation:
     ```bash
     pip install .
     ```
   - For development mode:
     ```bash
     pip install -e .[dev]
     ```

## Returning to the Streamlit Application Setup
After preparing your environment and managing the `farm-ng` package installations, follow the initial guide for navigating to the Streamlit application directory and running the application.

## Final Steps
- Navigate to the Streamlit application directory and run the application as previously outlined.
- Ensure all dependencies mentioned earlier are installed in your activated virtual environment.
