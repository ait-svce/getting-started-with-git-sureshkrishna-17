# Git Installation Assignment

Welcome to your first assignment! This assignment will guide you through installing Git on your local machine and verifying the installation.

## Assignment Objectives

By the end of this assignment, you will:
- Install Git on your local machine
- Verify the installation by running Git commands
- Learn to use Git Bash (Windows) or Terminal (macOS/Linux)
- Submit a screenshot as proof of successful installation

---

## Part 1: Installing Git

Follow the instructions for your operating system:

### Windows Installation

**Note :** Since windows is the Commonly used one here is the Link for How to do it!
🔗 https://youtu.be/TT8ktVp5j-k

> For other OS you can find the Guide Below !


1. **Download Git for Windows**
   - Visit the official Git website: [https://git-scm.com/download/win](https://git-scm.com/download/win)
   - The download should start automatically. If not, click on the appropriate version (64-bit or 32-bit)

2. **Run the Installer**
   - Locate the downloaded file (usually in your Downloads folder)
   - Double-click the `.exe` file to start the installation
   - Click "Yes" if prompted by User Account Control

3. **Installation Settings** (Recommended options)
   - **Select Components**: Keep the default selections
   - **Default Editor**: Choose your preferred text editor (Vim, Nano, Notepad++, VS Code, etc.)
   - **PATH Environment**: Select "Git from the command line and also from 3rd-party software"
   - **HTTPS Transport**: Use the OpenSSL library
   - **Line Ending Conversions**: "Checkout Windows-style, commit Unix-style line endings"
   - **Terminal Emulator**: Use MinTTY (the default terminal of MSYS2)
   - **Git Pull Behavior**: Default (fast-forward or merge)
   - Continue clicking "Next" and accept the remaining defaults
   - Click "Install"

4. **Complete Installation**
   - Once installation is complete, click "Finish"
   - You can choose to launch Git Bash immediately

### macOS Installation

**Method 1: Using Homebrew (Recommended)**

1. **Install Homebrew** (if not already installed)
   - Open Terminal (Applications → Utilities → Terminal)
   - Run the following command:
     ```bash
     /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
     ```
   - Follow the on-screen instructions

2. **Install Git**
   - In Terminal, run:
     ```bash
     brew install git
     ```

**Method 2: Using the Installer**

1. **Download Git for macOS**
   - Visit: [https://git-scm.com/download/mac](https://git-scm.com/download/mac)
   - Download the installer package

2. **Run the Installer**
   - Open the downloaded `.dmg` file
   - Double-click the `.pkg` file
   - Follow the installation wizard

**Method 3: Using Xcode Command Line Tools**

1. Open Terminal and run:
   ```bash
   xcode-select --install
   ```
2. Click "Install" in the dialog box that appears

### Linux Installation

**Ubuntu/Debian:**
```bash
sudo apt-get update
sudo apt-get install git
```

**Fedora:**
```bash
sudo dnf install git
```

**CentOS/RHEL:**
```bash
sudo yum install git
```

**Arch Linux:**
```bash
sudo pacman -S git
```

---

## Part 2: Verify Git Installation

After installing Git, you need to verify that it was installed correctly.

### Step 1: Open Git Bash or Terminal

- **Windows**: 
  - Search for "Git Bash" in the Start Menu
  - Right-click and select "Run as administrator" (optional but recommended)
  - A command-line window with a black background should open

- **macOS**: 
  - Open Terminal (Applications → Utilities → Terminal)
  - Or use Spotlight Search (Cmd + Space) and type "Terminal"

- **Linux**: 
  - Open your Terminal application
  - Or use the keyboard shortcut (usually Ctrl + Alt + T)

### Step 2: Check Git Version

In Git Bash or Terminal, type the following command and press Enter:

```bash
git --version
```

You should see output similar to:
```
git version 2.40.0
```

The version number may be different, but as long as you see "git version" followed by a number, Git is installed correctly.

### Step 3: Run the `whoami` Command

This is the **required command for your submission**. In the same Git Bash or Terminal window, type:

```bash
whoami
```

Press Enter. This command will display your current username. For example:
```
john_doe
```

---

## Part 3: Take a Screenshot

Now you need to capture a screenshot of your Git Bash or Terminal window showing the `whoami` command execution.

### Screenshot Requirements

Your screenshot MUST show:
1. The Git Bash or Terminal window
2. The command you typed: `whoami`
3. The output (your username)
4. The command prompt showing you're ready for the next command

### How to Take a Screenshot

**Windows:**
- **Method 1**: Press `Windows Key + Shift + S` to use Snipping Tool
- **Method 2**: Press `PrtScn` (Print Screen) to capture the full screen
- **Method 3**: Press `Alt + PrtScn` to capture only the active window
- Save the screenshot with a clear filename like `git_installation_yourname.png`

**macOS:**
- **Method 1**: Press `Cmd + Shift + 4` then drag to select the window
- **Method 2**: Press `Cmd + Shift + 3` to capture the full screen
- **Method 3**: Press `Cmd + Shift + 4`, then press `Space`, then click the window
- Screenshot will be saved to your Desktop

**Linux:**
- **Method 1**: Press `PrtScn` or use the Screenshot application
- **Method 2**: Press `Shift + PrtScn` to select a specific area
- **Method 3**: Use GNOME Screenshot or similar tool for your distribution

---

## Part 4: Submit Your Screenshot

1. **Add your screenshot to this repository**
   - Place your screenshot file in the `screenshots/` folder
   - Name your file: `git_installation_<your_name>.png` (or `.jpg`)
   - Example: `git_installation_john_doe.png`

2. **Fill out the SUBMISSION.md file**
   - Open the `SUBMISSION.md` file
   - Fill in your information
   - Add the relative path to your screenshot

3. **Commit and push your changes**
   ```bash
   git add screenshots/git_installation_<your_name>.png
   git add SUBMISSION.md
   git commit -m "Add Git installation verification screenshot"
   git push
   ```

---

## Troubleshooting

### Git command not found

If you get an error like `git: command not found` or `'git' is not recognized`:

**Windows:**
- Restart your computer after installation
- Make sure you're using Git Bash, not Command Prompt or PowerShell
- Reinstall Git and ensure "Git from the command line and also from 3rd-party software" is selected

**macOS/Linux:**
- Verify installation completed without errors
- Try opening a new Terminal window
- Check if Git is in your PATH by running: `which git`

### whoami command not working

- On Windows, make sure you're using Git Bash (not Command Prompt)
- The command should work in all Unix-like terminals and Git Bash
- If you still have issues, try: `echo $USER` (Linux/macOS) or `echo %USERNAME%` (Windows Command Prompt)

### Need Help?

If you encounter any issues:
1. Check the troubleshooting section above
2. Search for your error message online
3. Ask your instructor or teaching assistant
4. Post in the course discussion forum

---

## Additional Resources

- [Official Git Documentation](https://git-scm.com/doc)
- [Git Tutorial for Beginners](https://www.youtube.com/results?search_query=git+tutorial+for+beginners)
- [Pro Git Book (Free)](https://git-scm.com/book/en/v2)

---

## Grading Criteria

- ✅ Git successfully installed on your machine
- ✅ Screenshot clearly shows Git Bash/Terminal window
- ✅ Screenshot shows the `whoami` command and its output
- ✅ Screenshot is properly named and placed in the `screenshots/` folder
- ✅ SUBMISSION.md file is filled out correctly
- ✅ Changes are committed and pushed to the repository

---

**Good luck with your first assignment! 🚀**
