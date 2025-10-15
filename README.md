# README

![Twinkl Banner](./docs/assets/twinkl-banner.png)

Hello everyone! This is a plyground repository contianing a few different tips and goodies for you to learn to play with the github CLI and to help you vibe-codinx experience go much more smoothly.

**In this repo you'll find:**

```
.
├── docs
│   ├── github-commands.md
│   └── wsl-for-windows-vm.md
├── README.md
├── scripts
│   ├── hello.js
│   ├── hello.py
│   ├── linux-star-wars.sh
│   └── macos-star-wars.sh
└── shortcuts
    ├── aicommit
    ├── aigd
    ├── createrepo
    └── readme.md

4 directories, 11 files
```

- `./shortcuts` - A collection of CLI shortcuts that will make your life easier
- `./shortcuts/readme.md` - Installation instructions for some useful CLI tools and utilities
- `./docs/github-commands.md` - A GitHub cheat sheet
- `./scripts` - A collection of playground scripts you can run and edit as you please
- A WSL installation guide for Windows

 
# ⚙️  REQUIREMENTS

Before getting started, you'll need to make sure you're running the right setup. For the purposes of this training, that means making sure you're running on a **UNIX-based** system, that means having access to either a **Linux machine** or a **MacOS** machine.

If you are Windows, **do not panic!** WSL has go your back. WSL is an ultra-lightweight tool that allows us to run Linux inside Windows securely and easily.

- [Windows Setup Guide](./docs/windows-setup.md)
- [MacOS Setup Guide](./docs/macos-setup.md)


# 🧪 GETTING STARTED

## 1. Fork The Repo

Fork this repo to create your own copy

1. Click on the "Fork" button near the top-right corner of the screen
2. You may change the name or keep the same one
3. Hit "Create fork"

> [!NOTE]
> Forking a repo allows you to not just make a clone of someone else's project, but actually treat your own copy as its own github repository that you can make your own edits and changes to.

## 2. Clone Your Forked Repo Locally

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

## 3. Enable Shortcuts

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

