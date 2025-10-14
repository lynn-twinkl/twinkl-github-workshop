# 🚀 STARTER GITHUB CHEAT SHEET

This cheet sheet covers basic GitHub commands alongside their meanings and functions

## ⚙️  CREATING A REPO

1. **Create a directory for your codebase:** `mkdir new-dir`
2. **Go into thwe new directory:** `cd new-dir`
3. **Initialise Git:** `git init`

> [!NOTE]
> This command creates a hidden `.git` subdirectory in your current working directory that will keep track of all the changes in your codebase. It does **not** create a new remote repository on GitHub.

4. **Create a new remote repo from your local directory:**

```
gh repo create your-repo-name --private --source=. --remote=origin
```
> [!IMPORTANT]
> Note that the `--private` flag means that your repository will only be accessible to you and other people you explicitly invite as collaborators. In order to stay legally in the clear, always make sure your company repos are set to private.

> [!TIP]
> You can use the `createrepo` shortcut included in this repository to automate this!

5. **Add your files!** - Using codex, claude, or your own two hands. Files can incldue images, text, code, etc.

6. **Make your first commit:** add all directory contents using `git add .`
7. **Write your first commit message**: `git commit -m "Your message here!"`
8. **Push your changes to the cloud**: `git push -u origin main` or `git push -u origin master`
    - For subsequent pushes, you can ommit the '-u origin main' argument

> [!NOTE]
> To check whether your main branch is called 'main' or 'master', run `git status`

## ✨ CLONING REPOSITORIES

Sometimes you might want to copy a repository from GitHub into your local machine such that you can make use of the codebase or even make changes to it. Here's how to do it!

1. Go to the relevant github repository online (See [Flowise](https://github.com/FlowiseAI/Flowise) for example)
2. In there, you'll find a <code style="color:green">green button</code> that says 'Code'. Click on that button, and copy the URL listed in the popup window
3. Go to your terminal and run `git clone copied-repo-url`
4. Go into your new copy of the repo with `cd repo-name`
 

## 📸 STAGING & SNAPSHOTS

This section covers everything to do with viewing, updating and understadning the latest state of your repository.

### 1. Current Status

```
git status
```

This command will print to your terminal a list of all **local** files which either **differ from the latest remote changes** (those which have already been _pushed_ to GitHub), or file which are not being tracked by your remote repository (i.e. they have never been added ot GitHub)

### 2. Restoring Local Files

**1. Individual Files**

To revent a local file to the latest commited vesion on Github:

```
git restore path/to/file
```

**2. Entire codebase**

To restore entire codebase to latest committed changes for each respective file:

```
git restore .
```

> [!NOTE]
> This command will not delete any newly created local files that have never been commited. After running this command, you should still se eyour files undes `git status`

### 3. Seeing Changes

**See current changes made to individual files:**

```
git diff path/to/file
```

or use `aigd path/to/file` to view an AI made summary of the changes (requires `fabric`. See `./shortcuts/readme.md`)

**See history of changes:**

- Use `git log` to view a list of all your file commits
- Use `git log path/to/file` to view all commits for a specific file


## 💾 COMMIT & PUSH

Once you have finished making your desired changes locally and are ready to push them to the cloud, you can run the following sequence:

1. **Select files to commit**: `git add path/to/your/file`
2. **Write commit message**: `git commit -m "This is a commit message"`
3. **Push your changes to remote (GitHub)**: `git push`

> [!TIP]
> View `./github-best-practices.md` in order to learn how to write snappy, useful, and effective commit messages. Alternativelty, let AI do it for you! See `./shortcuts/readme.md`

## 🧪 MOVING & REMOVING FILES

### 1. Renaming or Moving Files

**Files previously committed and pushed**

```
git mv path/to/old_filename path/to/new_filename
``` 

> [!IMPORTANT]
> When working inside a git repostiry, make sure you always add `git` before `mv`. This will ensure that the movement or renaming of the file is also tracked in your repo. Same applies for `rm` commands.

**Local-only files**

```
mv path/to/old_filename path/to/new_filename
```

Since these files are not being tracked at all by Git, you can just move or rename them normally using bash commands

### 2. Removing Files

**Files previously committed and pushed**

```
git rm path/to/file
```
This will remove the specified file from **future commits**, however, the file will remain in Git's verion history.

```
git rm --cached path/to/file
```

This will fully, permanently remove the file from both future commits as well as from the version history.

> [!CAUTION]
> This command should only be used in situations where you accidentally committed highly-sensitive information, such as API keys.


**Local-only files**

```
rm path/to/file
```

> [!WARNING]
> Removing an uncommitted file is absolutely permantent and cannot be undone.

