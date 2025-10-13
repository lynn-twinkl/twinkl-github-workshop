# 🚀 STARTER GITHUB CHEAT SHEET

This cheet sheet covers basic GitHub commands alongside their meanings and functions

## ⚙️  SETUP

Initialising and cloning repositories

### 1. Initialising a Git Repository

```
git init
```
This command creates a hidden `.git` subdirectory in your current working directory that will keep track of all the changes in your codebase

Note this does not actually create a new repository on GitHub, it only initialises Git inside your directory such that it can later work alongside GitHub to store your changes and versions in the cloud.

### 2. Creating a Github Respository

```
gh repo create your-repo-name --private --source=. --remote=origin
```

The command below will actually let GitHub know that you want to store your proejct's repository in their servers

> [!IMPORTANT]
> Note that the `--private` flag means that your repository will only be accessible to you and other people you explicitly invite as collaborators. In order to stay legally in the clear, always make sure your company repos are set to private.

### 3. Cloning a Repository

Sometimes you wanna copy a repository from the GitHub GUI into your local machine such that you can make use of the codebase or even make changes to it. In order to so, you can use 

```
git clone git_repo_url
```

## 📸 STAGING & SNAPSHOTS

This section covers everything to do with viewing, updating and understadning the latest state of your repository.

### 1. Current Status

```
git status
```

This command will print to your terminal a list of all **local** files which either **differ from the latest remote changes** (those which have already been _pushed_ to GitHub), or file which are not being tracked by your remote repository (i.e. they have never been added ot GitHub)

## 💾 COMMIT & PUSH

Once you have finished making your desired changes locally and are ready to push them to the cloud, you can run the following sequence:

### 1. Commit Your Changes To Git

```
git add path/to/your/file
```

This registers your local changes to your **local** Git repository. In other words, it adds all the latest changes to the version history

### 2. Add obliagtory Commit Message

```
git commit -m "This is a commit message"
```

This adds the obligatory commit message in order to describe the nature of the latest changes that you made.

> [!TIP]
> View `./github-best-practices.md` in order to learn how to write snappy, useful, and effective commit messages.

> [!TIP]
> Writing commit messages can be a pain, especially during long coding sessions... let AI do  it for you!
> Run `aicommit path/to/your/file` to get AI to write your message

### 3. Pushing to GitHub

This is where the magic happens. Now that we have properly saved our newly-changed files, as well as their history and fingerprints to Git, it is time to push all our changes remotely, to our GitHub repository where they can live safely.

```
git push
```

or if pushing to a **brand new repo for the very first time**

```
git push -u origin main
```

> [!NOTE]
> Sometimes your main repo branch may be called 'master'
> To find out which you're on, run `git status`. You should see something like:

```
On branch main
Your branch is up to date with 'origin/main'.
```

