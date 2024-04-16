
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
