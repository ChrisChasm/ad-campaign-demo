# Installing Git and Homebrew: Complete Guide

This comprehensive guide provides step-by-step instructions for installing Git (and Homebrew on macOS) using two methods: **Cursor Agent** (automated) and **Terminal/Command Line** (manual). Git is required for version control and managing your repository for this ad campaign demo project.

## What is Git?

Git is a version control system that allows you to track changes to your files, collaborate with others, and manage your codebase. For this project, Git is essential for:
- Cloning the repository from GitHub
- Committing changes to your campaign files
- Pushing updates to GitHub (which triggers Netlify deployments)

## What is Homebrew? (macOS only)

Homebrew is a package manager for macOS that makes it easy to install software and tools from the command line. It's the recommended way to install Git on Mac because:
- It keeps Git updated easily
- It manages dependencies automatically
- It's widely used and well-maintained
- It makes installing other development tools simple

## Prerequisites

Before starting, ensure you have:
- **Cursor IDE** installed and running (for Cursor Agent method)
- **Terminal/Command Prompt** access
- **Administrator/Admin privileges** (may be required for installation)
- **Internet connection** for downloading Git and Homebrew
- **macOS** (for Homebrew) or **Windows** (for Git installation)

## Quick Start: Choose Your Method

You have two options for installation:

1. **Cursor Agent Method** (Recommended for beginners)
   - Let Cursor Agent handle the installation automatically
   - Less typing, more guidance
   - Best if you're new to command line tools

2. **Terminal/Command Line Method** (For experienced users)
   - Full control over the installation process
   - See exactly what's happening
   - Faster if you're comfortable with terminal commands

---

## Part 1: macOS Installation

### Step 1: Check if Git is Already Installed

Before installing anything, check if Git is already on your system:

#### Using Cursor Agent:
1. **Open Cursor IDE**
2. **Open the chat interface** (usually `Cmd+L` on Mac)
3. **Ask Cursor Agent**:
   ```
   Check if Git is installed on my Mac by running 'git --version'
   ```
