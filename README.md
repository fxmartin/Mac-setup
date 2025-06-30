# Notes for installing a new Macbook Pro

## Install macOS

**1. Setup Process**
- Select your language from the initial screen
- Choose your region/country
- Optional: Configure accessibility settings (can be done later if preferred)

**2. Account Configuration**
- Sign in with your Apple ID (or create a new one)
- Create a user account
- Set a password
- Optional: Add a password hint
- Choose a profile picture or Memoji

**3. System Customization**
- Configure system settings
- Set up Touch ID (if available)
- Customize desktop and dock
- Configure control center
- Adjust display and appearance settings

## Install XCode
```
xcode-select –-install
```

## Install Homebrew
```
https://brew.sh/
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
brew update
brew upgrade
```

## Install packages
```
brew install --cask iterm2
```
https://medium.com/@luzhenna/getting-started-with-zsh-on-a-macbook-bd1c98c6f383

Install ‘oh my zsh’ for the best terminal experience:
https://ohmyz.sh/#install
```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
Install zsh-autosuggestions:
https://github.com/zsh-users/zsh-autosuggestions
```
brew install fzf
```
### Install development packages
(https://www.datacamp.com/tutorial/python-uv?dc_referrer=https%3A%2F%2Fwww.google.com%2F)
```
brew install git
```
#### Set-up GIT
```
git config --global user.name "fxmartin"
git config --global user.email "enteryourmailhere"
git config --global core.editor code
git config --global credential.helper osxkeychain
git config --global --list
ssh-keygen -t ed25519 -C "enteryourmailhere"
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
```
Add the public key to your GitHub account:
- Copy the contents of `~/.ssh/id_ed25519.pub`.
- Go to GitHub Settings > SSH and GPG keys > New SSH key.
- Paste your public key and save
Clone a private repository
```
git clone git@github.com:username/repository.git
```
You will be prompted for your SSH key passphrase if you set one.
```
brew install uv
uv python install
brew install --cask visual-studio-code
brew install podman-desktop
https://nilesh93.medium.com/replacing-docker-desktop-with-podman-and-kind-in-macos-c750581a3fda
brew install --cask ollama
ollama pull llama3
ollama pull starcoder2:3b
ollama pull qwen2.5-coder:7b
ollama pull deepseek-r1:7b
ollama pull qwen2.5:14b
```
https://github.com/vladkens/macmon
```
brew install macmon
```
**Test Ollama**
```
ollama run deepseek-r1:7b
```
**Install OpenWebUI**
```
docker pull ghcr.io/open-webui/open-webui:main
```
To bypass the login page for a single-user setup, set the WEBUI_AUTH environment variable to False:
```
docker run -d -p 3000:8080 -e WEBUI_AUTH=False -v open-webui:/app/backend/data --name open-webui ghcr.io/open-webui/open-webui:main
```

### Install utilities
```
brew install --cask 1password
brew install --cask istat-menus
brew install --cask little-snitch
brew install --cask calibre
brew install --cask dropbox
brew install --cask onyx
Install Kindle with App Store
brew install --cask keka
brew install --cask chatgpt
brew install mas
# Install Perplexity.ai
mas install 6714467650
brew install --cask claude
```
Install iMCP from (https://imcp.app/download)
### Install Communication packages
```
brew install --cask zoom
brew install --cask webex
brew install --cask whatsapp
brew install --cask alfred
```
### Install Office tasks
```
brew install --cask arc
brew install --cask vlc
brew install --cask microsoft-office-businesspro
brew install --cask gimp
```
