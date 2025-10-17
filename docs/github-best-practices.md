# GITHUB BEST PRACTICES

![GitHub Banner](./assets/github-banner.png)

## CREATING A REPOSITORY

Creating a repository, like starting a new project, can be a bit of a daunting task. These guidelines can help you make sure you your space stays organised!

### 1. Naming Your Repo

While there is a long history of giving repositories proper names, like _LightRAG_ or _Fabric_, in the context of company work, it is important to always label your repositories clearly and **consistently**.

"Clearly" simply means "in a way which is clearly descriptive of the project", whereas "consistently" means making sure you are using **common naming conventions** to ensure your repository names are easily intepretable. Below is a set of recommended naming conventions:

**Style Guides**

| **Aspect**                                   | **Rule / Example**                                                     | **Explanation**                                                                                                |
| -------------------------------------------- | ---------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| **Case style (kebab case)**                               | `lowercase-with-hyphens`                                               | Use lowercase letters and hyphens (`-`) to separate words. Avoid spaces or underscores for better readability. |
| **Avoid special characters**                 | ✅ `data-visualization`<br>❌ `data_visualization!`                      | Only use letters, numbers, and hyphens. Special characters can cause issues in URLs.                           |
| **Keep it short and clear**                  | ✅ `math-games`<br>❌ `my-awesome-mathematics-educational-games-project` | Shorter names are easier to remember and type. Aim for 2–4 words that describe the project.                    |
| **Be descriptive**                           | ✅ `quiz-app`<br>❌ `project1`                                           | Use words that describe what the repository does or contains.                                                  |
| **Avoid redundant words**                    | ❌ `repo`, `project`, `codebase`                                        | These words don’t add useful meaning — your repo is already a project!                                         |


### 2. Repo Settings

- Repository shuold always be **private**
- Repository should **never** include API keys or internal comany passwords.
    - Instead, add these to a `.env` file and add it to your `.gitignore`!


## COMMITS

### 1. General

- **Balance between too small commits and too big commits!** -- committing every time you fix a typo or type a new word can get exhausting. On the other hand, waiting too long between changes to make a commit can be risky. Listen to you hear and ask youself "If I lost these latest changes, would I be heartbroken?". If the answer is yes... commit!
- **Commit intelligently** -- you can commit multiple files at the same time (i.e. `git add file1.py file3.py`). While this isn't wrong, it's better to be strategic about bundling multiple files under the same _commit message_ as this can make it harder to track down your changes.


### 2. Commit Message Best Practices

While git will _technically_ allow you to write a nonsense commit message (e.g. "adiuhag" or "new updates"), the whole purpose of github is to make your changes trackable, understandable and intuitive.

Here a few tips you can follow to make your commit messages better!

**1. Start with a tag**

Virtually all changes you make can be grouped under on eof the categories below:

- **feat**: used when the changes involves introducing a new feature
- **fix**: used when fixing an issue, typo, bug, etc
- **refac**: useful when you have simply re-strucutred or re-written something without changing the functionality or behaviour of the code itself
- **docs**: useful when making changes to documents (READMEs and readmes)
- **chore**: anything else that doesn't fall under the above tags/


**2. Add a one-line summary**

Think purpose! Describe briefly the issue that was fixed, or the feature that was added. Examples:

> fix: fixed typo at paragraph 2

> feat: unsubscribe button

> refac: simplified tool-calling for agents

**3. Add key details**

Take a little extra time to add a few extra bulletpoints outlining excatly what was changes to achieve your goal. It can be useful to mention key sections of your script/file, and what was done to them. For example:

> refac: simplified tool-calling for agents
> - Merged AdditionTool with MultiplicationTool into MathTool
> - Modified agent instructions to reflect MathTool usage

> [!NOTE]
> Some changes are simple and self-describing. Don't worry about adding more detail if not necessary!


> [!TIP]
> The `aicommit` shortcut included in this repository already follows these rules! So feel free to use it run your commits without the adminy pain


## DEVELOPMENT

- **Don't fear branches** -- If your codebase is working and you wanna add a new feature, simply start a new branch and **merge** it later! You can ask AI to do this for you and it will handle any conflicts!
    - Note: before creating a new branch **always try to commit your latest changes to `main`**
- **Starting over** -- `git restore` is always there for you. If you suddenly found yourself lost in a sea of ineffective changes, you can always go back to your latest working version


