# INSTALLING WSL ON WINDOWS VM

This documentation is internal to the trainer. It outline how to install WSL on a Windows virtual machine running via UTM on Mac.

## CONTEXT

Since WSL2 leverages nested virtualisation, which is not possible via MacOS, we can only use WSL1. This document outlines how to enable the installation.


## INSTALLATION

**1. Enable WSL system**

```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```
**2. Disable WSL 2**

```powershell
dism.exe /online /disable-feature /featurename:VirtualMachinePlatform /norestart
```
**3. Install WSL**

```powershell
wsl --install
```
**4. Reboot Windows VM**

I recommend using the reboot option via the Windows menu

**5. Pin WSL1 as defailt version**

```powershell
wsl --set-default-version 1
```

**6. Install Distro**

```powershell
wsl --install -d Ubuntu
```

## ENABLING VSCODE

### 1. Install VSCode

Install via Windows store or website

### 2. Install WSL extension

Once you've installed the WSL extension, make sure to connect it to your remote via de Command Palette `F1 > WSL: Connect to WSL`

### 3. Test CLI Extension

Open a new Powershell window and test `code --help` or `code file.txt` to make sure it opens VSCode

### 4. Enable Code via WSL

**Check path to your code command from WSL**

```bash
which code
```
Should be something like `/mnt/c/Users/Lynn/AppData/Local/Programs/Microsoft VS Code/bin/code`

**Verify if VSCode is in our WSL PATH**

```bash
echo $PATH | grep code
```

**Add code to PATH if necessary**

```bash
echo 'export PATH=$PATH:"path/to/vscode"' >> ~/.bashrc
```

