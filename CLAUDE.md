# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is a Mac setup repository containing documentation and configuration files for setting up a new MacBook Pro for development. The repository is structured as a collection of Markdown files with setup guides and configuration templates.

## Repository Structure

- `README.md` - Main installation guide covering macOS setup, development tools, and package installation
- `Git/` - Git-specific configuration and setup documentation
  - `README.md` - Git installation and SSH configuration guide
  - `gitignore.md` - Template for global gitignore file
- `SystemPreferences.md` - Comprehensive macOS system preferences configuration guide

## Key Setup Components

### Development Environment Setup
The main README provides installation commands for:
- XCode command line tools: `xcode-select --install`
- Homebrew package manager installation and usage
- Terminal setup with iTerm2, oh-my-zsh, and zsh-autosuggestions
- Development tools: Git, Python (via uv), Visual Studio Code, Podman Desktop
- AI/ML tools: Ollama with various models (llama3, deepseek-r1:7b, etc.)

### Git Configuration
Git setup includes both HTTPS and SSH authentication methods:
- Global user configuration with name and email
- Credential helper for macOS keychain
- SSH key generation using ed25519 encryption
- SSH key setup for GitHub authentication

### System Security Configuration
The SystemPreferences.md covers security hardening:
- Firewall configuration with stealth mode
- FileVault disk encryption setup
- User account management with admin and standard user profiles
- Privacy settings and system access controls

## Common Commands

### Package Installation
```bash
# Install Homebrew packages
brew install <package-name>
brew install --cask <cask-name>

# Update Homebrew
brew update && brew upgrade
```

### Git Setup
```bash
# Configure Git user
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
git config --global core.editor code
git config --global credential.helper osxkeychain

# Generate SSH key
ssh-keygen -t ed25519 -C "your@email.com"
ssh-add ~/.ssh/id_ed25519
```

### Ollama AI Models
```bash
# Test Ollama installation
ollama run deepseek-r1:7b

# Pull additional models
ollama pull <model-name>
```

## File Types and Conventions

All documentation files use Markdown format with consistent formatting:
- Headers use `#` syntax
- Code blocks use triple backticks with language specification
- Installation commands are provided in copyable code blocks
- External links reference official documentation and repositories

## Repository Purpose

This repository serves as a comprehensive setup guide for macOS development environments, focusing on security, development tools, and productivity applications. It's designed to be followed sequentially during initial Mac setup or referenced for specific configuration needs.