4. **Review the output**:
   - If you see `git version 2.x.x` or similar → ✅ **Git is installed!** Skip to [Verification](#verification)
   - If you see "command not found" → Continue to Step 2

#### Using Terminal (Manual):
1. **Open Terminal** in Cursor (Terminal → New Terminal) or use macOS Terminal app
2. **Run this command**:
   ```bash
   git --version
   ```
3. **Check the output**:
   - If you see `git version 2.x.x` or similar → ✅ **Git is installed!** Skip to [Verification](#verification)
   - If you see "command not found" → Continue to Step 2

---

### Step 2: Install Homebrew (macOS - Recommended First Step)

Homebrew is the best way to install Git on macOS. Let's install it first.

#### Method A: Using Cursor Agent (Easiest)

1. **Open Cursor IDE** and the chat interface (`Cmd+L`)
2. **Ask Cursor Agent**:
   ```
   Install Homebrew on my Mac. Follow the installation prompts and help me complete the setup.
   ```
3. **Follow the prompts**:
   - Cursor Agent will run the installation command
   - You may be asked to enter your Mac password (for sudo access)
   - The installation will download and set up Homebrew
   - This typically takes 5-10 minutes

4. **After installation**, Cursor Agent will help verify Homebrew is working

#### Method B: Using Terminal (Manual)

1. **Open Terminal** in Cursor or macOS Terminal app

2. **Run the Homebrew installation command**:
   ```bash
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   ```
   - This downloads and runs the Homebrew installation script
   - You'll be prompted to enter your Mac password (for administrator access)
   - Type your password and press Enter (you won't see characters as you type - this is normal)

3. **Follow the on-screen prompts**:
   - The installer will explain what it's doing
   - You may see messages about installing Xcode Command Line Tools (this is normal)
   - Press `Enter` when prompted to continue
   - Wait for installation to complete (5-10 minutes)

4. **Complete post-installation setup** (if needed):
   
   After installation, you may see instructions to add Homebrew to your PATH. If you see a message like:
   ```
   Next steps:
   - Run these commands in your terminal to add Homebrew to your PATH:
   ```
   
   **For Apple Silicon Macs (M1/M2/M3):**
   ```bash
   echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.zprofile
   eval "$(/opt/homebrew/bin/brew shellenv)"
   ```
   
   **For Intel Macs:**
   ```bash
   echo 'eval "$(/usr/local/bin/brew shellenv)"' >> ~/.zprofile
   eval "$(/usr/local/bin/brew shellenv)"
   ```

5. **Verify Homebrew installation**:
   ```bash
   brew --version
   ```
   - You should see output like `Homebrew 4.x.x` or similar
   - If you see "command not found", you may need to restart your terminal or add Homebrew to PATH (see step 4)

---

### Step 3: Install Git Using Homebrew (macOS)

Now that Homebrew is installed, installing Git is simple.

#### Method A: Using Cursor Agent

1. **Open Cursor IDE** and the chat interface (`Cmd+L`)
2. **Ask Cursor Agent**:
   ```
   Install Git on my Mac using Homebrew
   ```
3. **Wait for installation**:
   - Cursor Agent will run `brew install git`
   - This typically takes 2-5 minutes
   - You'll see progress in the terminal

4. **Verify installation**:
   ```
   Verify Git installation by running 'git --version'
   ```

#### Method B: Using Terminal (Manual)

1. **Open Terminal** in Cursor or macOS Terminal app

2. **Install Git**:
   ```bash
   brew install git
   ```
   - This downloads and installs the latest version of Git
   - You'll see progress messages as it installs
   - This typically takes 2-5 minutes

3. **Verify installation**:
   ```bash
   git --version
   ```
   - You should see output like `git version 2.x.x` or similar
   - If you see an error, try closing and reopening your terminal

---

### Step 4: Alternative - Install Git Using Xcode Command Line Tools (macOS)

If you prefer not to use Homebrew, you can install Git via Xcode Command Line Tools. This is Apple's official method.

#### Method A: Using Cursor Agent

1. **Open Cursor IDE** and the chat interface (`Cmd+L`)
2. **Ask Cursor Agent**:
   ```
   Install Xcode Command Line Tools which includes Git. Help me complete the installation process.
   ```
3. **Follow the prompts**:
   - Cursor Agent will run the installation command
   - A pop-up window may appear asking you to install Command Line Tools
   - Click "Install" in the pop-up
   - Wait for installation (10-15 minutes)

#### Method B: Using Terminal (Manual)

1. **Open Terminal** in Cursor or macOS Terminal app

2. **Run the installation command**:
   ```bash
   xcode-select --install
   ```
   - This triggers the Xcode Command Line Tools installer

3. **Complete the installation**:
   - A pop-up window will appear asking "The xcode-select command requires the command line developer tools"
   - Click **"Install"**
   - A progress window will show installation status
   - Wait for installation to complete (10-15 minutes)
   - You may be asked to agree to license terms

4. **Verify installation**:
   ```bash
   git --version
   ```
   - You should see output like `git version 2.x.x` or similar

---

## Part 2: Windows Installation

### Step 1: Check if Git is Already Installed

Before installing, check if Git is already on your system:

#### Using Cursor Agent:
1. **Open Cursor IDE**
2. **Open the chat interface** (usually `Ctrl+L` on Windows)
3. **Ask Cursor Agent**:
   ```
   Check if Git is installed on my Windows computer by running 'git --version'
   ```
4. **Review the output**:
   - If you see `git version 2.x.x` or similar → ✅ **Git is installed!** Skip to [Verification](#verification)
   - If you see "command not found" or "'git' is not recognized" → Continue to Step 2

#### Using Command Prompt/PowerShell (Manual):
1. **Open Command Prompt or PowerShell** in Cursor (Terminal → New Terminal) or Windows Command Prompt
2. **Run this command**:
   ```bash
   git --version
   ```
3. **Check the output**:
   - If you see `git version 2.x.x` or similar → ✅ **Git is installed!** Skip to [Verification](#verification)
   - If you see "'git' is not recognized" → Continue to Step 2

---

### Step 2: Install Git Using winget (Windows 11/10 - Recommended)

winget is Windows' built-in package manager (available on Windows 11 and Windows 10 with updates).

#### Method A: Using Cursor Agent

1. **Open Cursor IDE** and the chat interface (`Ctrl+L`)
2. **Ask Cursor Agent**:
   ```
   Install Git for Windows using winget. Run the installation command in an elevated PowerShell.
   ```
3. **Follow the prompts**:
   - Cursor Agent will attempt to run the installation
   - You may need to run PowerShell as Administrator
   - The installation will proceed automatically

4. **Verify installation**:
   ```
   Verify Git installation by running 'git --version'
   ```

#### Method B: Using PowerShell (Manual)

1. **Open PowerShell as Administrator**:
   - Press `Windows Key + X`
   - Select "Windows PowerShell (Admin)" or "Terminal (Admin)"
   - Click "Yes" when prompted by User Account Control

2. **Check if winget is available**:
   ```powershell
   winget --version
   ```
   - If you see a version number, winget is available → Continue to step 3
   - If you see an error, winget may not be available → Skip to Step 3 (Chocolatey) or Step 4 (Official Installer)

3. **Install Git**:
   ```powershell
   winget install --id Git.Git -e --source winget
   ```
   - The `-e` flag accepts the license automatically
   - Wait for installation to complete (2-5 minutes)

4. **Close and reopen your terminal** (important for PATH updates)

5. **Verify installation**:
   ```bash
   git --version
   ```
   - You should see output like `git version 2.x.x` or similar

---

### Step 3: Install Git Using Chocolatey (Windows Alternative)

Chocolatey is a popular third-party package manager for Windows.

#### Method A: Using Cursor Agent

1. **Open Cursor IDE** and the chat interface (`Ctrl+L`)
2. **First, check if Chocolatey is installed**:
   ```
   Check if Chocolatey is installed by running 'choco --version'
   ```
3. **If Chocolatey is not installed, install it**:
   ```
   Install Chocolatey package manager for Windows. Run the installation in an elevated PowerShell.
   ```
4. **Then install Git**:
   ```
   Install Git using Chocolatey
   ```

#### Method B: Using PowerShell (Manual)

**Installing Chocolatey (if not already installed):**

1. **Open PowerShell as Administrator**:
   - Press `Windows Key + X`
   - Select "Windows PowerShell (Admin)"
   - Click "Yes" when prompted by User Account Control

2. **Set execution policy** (if needed):
   ```powershell
   Set-ExecutionPolicy Bypass -Scope Process -Force
   ```

3. **Install Chocolatey**:
   ```powershell
   [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
   ```
   - This downloads and installs Chocolatey
   - Wait for installation to complete

4. **Verify Chocolatey installation**:
   ```powershell
   choco --version
   ```
   - You should see a version number

**Installing Git with Chocolatey:**

1. **Install Git**:
   ```powershell
   choco install git -y
   ```
   - The `-y` flag accepts all prompts automatically
   - Wait for installation to complete (2-5 minutes)

2. **Close and reopen your terminal** (important for PATH updates)

3. **Verify installation**:
   ```bash
   git --version
   ```
   - You should see output like `git version 2.x.x` or similar

---

### Step 4: Install Git Using Official Installer (Windows - Most Reliable)

If package managers aren't available or you prefer a GUI installer, use the official Git installer.

#### Method A: Using Cursor Agent

1. **Open Cursor IDE** and the chat interface (`Ctrl+L`)
2. **Ask Cursor Agent**:
   ```
   Help me download and install Git for Windows from the official website. Guide me through the installation wizard.
   ```
3. **Follow Cursor Agent's guidance**:
   - It will help you navigate to the download page
   - Guide you through the installation wizard
   - Help you configure Git settings

#### Method B: Manual Installation

1. **Download Git for Windows**:
   - Visit: https://git-scm.com/download/win
   - The website will automatically detect your system and show the download link
   - Click the download button to get the installer

2. **Run the installer**:
   - Locate the downloaded file (usually in your Downloads folder)
   - Double-click the installer file (e.g., `Git-2.x.x-64-bit.exe`)
   - Click "Yes" if Windows asks for permission

3. **Follow the installation wizard**:
   - **Information**: Click "Next"
   - **Select Components**: Keep default selections, click "Next"
   - **Choosing the default editor**: Choose your preferred editor (or keep default), click "Next"
   - **Adjusting your PATH environment**: 
     - **Recommended**: "Git from the command line and also from 3rd-party software"
     - Click "Next"
   - **Choosing HTTPS transport backend**: Keep default, click "Next"
   - **Configuring the line ending conversions**: 
     - **Recommended**: "Checkout Windows-style, commit Unix-style line endings"
     - Click "Next"
   - **Configuring the terminal emulator**: Keep default, click "Next"
   - **Configuring extra options**: Keep defaults, click "Next"
   - **Configuring experimental options**: Uncheck experimental options (unless you want them), click "Install"
   - Wait for installation to complete

4. **Complete the installation**:
   - Check "Launch Git Bash" if you want to open it immediately
   - Click "Finish"

5. **Verify installation**:
   - Open Command Prompt or PowerShell (close and reopen if it was already open)
   - Run:
     ```bash
     git --version
     ```
   - You should see output like `git version 2.x.x` or similar

---

## Verification

After installation, verify Git is working correctly:

### Basic Verification

#### Using Cursor Agent:
```
Verify Git installation by running 'git --version' and show me the output. Also check the Git configuration.
```

#### Using Terminal/Command Line:

1. **Check Git version**:
   ```bash
   git --version
   ```
   Should return: `git version 2.x.x` or similar

2. **Check Git configuration**:
   ```bash
   git config --global --list
   ```
   (This may be empty if you haven't configured Git yet)

---

### Configure Git (First Time Setup)

If this is your first time using Git, you need to configure your identity. This information is used for all your Git commits.

#### Using Cursor Agent:
```
Configure Git with my name and email. Use 'Your Name' for the name and 'your.email@example.com' for the email.
```
(Replace with your actual name and email)

#### Using Terminal/Command Line:

1. **Set your name** (replace with your actual name):
   ```bash
   git config --global user.name "Your Name"
   ```
   Example: `git config --global user.name "John Doe"`

2. **Set your email** (use your GitHub email):
   ```bash
   git config --global user.email "your.email@example.com"
   ```
   Example: `git config --global user.email "john@example.com"`

3. **Verify configuration**:
   ```bash
   git config --global --list
   ```
   You should see your name and email listed

---

### Test Git Functionality

#### Using Cursor Agent:
```
Navigate to my project folder and run 'git status' to test Git functionality.
```

#### Using Terminal/Command Line:

1. **Navigate to your project folder**:
   ```bash
   cd /path/to/ad-campaign-demo
   ```
   (Replace with your actual project path)

2. **Check Git status**:
   ```bash
   git status
   ```
   Should show your current branch and any uncommitted changes

---

## Troubleshooting

### macOS Issues

**Problem**: `brew: command not found`
- **Solution**: 
  - Homebrew is not installed. Follow [Step 2: Install Homebrew](#step-2-install-homebrew-macos---recommended-first-step) above
  - Or use the Xcode Command Line Tools method instead

**Problem**: `xcode-select: command not found`
- **Solution**: 
  - You may need to install Xcode from the App Store first
  - Or use Homebrew instead (recommended)

**Problem**: Permission denied errors during Homebrew installation
- **Solution**: 
  - Make sure you're entering your Mac password correctly
  - Ensure your user account has administrator privileges
  - Try running with `sudo` if needed (though Homebrew installer handles this)

**Problem**: Git installed but not found in terminal
- **Solution**: 
  - Close and reopen your terminal completely
  - Check your PATH: `echo $PATH`
  - For Homebrew installations, add to PATH if needed:
    - **Apple Silicon**: `export PATH="/opt/homebrew/bin:$PATH"`
    - **Intel**: `export PATH="/usr/local/bin:$PATH"`
  - Add these lines to your `~/.zprofile` or `~/.zshrc` file to make it permanent

**Problem**: Homebrew installation seems stuck
- **Solution**: 
  - Homebrew installation can take 5-10 minutes
  - Check your internet connection
  - Look for any prompts asking for your password
  - Don't interrupt the installation process

**Problem**: "Failed to connect to raw.githubusercontent.com" during Homebrew install
- **Solution**: 
  - Check your internet connection
  - Try again later (GitHub may be temporarily unavailable)
  - Check if you're behind a firewall or proxy

### Windows Issues

**Problem**: `winget: command not found`
- **Solution**: 
  - Windows 10 users may need to install winget separately or update Windows
  - Use Chocolatey or the official installer instead
  - Check if you're running PowerShell as Administrator

**Problem**: `choco: command not found`
- **Solution**: 
  - Chocolatey is not installed. Follow [Step 3: Install Git Using Chocolatey](#step-3-install-git-using-chocolatey-windows-alternative) above
  - Or use the official installer instead

**Problem**: PowerShell execution policy errors
- **Solution**: 
  - Run PowerShell as Administrator
  - Execute: `Set-ExecutionPolicy RemoteSigned -Scope CurrentUser`
  - Or use: `Set-ExecutionPolicy Bypass -Scope Process -Force` (for current session only)

**Problem**: Git installed but not found in terminal
- **Solution**: 
  - Close and reopen your terminal/Command Prompt completely
  - Restart Cursor IDE
  - Check if Git is in your PATH: `where git` (Windows) or `which git` (macOS)
  - You may need to log out and log back in for PATH changes to take effect

**Problem**: Git Bash vs Command Prompt confusion
- **Solution**: 
  - Git for Windows includes Git Bash (a Unix-like terminal)
  - You can use either Git Bash, Command Prompt, or PowerShell
  - Make sure to use the same terminal consistently
  - Git commands work the same in all of them

**Problem**: Installation wizard closes unexpectedly
- **Solution**: 
  - Run the installer as Administrator (right-click → "Run as administrator")
  - Check Windows Event Viewer for error details
  - Try downloading the installer again

### General Issues

**Problem**: Cursor Agent can't execute installation commands
- **Solution**: 
  - Some installations require user interaction (like clicking "Next" in installers)
  - Cursor Agent can run package manager commands, but GUI installers may need manual completion
  - Use package managers (Homebrew, Chocolatey, winget) for fully automated installation
  - For GUI installers, use Cursor Agent for guidance but complete the wizard manually

**Problem**: Installation seems stuck or taking too long
- **Solution**: 
  - Some installations take 10-15 minutes (especially Xcode Command Line Tools)
  - Check your internet connection speed
  - Look for any pop-up windows that need your attention
  - Don't interrupt the installation process

**Problem**: "Command not found" after installation
- **Solution**: 
  - Close and reopen your terminal completely
  - Restart Cursor IDE
  - Log out and log back into your computer (for PATH changes)
  - Verify the installation completed successfully

---

## Quick Reference: Cursor Agent Commands

### For macOS:

**Check if Git is installed:**
```
Check if Git is installed on my Mac by running 'git --version'
```

**Install Homebrew and Git:**
```
Install Homebrew on my Mac. After installation, install Git using Homebrew. Verify both installations.
```

**Install Git only (if Homebrew exists):**
```
Install Git on my Mac using Homebrew. Verify the installation.
```

**Install Git via Xcode Command Line Tools:**
```
Install Xcode Command Line Tools which includes Git. Help me complete the installation process.
```

### For Windows:

**Check if Git is installed:**
```
Check if Git is installed on my Windows computer by running 'git --version'
```

**Install Git using winget:**
```
Install Git for Windows using winget. Run the installation in an elevated PowerShell and verify it worked.
```

**Install Git using Chocolatey:**
```
Check if Chocolatey is installed. If not, install Chocolatey first, then install Git using Chocolatey.
```

**Install Git using official installer:**
```
Help me download and install Git for Windows from the official website. Guide me through the installation wizard.
```

**Configure Git:**
```
Configure Git with my name '[Your Name]' and email '[your.email@example.com]'
```

---

## Next Steps

After Git is installed and verified:

1. **Continue with the project setup** as described in [README.md](../README.md)
2. **Clone your repository** (if you haven't already):
   ```bash
   git clone [YOUR_REPOSITORY_URL]
   ```
3. **Configure Git** with your name and email (see Verification section above)
4. **Proceed to GitHub Setup** in the main README.md
5. **Then proceed to Netlify Setup** in the main README.md

---

## Additional Resources

- **Git Official Website**: https://git-scm.com
- **Git Documentation**: https://git-scm.com/doc
- **GitHub Guides**: https://guides.github.com
- **Homebrew**: https://brew.sh (macOS)
- **Homebrew Documentation**: https://docs.brew.sh
- **Chocolatey**: https://chocolatey.org (Windows)
- **winget**: https://learn.microsoft.com/en-us/windows/package-manager/winget/ (Windows)
- **Git for Windows**: https://git-scm.com/download/win

---

## Summary

### Quick Installation Commands

**macOS (Recommended - using Homebrew):**
```bash
# Install Homebrew
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# Install Git
brew install git

# Verify
git --version
```

**Windows (using winget):**
```powershell
# Install Git (run as Administrator)
winget install --id Git.Git -e --source winget

# Verify (after restarting terminal)
git --version
```

**Windows (using Chocolatey):**
```powershell
# Install Chocolatey (run as Administrator)
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))

# Install Git
choco install git -y

# Verify (after restarting terminal)
git --version
```

### Configuration (First Time Only)

```bash
# Set your name
git config --global user.name "Your Name"

# Set your email
git config --global user.email "your.email@example.com"

# Verify configuration
git config --global --list
```

---

*Last updated: 2024*
*For project-specific setup, see [README.md](../README.md)*
*For GitHub setup, see [github-setup-instructions.md](github-setup-instructions.md)*
*For Netlify setup, see [netlify-setup-instructions.md](netlify-setup-instructions.md)*
