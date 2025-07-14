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
- Connect to WIFI

### 2. Account Configuration
- Sign in with your Apple ID (or create a new one)
- Create a user account
- Set a password
- Optional: Add a password hint
- Choose a profile picture or Memoji

### 3. System Customization
- Configure system settings
- Set up Touch ID (if available)

#### Customize Finder
Finder is the heart of the macOS file system and by default, it is kind of a mess or atleast that is what I think.
##### Decluttering the Sidebar
The first thing I do is clean up the sidebar.

Out with the default clutter like Tags, Movies, Music, Pictures, and iCloud. I never use them. Even AirDrop gets the axe.

Instead, I pin folders that actually matter to me. These could be local project folders, external drives with current video work, or even cloud storage directories.

The goal is to create a sidebar that works like muscle memory — I open Finder, and bam, everything I need is just a click away.

Through Finder Settings, click Sidebar and only keep Applications, Documents, Downloads, user, iCloud drive, Shared, Laptop, External disks, CD/DVD/ios Devices, Connected servers.

##### Switching to List View
Next, I change the default view to List View.

I also tweak the columns:

I make Date Modified the first column and shorten the date format to keep things tidy.

##### Path Bar & Status Bar: Finding My Way
Have you ever found yourself deep in those subfolders and completely lost?

Enabling the Path Bar under the View menu solves that.

While I’m at it, I enable the Status Bar too. Now I can see how much space is left in any folder I’m in — super handy when dealing with large video files.

##### Customizing the Toolbar: Make It Yours
The default toolbar in Finder is kinda ‘meh’. So I customize it.

Removed: Tags, Groups, Get Info (I can get that by right-clicking).

Added: AirDrop — and this is why I removed it from the sidebar. I use it occasionally, but I don’t want it staring at me 24/7.

Cleaned up the Share Button by editing extensions and removing stuff I never use.

#### Smarter Search & File Associations
By default, Finder searches your entire Mac — but most of the time, I just want to search the folder I’m in. So I change that in Finder Settings → Advanced to “Search current folder”.

#### Fixing the “Recents” Folder
I’ve always had a love-hate relationship with the Recents folder.

Recents folder shows every file you’ve ever opened, which becomes a nightmare over time.

Plus, it doesn’t show folders — and I usually want to get back to folders, not individual files.

My Fix:
I build a custom Smart Folder:

Shows files opened in the last 7 days.
Excludes apps and folders (using the Option key to get a “None of the following” filter when clicking the + criteria button).

Saved it as “Recents” and pinned it to the sidebar.

##### Making the Desktop Useful Again (Thanks, Widgets)
I used to ignore my wallpaper because my desktop was always hidden behind a million windows. But the introduction of interactive desktop widgets changed everything.

Now my desktop is a dashboard:

- Fantastical Calendar — Click on a day and see what’s up.
- HomeKit — Control lights, check on the garage door.
- Weather Widget — For that glanceable forecast.
- Battery Widget — Track my AirPods and mouse levels.
- Shortcuts Folder — All my favorite macros a swipe away (activated with a thumb + three fingers gesture).

Even better:

Widgets turn monochrome when you open apps, and you can change this behavior under System Settings → Desktop & Dock → Widgets.

For widgets I don’t need all the time, like my delivery tracker (Parcel), I tuck them away in the Control Center.

##### Clean Desktop, Clean Mind
Under Finder settings, I disable all desktop icons — external drives, connected servers, etc. I prefer my desktop to feel like a calm, neutral space — not a dumping ground.

##### Dock Customization: Sleek and Efficient
Removed all default apps.

Resized the Dock.

Set position to bottom (side docks might be “smarter,” but I can’t get used to them).

Changed window minimize effect to Scale for faster performance.

Enabled “Minimize windows into app icon” to avoid clutter.

Disabled “Show recent applications” — I like a clean dock.

##### Menu Bar: Trim the Fat
A few small but impactful tweaks:
- Show battery percentage (why isn’t this on by default?).
- Add Bluetooth.
- Remove Spotlight (I use Alfred instead — more on that later).

##### Trackpad Settings: Make It Snappier
Increase pointer speed — macOS’s default is sluggish.

Enable Tap to Click (should be default, really).

Disable Natural Scrolling — I prefer the screen to move in the direction I swipe.

Three-Finger Drag:
Go to System Settings → Accessibility → Pointer Control → Trackpad Options and enable Three-Finger Drag. It’s game-changing for moving windows around.

##### System Settings: Final Touches
Spotlight: Disable indexing of useless stuff like code headers and JSON files.

Apple Watch Unlock: If you have one, enable unlock via Apple Watch.

Touch ID: Add multiple fingerprints — different fingers, different angles.

Network: Prioritize Ethernet over Wi-Fi if you use both.

Keyboard Settings:
Disable autocorrect (except double-space for period).

Sleep: Extend time to sleep from 2 to 20 minutes.

Login: Hide username and profile photo at login.

Display Settings:
Turn off auto-brightness and True Tone (for color accuracy).

Enable Night Shift, or better yet, install f.lux for better control.

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
brew install --cask iterm2          # Advanced terminal emulator with split panes and customization
```

Install Oh My Zsh for enhanced shell experience:
```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

Install additional terminal tools:
```bash
brew install fzf                    # Command-line fuzzy finder for files and history
```

