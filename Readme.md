
# Streamlit Application Setup Guide for `farm-ng`

## Objective
Prepare your system and run a Streamlit application related to the `AMIGA`, utilizing best practices in Python environment management.

# Setup Environment

## Installation Guide for Python and virtualenv

  ### For MacOS:


### 1. Install Homebrew
- Install homebrew using:
  ```bash
  /bin/bash -c $(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)
  ```
  - If homebrew is not working use these two commands:
  ```bash
  (echo; echo 'eval "$(/opt/homebrew/bin/brew shellenv)"') >> /Users/aravgupta/.zprofile
  eval "$(/opt/homebrew/bin/brew shellenv)"
  ```
 - Verify Homebrew Installation:
  ```bash
  brew doctor
  ```
   - Or Verify Homebrew Installation:
     Open your Terminal and enter the following command to see if Homebrew is installed in the expected location:
  ```bash
  /opt/homebrew/bin/brew --version
  ```

### 3. Install Python 3
- Visit the official Python website (https://www.python.org/downloads/) to download and install Python 3 for MacOS. This installation will also include `pip`.
- Alternatively, you can install Python using Homebrew by running:
  ```bash
  brew install python
  ```

### 2. Install virtualenv
- After installing Python, you can create a virtual environment to manage your project's dependencies separately from the system's Python. You can do this with:
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


## Creating and Activating a Virtual Environment on Mac:

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
  source venv/bin/activate
  ```

**[Optional]** To exit or re-enter your virtual environment:
- Exit: `deactivate`
- Re-enter (ensure you're in the directory containing `venv/`): `source venv/bin/activate`



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

## Package Installation for Mac
  -please make sure to deactivate or kill your virtual envrionment before starting this step. 
  
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
3. Checkout the correct release and update submodulesBuild and install the package:
     ```bash
      git checkout v2.2.0
     ```
4. Checkout the correct release and update submodules
     ```bash
      git submodule update --init --recursive
     ```

4. Activate your virtual enviornment
     ```bash
      source venv/bin/activate
     ``` 
    
     
4. Navigate to the farm-ng directory within your virtual enviornment
     ```bash
      cd farm-ng-core/

     ``` 
    
5. Build and install these packages:
     ```bash
     pip install .
     pip install --upgrade pip
     pip install --upgrade setuptools wheel
     pip install --no-build-isolation farm-ng-amiga
     ```
 6. Check if you have installed the packages correctly
    -run this command:
      ```bash
      pip list | grep -E 'farm-ng|farm_ng'
       ``` 
      You should see something like:
      ```bash
         farm-ng-amiga      2.0.0
         farm-ng-core       2.0.0
         farm-ng-package    0.1.3
       ``` 
         


## Package Installation for Windows  
  -please make sure to deactivate or kill your virtual envrionment before starting this step. 
### Install Required Packages
Ensure your pip and setuptools are up-to-date:
```bash
pip install --upgrade pip
pip install --upgrade setuptools
```



## Check Installed Version
You should see this as a result :
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
