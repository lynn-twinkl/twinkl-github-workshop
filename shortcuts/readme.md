# CLI SHORTCUTS

This directory contains useful bash scripts that you can take advantage of in order to make your command line adventures a litle smoother!

Please make sure you read this documentation prior to running or installing any of the commands.


# REQUIREMENTS

Some of the scripts in this directory have external dependencies that need to be installed prior to running.

## 1. FABRIC

Fabric is a **lightweight utility** that allows us to make use of AI seamlessly via templated prompts. Think of it like **Custom GPTs**, except crowd tested and validated, and right from the commands line

### Installation

**1. Install on Unix/Linux/MacOS**

```bash
curl -fsSL https://raw.githubusercontent.com/danielmiessler/fabric/main/scripts/installer/install.sh | bash
```

**2. Add to PATH**

WSL:

```bash
echo 'export PATH=$PATH:$HOME/.local/bin' > ~/.bashrc
```
MacOS:

```bash
echo 'export PATH=$PATH:$HOME/.local/bin' > ~/.zshrc
```
