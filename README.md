# macOS Development Environment Setup

A comprehensive guide for setting up a new MacBook Pro for development work, including security configurations, development tools, and productivity applications.

## Table of Contents

- [Initial macOS Setup](#initial-macos-setup)
- [System Configuration](#system-configuration)
- [Development Environment](#development-environment)
- [Git Configuration](#git-configuration)
- [AI/ML Tools](#aiml-tools)
- [Utilities](#utilities)
- [Communication Tools](#communication-tools)
- [Productivity Applications](#productivity-applications)

## Initial macOS Setup

### 1. Setup Process
- Select your language from the initial screen
- Choose your region/country
- Optional: Configure accessibility settings (can be done later if preferred)

### 2. Account Configuration
- Sign in with your Apple ID (or create a new one)
- Create a user account
- Set a password
- Optional: Add a password hint
- Choose a profile picture or Memoji

### 3. System Customization
- Configure system settings
- Set up Touch ID (if available)
- Customize desktop and dock
- Configure control center
- Adjust display and appearance settings

## System Configuration

Essential system preferences and security configurations for a development machine.

**Important:** First update your system through App Store → Updates and consider upgrading to the latest macOS version.

### General Settings
- **Appearance:** Graphite
- **Highlight color:** Blue
- **Sidebar icon size:** Medium
- **Show scroll bars:** When scrolling
- **Click on scroll bar to:** Jump to the spot that's clicked
- **Default web browser:** Set after installing preferred browser
- **Allow Handoff between this Mac and your iCloud devices:** Unchecked
- **Use LCD font smoothing when available:** Checked

### Desktop & Screen Saver
#### Desktop
- **Background:** Apple → Solid Colors → Solid Gray Medium

#### Screen Saver
- **Screen Saver:** Message or preferred option
- **Start after:** 5 minutes
- **Hot Corners:** Top Left = Start Screen Saver

### Dock Configuration
- **Size:** Closer to small side
- **Position on screen:** Left (or preferred side)
- **Minimize windows using:** Genie effect
- **Prefer tabs when opening documents:** In Full Screen Only
- **Double-click window's title bar to:** Zoom
- **Minimize window into application icon:** Checked
- **Animate opening applications:** Unchecked
- **Automatically hide and show the Dock:** Unchecked
- **Show indicators for open applications:** Checked

### Language & Region
- **Preferred languages:** English (primary), add others as needed
- **Region:** Set to your location
- **First day of week:** Monday
- **Calendar:** Gregorian
- **Time format:** 24-Hour Time
- **Temperature:** °C - Celsius
- **List sort order:** Universal

### Security & Privacy

A development machine requires robust security measures including virus protection, firewall configuration, and disk encryption.

#### General Security
- **Require password:** Immediately after sleep or screen saver begins
- **Disable automatic login:** Checked
- **Allow apps downloaded from:** App Store and identified developers

#### Firewall Configuration
Configure the built-in firewall for network security:

1. System Preferences → Security & Privacy → Firewall tab
2. Click the lock button and enter administrator credentials
3. Click "Turn On Firewall"
4. Click "Firewall Options"
5. Uncheck "Automatically allow signed software to receive incoming connections"
6. Enable stealth mode

This setup requires manual approval for network access, providing better security control.

#### FileVault Disk Encryption
Enable full disk encryption for data protection:

1. System Preferences → Security & Privacy → FileVault tab
2. Click the lock button and enter administrator credentials
3. Click "Turn On FileVault"
4. Follow the setup wizard
5. Create a recovery key and store it securely offline

**Note:** FileVault provides essential data protection, especially for portable devices.

#### Privacy Settings
- **Enable location services:** Unchecked (unless needed)
- **Diagnostic & Usage:** Unchecked

#### Advanced Security
- **Require administrator password to access system-wide preferences:** Checked

### Display Settings
- **Resolution:** Scaled (choose preferred scaling)
- **AirPlay Display:** Off

### Energy Saver
- **Turn display off after:** 5 minutes
- **Put hard disks to sleep when possible:** Checked
- **Slightly dim display when on battery power:** Checked
- **Enable Power Nap while on battery power:** Unchecked
- **Show battery status in menu bar:** Unchecked (iStat Menus provides better monitoring)

### Trackpad Configuration
#### Point & Click
- **Lookup and data detectors:** Checked
- **Secondary click:** Checked
- **Tap to click:** Personal preference
- **Click:** Medium
- **Tracking speed:** Fourth mark (adjust to preference)
- **Silent clicking:** Unchecked
- **Force click and haptic feedback:** Checked

#### Scroll & Zoom
- Enable all scroll and zoom gestures

#### More Gestures
- Enable all gesture options for productivity

### iCloud Setup
Configure iCloud services based on your needs:
- iCloud Drive, Photos, Calendar, Contacts
- Find My Mac for device security
- Sync preferences based on privacy requirements

### App Store Settings
- **Automatically check for updates:** Checked
- **Auto-download updates:** Unchecked (manual control recommended)
- **Password settings:** Always require password

### Users & Groups
Create secure user account structure:

#### User Management
- **Turn off Guest User:** For security
- **Create Admin profile:** For system administration
- **Create standard user profile:** For daily work (principle of least privilege)
- **Profile setup:** Configure password, Apple ID, profile picture

#### Login Options
- **Automatic login:** Unchecked
- **Display login window as:** Name and password
- **Show Sleep, Restart, and Shutdown buttons:** Checked
- **Show input menu in login window:** Unchecked
- **Show password hints:** Unchecked
- **Show fast user switching menu as:** Full Name
- **Use VoiceOver in login window:** Unchecked

### Additional System Settings

#### Spotlight
- Disable unnecessary search categories (fonts, images, files)
- Disable keyboard shortcuts (replaced by Alfred)

#### Siri
- **Enable Siri:** Unchecked (or configure based on preference)

#### Bluetooth
- Configure to be non-discoverable when not needed

#### Sharing
- Disable all sharing services unless specifically required

#### Finder Customization
##### Toolbar
- Add useful items: Path, New Folder, Delete

##### Sidebar
- Add: Home directory, Code directory
- Remove: Shared, Tags (unless needed)
- Set new Finder windows to open in home directory

## Development Environment

### XCode Command Line Tools
```bash
xcode-select --install
```

### Homebrew Package Manager
Install Homebrew from [brew.sh](https://brew.sh/):
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
brew update
brew upgrade
```

### Terminal Setup
Install iTerm2 and configure for the best terminal experience:
```bash
brew install --cask iterm2
```

Install Oh My Zsh for enhanced shell experience:
```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

Install additional terminal tools:
```bash
brew install fzf
```

For zsh-autosuggestions, follow the [official guide](https://github.com/zsh-users/zsh-autosuggestions).

### Development Tools
```bash
# Python environment manager
brew install uv
uv python install

# Code editor
brew install --cask visual-studio-code

# Container management
brew install podman-desktop
```

### Claude Code
Install Claude Code CLI tool for AI-powered development assistance:
```bash
# Install via curl (recommended)
curl -fsSL https://claude.ai/install.sh | sh

# Or install via npm
npm install -g @anthropic-ai/claude-code
```

Verify installation:
```bash
claude --version
```

Set up your API key:
```bash
claude auth login
```

Learn more about Claude Code features and usage at [docs.anthropic.com/claude-code](https://docs.anthropic.com/en/docs/claude-code).

For best practices and advanced usage, see the [Claude Code Best Practices Guide](https://www.anthropic.com/engineering/claude-code-best-practices).

For Docker alternative setup with Podman, see [this guide](https://nilesh93.medium.com/replacing-docker-desktop-with-podman-and-kind-in-macos-c750581a3fda).

### System Monitoring
```bash
brew install macmon
```

Learn more about [macmon](https://github.com/vladkens/macmon).

## Git Configuration

### Installation
```bash
brew install git
```

Verify installation:
```bash
git --version
which git  # Should output /usr/local/bin/git
```

### Global Configuration
```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
git config --global core.editor code
git config --global credential.helper osxkeychain
```

### SSH Key Setup
Generate a new SSH key using ed25519 encryption:
```bash
ssh-keygen -t ed25519 -C "your@email.com"
```

Add the SSH key to the SSH agent:
```bash
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
```

### GitHub SSH Configuration
1. Copy your public key to clipboard:
   ```bash
   cat ~/.ssh/id_ed25519.pub
   ```
2. Go to GitHub Settings → SSH and GPG keys → New SSH key
3. Paste your public key and save

### Global Git Ignore
Create `~/.gitignore` to exclude common system files:
```bash
# Folder view configuration files
.DS_Store
Desktop.ini

# Thumbnail cache files
._*
Thumbs.db

# Files that might appear on external disks
.Spotlight-V100
.Trashes

# Compiled Python files
*.pyc

# Compiled C++ files
*.out

# Application specific files
venv
node_modules
.sass-cache
```

Then configure Git to use it globally:
```bash
git config --global core.excludesfile ~/.gitignore
```

### Test Your Setup
Clone a repository using SSH to verify everything works:
```bash
git clone git@github.com:username/repository.git
```

## AI/ML Tools

### Ollama
Install Ollama for local AI model management:
```bash
brew install --cask ollama
```

Pull useful models:
```bash
ollama pull llama3
ollama pull starcoder2:3b
ollama pull qwen2.5-coder:7b
ollama pull deepseek-r1:7b
ollama pull qwen2.5:14b
```

Test your installation:
```bash
ollama run deepseek-r1:7b
```

### Open WebUI
Install Open WebUI for a web-based interface to your local models:
```bash
docker pull ghcr.io/open-webui/open-webui:main
```

Run with authentication disabled for single-user setup:
```bash
docker run -d -p 3000:8080 -e WEBUI_AUTH=False -v open-webui:/app/backend/data --name open-webui ghcr.io/open-webui/open-webui:main
```

## Utilities

Essential utility applications:
```bash
brew install --cask 1password          # Password manager
brew install --cask istat-menus        # System monitoring
brew install --cask little-snitch      # Network monitor
brew install --cask calibre            # E-book management
brew install --cask dropbox            # Cloud storage
brew install --cask onyx               # System maintenance
brew install --cask keka               # Archive utility
brew install --cask chatgpt            # OpenAI ChatGPT
brew install mas                       # Mac App Store CLI
```

Install Kindle from the App Store, or use:
```bash
mas install 302584613  # Kindle
```

Install Perplexity.ai:
```bash
mas install 6714467650
```

## Communication Tools

```bash
brew install --cask zoom               # Video conferencing
brew install --cask webex              # Cisco WebEx
brew install --cask whatsapp           # Messaging
brew install --cask alfred             # Productivity launcher
```

## Productivity Applications

```bash
brew install --cask google-chrome              # Web browser
brew install --cask vlc                        # Media player
brew install --cask microsoft-office-businesspro  # Office suite
brew install --cask gimp                       # Image editor
```

---

## Additional Resources

- [Python UV Guide](https://www.datacamp.com/tutorial/python-uv)
- [Getting Started with Zsh on MacBook](https://medium.com/@luzhenna/getting-started-with-zsh-on-a-macbook-bd1c98c6f383)
- [Oh My Zsh Installation](https://ohmyz.sh/#install)
- [Git SSH Key Setup](https://docs.github.com/en/authentication/connecting-to-github-with-ssh)

For additional system security and privacy considerations, refer to the [System Configuration](#system-configuration) section above.