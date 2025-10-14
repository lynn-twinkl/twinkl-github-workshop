# README

Hello everyone! This is a plyground repository contianing a few different tips and goodies for you to learn to play with the github CLI and to help you vibe-codinx experience go much more smoothly.

**In this repo you'll find:**

- Command line shortcuts to make your life easier
- A GitHub cheat sheet!
- A WSL installation guide for Windows
- Installation instructions for some useful CLI tools and utilities

 
# ⚙️  REQUIREMENTS

Before getting started, you'll need to make sure you're running the right setup. For the purposes of this training, that means making sure you're running on a **UNIX-based** system, that means having access to either a Linux machine or a MacOS machine.

If you are Windows, **do not panic!** WSL has go your back. WSL is an ultra-lightweight tool that allows us to run Linux inside Windows securely and easily.

> [!IMPORTANT]
> If you are on MacOS, you can skip this section. You're all good to go!

## INSTALLING WSL

**1. Launch an Administrator Powershell**

`Win > Powershell > Run as administrator`

**2. Install the WSL Virtual Machine Platform**

```powershell
wsl --install
```

> [!NOTE]
> You may be prompted to reboot your system. Please restart your computer as you normally would and open a new Administrator Powershell


**3. Install Our Linux Distribution**

```powerhsell
wsl --install -d Ubuntu
```
Wait until you see your **shell prompt** appear at the bottom of your Powershell window once again (that's the bit that looks something like `PS C:\Windows\System32>`). That means the installation is finished. You will be prompted to create a new user.

**4. Create New User**

1. Inside the Windows Powershell, type a new user name (this can be anything) and hit `ENTER`
2. You will then be prompted to type your password.

> [!IMPORTANT]
> Please note that when entering passwords on any command line interface, **you will not see anything being typed out**. You won't see any characters or placeholders, no cursor movement or anything. It will look as if nothing is happening. **This is normal**.
> Please type your password carefully and hit enter when ready

**5. Activate WSL**

This is the fun part! What we've just installed is essentially a TUI-only version of Linux that we can intercat with via our command line! However, in order for your Windows computer to _understand_ when you want to run Linux commands vs Powershell commands, you need to fir activate your WSL virtual machine. To do so, run:

```powershell
wsl
```

You will know you are inside Linux when your **shell prompt** turns <code style="color:green">green</code>

**6. You are DONE!**

You can further verify you are running Linux by checking which SHELL you are running: `which $SHELL`

Should print `/bin/bash`. BASH is the language used for interacting with Linux via the command line!

**7. Exiting WSL**

In order to exit WSL and go back to your normal Windows Powershell, simply run `exit`


# 🧪 GETTING STARTED

## 1. FORK THE REPO

Fork this repo to create your own copy

1. Click on the "Fork" button near the top-right corner of the screen
2. You may change the name or keep the same one
3. Hit "Create fork"

> [!NOTE]
> Forking a repo allows you to not just make a clone of someone else's project, but actually treat your own copy as its own github repository that you can make your own edits and changes to.

## 2. CLONE YOUR FORKED REPO LOCALLY

Now we'll clone your forked repo to your local device. This will allow you to actuall run the commands in this repository as well as to make any relevant changes to it.

> [!TIP]
> For this section I strongly recommend making sure you are in your home directory.
> Run `cd ~` to go home

1. Go to the forked repo via the GitHub GUI and click on the <span style="color:#3E7F41">green _Code_ button</span>
2. On the appearing dropdown panel, you will see a url starting with `https://`. Copy that URL
3. Open your terminal and clone your repo using that URL

```
git clone your_repo_url
```

## 3. ENABLE SHORTCUTS

1. Add the `./shortcuts` directory to you PATH. This will make the shortcuts available from any directory in your device.

```
echo 'export PATH="$HOME/twinkl-github-workshop/shortcuts:$PATH"' >> ~/.bashrc
```

2. Restart your shell with the command

**On Windows running WSL** 

```
source ~/.bashrc
```

**On Mac**

```
source ~/.zshrc
```

You should now be able to use the shortcuts from anywhere by running their name and arguments. See `./shortcuts/readme.md` to learn about the different scripts available in this starter pack

