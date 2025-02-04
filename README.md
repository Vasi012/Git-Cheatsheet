<h1 align="center" style="color: #FF4500; background-color: #222; padding: 10px; border-radius: 10px;">🚀 Working with Git in Teams: A Cheatsheet for Success 🎯</h1>

This guide is designed to help teams collaborate efficiently using Git. It outlines a structured workflow that keeps your commit history clean, prevents merge conflicts, and ensures that everyone is working smoothly. 🛠️

## <span style="color: #FF4500; background-color: #222; padding: 5px; border-radius: 5px;">🎯 Why Follow This Workflow?</span>

Using a consistent workflow makes it easier for teams to manage code, review changes, and avoid messy histories. Following these steps ensures that everyone is working in an organised manner while reducing errors and conflicts. ✅

## <span style="color: #FFA500; background-color: #222; padding: 5px; border-radius: 5px;">📌 Overview of the Workflow</span>

1. **🆕 Create a new branch**: Work on a feature or fix in an isolated branch.
2. **💾 Develop and commit**: Make regular, meaningful commits to track progress.
3. **🔄 Fetch updates**: Keep your branch updated with the latest changes from the remote repository.
4. **🧹 Squash commits**: Clean up your commit history by consolidating multiple commits.
5. **🔗 Merge into main**: Integrate the feature branch into the `main` branch in a structured way.
6. **🗑️ Cleanup**: Delete the feature branch after it has been merged to keep things tidy.

## <span style="color: #008CBA; background-color: #222; padding: 5px; border-radius: 5px;">📝 Step-by-Step Guide</span>

### 1️⃣ Create a New Branch

Before you start working on a new feature or bug fix, create a new branch. This ensures that your work is separate from the `main` branch, preventing unfinished or experimental changes from affecting stable code.

<pre style="background-color: #2E2E2E; color: #FFFFFF; padding: 10px; border-radius: 5px;"><code>
# Create a new feature branch
git branch vp_new_feature
  
# Switch to the new branch
git checkout vp_new_feature
</code></pre>

Using a naming convention (like your initials followed by the feature name) makes it clear who is working on what. ✨

### 2️⃣ Develop and Commit Your Work

As you make progress, commit your changes frequently. This keeps your work organised and makes it easier to track changes.

<pre style="background-color: #2E2E2E; color: #FFFFFF; padding: 10px; border-radius: 5px;"><code>
# Stage all modified and new files
git add .
  
# Commit the changes with a descriptive message
git commit -m "Added a new feature to improve user experience"
  
# Push your branch to the remote repository
git push origin vp_new_feature
</code></pre>

Regular commits make it easier to understand what changes were made and when, helping both you and your team. 🔍

### 3️⃣ Keep Your Branch Updated

Before merging your branch, ensure it's up to date with the latest changes from `main`. This prevents merge conflicts later. 🔄

```bash
git fetch
```

Fetching retrieves the latest updates from the remote repository without affecting your local changes.

### 4️⃣ Squash Commits

Instead of merging lots of small commits into `main`, it's best to combine them into a single meaningful commit. This keeps the history clean and readable. 📖

```bash
# Start an interactive rebase
git rebase -i origin/main
```

In the rebase interface, change `pick` to `s` (squash) for all but the first commit. This merges them into one commit while keeping a clear message.

### 5️⃣ Merge Your Work into Main

Once your feature is complete and your commits are clean, merge your branch into `main`. ✅

```bash
# Switch to the main branch
git checkout main

# Merge the feature branch into main
git merge vp_new_feature
```

After merging, push the updated `main` branch to the remote repository. 📤

```bash
# Push changes to the remote main branch
git push origin main
```

### 6️⃣ Cleanup: Delete the Feature Branch

Once your work is merged, delete your branch to keep the repository organised. 🗑️

```bash
# Delete the branch from the remote repository
git push origin --delete vp_new_feature

# Delete the branch locally
git branch -d vp_new_feature
```

## <span style="color: #673AB7; background-color: #222; padding: 5px; border-radius: 5px;">💻 Using This Workflow in VSCode</span>

VSCode has built-in Git integration, making this workflow even easier:

- **🖥️ Branch Management**: Click the branch name in the bottom left corner to switch or create branches.
- **💾 Committing Changes**: Open the Source Control tab (`Ctrl + Shift + G` / `Cmd + Shift + G` on Mac) to stage, commit, and push changes.
- **🔄 Fetching Updates**: Use `Ctrl + Shift + P` / `Cmd + Shift + P` and search for `Git: Fetch`.
- **🧹 Rebasing & Squashing Commits**: Run `Git: Rebase` from the command palette.
- **⚠️ Resolving Merge Conflicts**: If a conflict arises, VSCode highlights conflicting lines and provides an easy interface for choosing the correct version.

## <span style="color: #E91E63; background-color: #222; padding: 5px; border-radius: 5px;">🖥️ Windows, MacOS, and Linux Instructions</span>

### **🖥️ Windows Users**
If using Git Bash or Command Prompt:
```bash
# Open Git Bash or Terminal

cd path/to/your/repo
git checkout -b feature_branch
```

### **🐧 Linux Users**
If using Terminal:
```bash
# Open Terminal

cd ~/path/to/your/repo
git checkout -b feature_branch
```

### **🍏 MacOS Users**
If using Terminal or iTerm:
```bash
# Open Terminal or iTerm

cd ~/path/to/your/repo
git checkout -b feature_branch
```

Everything else works the same on all systems. 🔄

## <span style="color: #795548; background-color: #222; padding: 5px; border-radius: 5px;">🌟 Best Practices</span>

- **✅ Commit often and with clear messages**: This makes tracking changes easier.
- **🔄 Keep your branch updated**: Avoid merge conflicts by fetching the latest changes.
- **📌 Use descriptive branch names**: This helps your team understand what each branch is for.
- **🧹 Squash commits before merging**: This keeps the Git history clean and readable.

By following this workflow, you and your team can collaborate efficiently while keeping your repository organized and easy to navigate. 🚀

---

<p align="center"><i>This README is based on the Git team workflow cheatsheet by James Chambers. <a href="https://jameschambers.co.uk/git-team-workflow-cheatsheet" style="color: #FF4500;">jameschambers.co.uk</a></i></p>
