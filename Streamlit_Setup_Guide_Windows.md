
# Streamlit Application Setup Guide for Windows - `farm-ng`

## Objective
Prepare your Windows system to run a Streamlit application related to `AMIGA`, utilizing best practices in Python environment management.

## Prerequisites
- Administrator access on your Windows system.
- Stable internet connection for downloading software.

## Step 1: Install Python 3
Python is essential for running Python-based applications like Streamlit.

1. Visit the official Python website: https://www.python.org/downloads/
2. Download the latest version of Python 3 for Windows.
3. Run the installer. Ensure to check 'Add Python 3.x to PATH' at the beginning of the installation process.
4. Verify the installation by opening Command Prompt and running:
   ```cmd
   python --version
   ```

## Step 2: Install virtualenv
`virtualenv` is a tool to create isolated Python environments.

1. Open Command Prompt as Administrator.
2. Install `virtualenv` using pip:
   ```cmd
   pip install virtualenv
   ```
3. Verify the installation:
   ```cmd
   virtualenv --version
   ```

## Step 3: Create and Activate a Virtual Environment
1. Navigate to the directory where you want to set up your project.
   ```cmd
   cd path\to\your\project
   ```
2. Create a virtual environment named `venv`:
   ```cmd
   python -m venv venv
   ```
3. Activate the virtual environment:
   ```cmd
   source venv/bin/activate
   ```
   Your command prompt should now show the virtual environment name.
4. To deactivate the virtual environment, use:
   ```cmd
   deactivate
   ```

## Step 4: Package Installation
1. Ensure your `pip`, `setuptools`, and `wheel` are up to date in your virtual environment:
   ```cmd
   pip install --upgrade pip setuptools wheel
   ```
2. Clone the `farm-ng-amiga` repository:
   ```cmd
   git clone https://github.com/farm-ng/farm-ng-amiga.git
   ```
3. Navigate to the repository directory and install the packages:
   ```cmd
   cd farm-ng-amiga
   pip install .
   ```

## Step 5: Run Streamlit Application
1. Install Streamlit
   ```cmd
   pip install streamlit
   ```
2. Navigate to the Streamlit application directory within the repository:
   ```cmd
   cd py\examples\track_planner\
   ```
3. Run the Streamlit application:
   ```cmd
   streamlit run track_planner.py
   ```
4. Access the Streamlit application in your web browser at `http://localhost:8501`.
   
5. To stop the app use:
   ```cmd
   control+d
   ```
   in the terminal

## Troubleshooting
- Ensure all commands are run within the virtual environment.
- If you encounter errors during installation, ensure your internet connection is stable, and retry the commands.
- For specific error messages, consult the documentation or seek help from Stack Overflow or similar forums.
  
## Tips and Guides
For more information on how to build your own track head over to these links:
   - [https://amiga.farm-ng.com/docs/brain/brain-install/](https://amiga.farm-ng.com/docs/examples/track_planner/) 
   - [https://amiga.farm-ng.com/docs/concepts/tracks_and_waypoints/](https://amiga.farm-ng.com/docs/concepts/tracks_and_waypoints/)


