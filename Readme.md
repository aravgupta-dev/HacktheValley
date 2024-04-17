
# Streamlit Application Setup Guide for `farm-ng`

## Objective
Prepare your system and run a Streamlit application related to the `farm-ng` project, utilizing best practices in Python environment management.

## Prerequisites
- Basic knowledge of terminal/command line usage.
- Git and Python installed on your system.

## Setup Environment

# Installation Guide for Python and virtualenv

  ## For MacOS:

### Prerequisites
If Python 3 and pip are not installed:

### 1. Install Python 3
- Visit the official Python website (https://www.python.org/downloads/) to download and install Python 3 for MacOS. This installation will also include `pip`.
- Alternatively, you can install Python using Homebrew by running:
  ```bash
  brew install python
  ```

### 2. Install virtualenv
- Once Python 3 and pip are installed, you can install `virtualenv` using pip3:
  ```bash
  sudo pip3 install virtualenv
  ```

## For Windows:

### Prerequisites
If Python and pip are not installed:

### 1. Install Python 3
- Download Python 3 from the official Python website (https://www.python.org/downloads/). During installation, ensure that you check the box that says "Add Python 3.x to PATH" to ensure that the interpreter is placed in your execution path.

### 2. Install virtualenv
- Open a command prompt (CMD) as an administrator and run:
  ```cmd
  pip install virtualenv
  ```

## Creating and Activating a Virtual Environment on Windows:

### 1. Navigate to the directory where you want your virtual environment
- Open Command Prompt and change directory to where you want the virtual environment to be set up.

### 2. Create the virtual environment
- Run:
  ```cmd
  python -m venv venv
  ```

### 3. Activate the virtual environment
- To activate the virtual environment, execute:
  ```cmd
  .\venv\Scripts\activate
  ```

## [Optional] Exiting or Re-entering Your Virtual Environment on Windows:
- **Exit**: Run `deactivate` in your Command Prompt.
- **Re-enter**: Make sure you're in the directory containing `venv/` and run:
  ```cmd
  .\venv\Scripts\activate
  ```

These instructions ensure that users with no prior Python installation can set up their environment correctly on both MacOS and Windows.

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

## Navigate and Run Streamlit App
1. Navigate to the Streamlit application directory:`farm-ng-amiga`
   ```bash
   cd py/examples/track_planner/
   ```
2. Run the StreamLit Application:
   ```bash
   streamlit run streamlit.py
   ```
3. HAVE FUN! 
   

## Final Steps
- Ensure all dependencies mentioned earlier are installed in your activated virtual environment.