For zsh-autosuggestions, follow the [official guide](https://github.com/zsh-users/zsh-autosuggestions) to enable command autocompletion based on history.

### Development Tools
```bash
# Python environment manager - fast Python package installer and resolver
brew install uv
uv python install

# Code editor - extensible source code editor with rich ecosystem
brew install --cask visual-studio-code

# Container management - desktop application for managing containers and pods
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

### Claude Code Sessions

Install Claude Code Sessions for structured development session management:

```bash
# Clone the repository
git clone https://github.com/iannuttall/claude-sessions.git

# Copy commands to your project (adjust path as needed)
cp -r claude-sessions/commands your-project/.claude/commands

# Create session directory if it doesn't exist
mkdir -p .claude/sessions
touch .claude/sessions/.current-session

# Optional: Add sessions to .gitignore for private session tracking
echo "sessions/" >> .gitignore
```

Available session commands:
- `/project:session-start [name]` - Begin a new development session
- `/project:session-update [notes]` - Add progress updates to current session
- `/project:session-end` - Conclude session with comprehensive summary
- `/project:session-current` - View current session status
- `/project:session-list` - List all past sessions

Features:
- Document development progress and code changes
- Track problem-solving steps and decisions
- Transfer knowledge between coding sessions
- Maintain structured development history

Learn more at [Claude Sessions GitHub](https://github.com/iannuttall/claude-sessions).

### Install yadm

https://yadm.io/docs/getting_started

### Claude Usage Monitoring

Install [https://github.com/ryoppippi/ccusage](https://github.com/ryoppippi/ccusage)

### Context7 MCP

Install Context7 MCP for up-to-date code documentation in Claude Code:

```bash
# Remote server connection (recommended)
claude mcp add --transport http context7 https://mcp.context7.com/mcp

# Alternative SSE transport
claude mcp add --transport sse context7 https://mcp.context7.com/sse

# Local server connection (requires Node.js 18.0.0+)
claude mcp add context7 -- npx -y @upstash/context7-mcp
```

Context7 provides real-time, version-specific documentation for programming libraries. Add "use context7" to your coding prompts to fetch current documentation.

Learn more at [Context7 GitHub](https://github.com/upstash/context7).

For Docker alternative setup with Podman, see [this guide](https://nilesh93.medium.com/replacing-docker-desktop-with-podman-and-kind-in-macos-c750581a3fda).

### System Monitoring
```bash
brew install macmon                  # Real-time system monitoring with CPU, memory, and network stats
```

Learn more about [macmon](https://github.com/vladkens/macmon).

## Git Configuration

### Installation
```bash
brew install git                     # Distributed version control system for tracking code changes
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
brew install --cask ollama           # Run large language models locally on your machine
```

Pull useful models:
```bash
ollama pull qwen2.5-coder:7b         # Alibaba's coding-focused language model (4.7 GB)
ollama pull llama3.1:8b              # Meta's latest general-purpose language model (4.9 GB)
ollama pull gemma3n:latest           # Google's efficient language model (7.5 GB)
```

Test your installation:
```bash
ollama run qwen2.5-coder:7b
```

### Open WebUI
Install Open WebUI for a web-based interface to your local models:
```bash
docker pull ghcr.io/open-webui/open-webui:main    # Web interface for interacting with local AI models
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
brew install --cask flux-app # f.lux app for lights management
```

Install Kindle from the App Store, or use:
```bash
mas install 302584613  # Kindle - e-book reader for Amazon's digital library
```

Install Perplexity.ai:
```bash
mas install 6714467650              # Perplexity - AI-powered search and research assistant

brew install --cask claude         # Claude desktop app - AI assistant for coding and writing

brew install --cask nordvpn        # VPN service - secure internet connection and privacy protection
```

Install iMCP from [imcp.app/download](https://imcp.app/download) - Model Context Protocol server for AI integrations

Install Memory MCP from [src/memory/README.md](src/memory/README.md)

Install Perplexity MCP from [https://github.com/ppl-ai/modelcontextprotocol](https://github.com/ppl-ai/modelcontextprotocol) 

## Communication Tools

```bash
brew install --cask zoom               # Video conferencing platform for meetings and webinars
brew install --cask webex              # Cisco WebEx - enterprise video conferencing solution
brew install --cask whatsapp           # Cross-platform messaging app with end-to-end encryption
brew install --cask alfred             # Productivity launcher with workflows and file search
```

## Productivity Applications

```bash
brew install --cask arc                        # Modern web browser with workspaces and AI features
brew install --cask google-chrome              # Fast web browser with extensive extension ecosystem
brew install --cask vlc                        # Universal media player supporting all video/audio formats
brew install --cask microsoft-office-businesspro  # Complete office suite with Word, Excel, PowerPoint
brew install --cask gimp                       # Free image editor and graphics manipulation program
```

---

## Additional Resources

- [Python UV Guide](https://www.datacamp.com/tutorial/python-uv)
- [Getting Started with Zsh on MacBook](https://medium.com/@luzhenna/getting-started-with-zsh-on-a-macbook-bd1c98c6f383)
- [Oh My Zsh Installation](https://ohmyz.sh/#install)
- [Git SSH Key Setup](https://docs.github.com/en/authentication/connecting-to-github-with-ssh)

For additional system security and privacy considerations, refer to the [System Configuration](#system-configuration) section above.
