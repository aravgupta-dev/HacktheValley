
# Streamlit Application Setup Guide for MacOS - `farm-ng`

## Objective
Prepare your MacOS system to run a Streamlit application related to `AMIGA`, utilizing best practices in Python environment management.

## Prerequisites
- Administrator access on your MacOS.
- Stable internet connection for downloading software.

## Step 1: Install Homebrew
Homebrew is a package manager for MacOS which simplifies the installation of software.

1. Open the Terminal.
2. Install Homebrew by running the following command:
   ```bash
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   ```
3. After installation, add Homebrew to your system's shell environment by running:
   ```bash
   echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.zprofile
   eval "$(/opt/homebrew/bin/brew shellenv)"
   ```
4. Verify the installation with:
   ```bash
   brew doctor
   ```
   You should see a message saying 'Your system is ready to brew.'

## Step 2: Install Python 3
Python is essential for running Python-based applications like Streamlit.

1. You can install Python via Homebrew with the following command:
   ```bash
   brew install python
   ```
2. Verify the installation by checking the version of Python:
   ```bash
   python3 --version
   ```

## Step 3: Install virtualenv
`virtualenv` is a tool to create isolated Python environments.

1. Install `virtualenv` using pip:
   ```bash
   pip3 install virtualenv
   ```
2. Verify the installation:
   ```bash
   virtualenv --version
   ```

## Step 4: Create and Activate a Virtual Environment
1. Navigate to the directory where you want to set up your project.
   ```bash
   cd path/to/your/project
   ```
2. Create a virtual environment named `venv`:
   ```bash
   python3 -m venv venv
   ```
3. Activate the virtual environment:
   ```bash
   source venv/bin/activate
   ```
   Your prompt will change to indicate that you are now working inside the virtual environment.
4. To deactivate the virtual environment, use:
   ```bash
   deactivate
   ```

## Step 5: Package Installation
1. Ensure your `pip`, `setuptools`, and `wheel` are up to date in your virtual environment:
   ```bash
   pip install --upgrade pip setuptools wheel
   ```
2. Clone the `farm-ng-amiga` repository:
   ```bash
   git clone https://github.com/farm-ng/farm-ng-amiga.git
   ```
3. Navigate to the repository directory and install the packages:
   ```bash
   cd farm-ng-amiga
   pip install .
   ```

## Step 6: Run Streamlit Application
1. Navigate to the Streamlit application directory within the repository:
   ```bash
   cd py/examples/track_planner/
   ```
2. Run the Streamlit application:
   ```bash
   streamlit run streamlit.py
   ```
3. Access the Streamlit application in your web browser at `http://localhost:8501`.

## Troubleshooting
- Ensure all commands are run within the virtual environment.
- If you encounter errors during installation, ensure your internet connection is stable, and retry the commands.
- For specific error messages, consult the documentation or seek help from Stack Overflow or similar forums.

