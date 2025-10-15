# WINDOWS SETUP INSTRUCTIONS

In this doc you'll find the instructions you need to make sure you're ready to go for vibe-coding from your Linux terminal!


## NodeJS

NodeJS allows you to run JavaScript-based applications and commands

**1. Update System**

```
sudo apt update
sudo apt upgrade
sudo apt install -y curl
```

**2. Install the NodeJS Source Repository**

```
curl -fsSL https://deb.nodesource.com/setup_20.x | sudo -E bash -
```

**3. Install NodeJS**

```
sudo apt install -y nodejs
```

**4. Verify Installation**


```
node -v
npm -v
```

## Coding CLI Tools

**Gemini CLI**

```
sudo npm install -g @google/gemini-cli
```

**Codex CLI**

```
sudo npm install -g @openai/codex
```

## VSCode

VSCode is a GUI code editor which seamlessly integrates with extensions such as `codex`, `claude code`, etc.

If you'll be vibe-coding, I recommend installing VSCode as it will allow you to make changes more easily if you ever need to make small manual edits.

You can install VSCode from the Windows app store.


