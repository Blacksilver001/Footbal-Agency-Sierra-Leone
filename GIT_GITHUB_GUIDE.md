# Git & GitHub Guide: How to Push Your Files to GitHub

This guide will help you push your local files to GitHub step by step.

## Prerequisites
- Git installed on your computer
- A GitHub account
- Your project files in a folder

---

## Step-by-Step Instructions

### 1. Initialize Git in Your Project (First Time Only)

Open Terminal/Command Prompt in your project folder and run:

```bash
git init
```

This creates a hidden `.git` folder that tracks your changes.

---

### 2. Stage Your Files

Add all files to the staging area:

```bash
git add .
```

Or add specific files:

```bash
git add filename.html
git add style.css
```

---

### 3. Commit Your Changes

Create a commit with a descriptive message:

```bash
git commit -m "Initial commit: Add project files"
```

**Note:** Always write clear commit messages describing what you changed.

---

### 4. Create a Repository on GitHub

1. Go to https://github.com
2. Click the **"+"** icon in the top right corner
3. Select **"New repository"**
4. Enter a repository name (e.g., "my-project")
5. **Important:** Do NOT check "Initialize with README" if you already have files
6. Click **"Create repository"**
7. Copy the repository URL (looks like: `https://github.com/username/repository-name.git`)

---

### 5. Connect Your Local Repository to GitHub

Add the GitHub repository as a remote:

```bash
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git
```

Replace `YOUR-USERNAME` and `YOUR-REPO-NAME` with your actual GitHub username and repository name.

---

### 6. Push Your Files to GitHub

#### If this is a brand new GitHub repository (empty):

```bash
git push -u origin main
```

#### If the GitHub repository already has files (README, license, etc.):

First, pull and merge the remote files:

```bash
git pull origin main --allow-unrelated-histories
```

If an editor opens asking for a merge message:
- **In vim:** Press `ESC`, then type `:wq` and press `ENTER`
- **In nano:** Press `CTRL+X`, then `Y`, then `ENTER`

Then commit the merge:

```bash
git commit -m "Merge remote repository with local files"
```

Finally, push your files:

```bash
git push -u origin main
```

---

## Making Future Changes

After the initial setup, whenever you make changes to your files:

### 1. Check what files changed:
```bash
git status
```

### 2. Stage the changes:
```bash
git add .
```
Or stage specific files:
```bash
git add filename.html
```

### 3. Commit the changes:
```bash
git commit -m "Describe what you changed"
```

### 4. Push to GitHub:
```bash
git push
```

---

## Useful Git Commands

| Command | Description |
|---------|-------------|
| `git status` | Check which files have changed |
| `git log` | View commit history |
| `git diff` | See what changed in files |
| `git remote -v` | View connected remote repositories |
| `git branch` | List all branches |
| `git pull` | Download changes from GitHub |
| `git clone <url>` | Download a repository from GitHub |

---

## Common Issues & Solutions

### Issue 1: "Updates were rejected"
**Solution:** Pull the latest changes first:
```bash
git pull origin main
```
Then push again:
```bash
git push
```

### Issue 2: "Permission denied"
**Solution:** You may need to authenticate. GitHub now requires personal access tokens instead of passwords.

1. Go to GitHub Settings → Developer settings → Personal access tokens
2. Generate a new token with "repo" permissions
3. Use the token as your password when pushing

### Issue 3: "Not a git repository"
**Solution:** Make sure you're in the correct folder and have run `git init`

### Issue 4: Merge conflicts
**Solution:** 
1. Open the conflicting files
2. Look for conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`)
3. Edit the file to keep the version you want
4. Remove the conflict markers
5. Stage and commit the resolved files

---

## Best Practices

1. **Commit often** with clear messages
2. **Pull before you push** to avoid conflicts
3. **Don't commit sensitive information** (passwords, API keys)
4. **Use .gitignore** to exclude unnecessary files (node_modules, .DS_Store, etc.)
5. **Write descriptive commit messages** (e.g., "Add contact form validation" instead of "Update")

---

## Quick Reference: Complete Workflow

```bash
# First time setup
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/username/repo.git
git push -u origin main

# Making changes later
git add .
git commit -m "Description of changes"
git push
```

---

## Need Help?

- Git documentation: https://git-scm.com/doc
- GitHub guides: https://guides.github.com
- Git cheat sheet: https://education.github.com/git-cheat-sheet-education.pdf

---

**Remember:** Practice makes perfect! The more you use Git and GitHub, the more comfortable you'll become with these commands.
