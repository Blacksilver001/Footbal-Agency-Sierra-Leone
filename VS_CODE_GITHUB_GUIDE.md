# VS Code Git & GitHub Guide: Push Files to GitHub from VS Code

This guide shows you how to use VS Code's built-in Git features to push your files to GitHub.

## Method 1: Using VS Code's Built-in Git Integration

### Step 1: Open Your Project in VS Code
1. Open VS Code
2. Go to **File** → **Open Folder**
3. Select your project folder (e.g., "Web Development Assigment")
4. Your project files will appear in the Explorer panel

### Step 2: Initialize Git Repository (First Time Only)
1. Look at the bottom left corner of VS Code - you'll see a **Source Control** icon (looks like a branch)
2. Click the Source Control icon
3. Click **"Initialize Repository"** button
4. Your folder is now a Git repository

### Step 3: Stage Your Files
1. In the Source Control panel, you'll see all your files listed under "Changes"
2. Click the **"+"** icon next to each file you want to add, OR
3. Click the **"+"** icon at the top to stage all files at once

### Step 4: Commit Your Changes
1. Enter a commit message in the text box at the top (e.g., "Initial commit: Add project files")
2. Click the **checkmark icon** (✓) to commit

### Step 5: Create GitHub Repository
1. Go to https://github.com in your browser
2. Click the **"+"** icon → **"New repository"**
3. Enter repository name (e.g., "web-development-project")
4. **Important:** Leave "Initialize with README" unchecked
5. Click **"Create repository"**
6. Copy the repository URL

### Step 6: Connect to GitHub Repository
1. In VS Code, click the **"..."** menu in Source Control panel
2. Select **"Remote"** → **"Add Remote"**
3. Enter:
   - **Remote name:** `origin`
   - **Remote URL:** Paste your GitHub repository URL
4. Click **"Add Remote"**

### Step 7: Push to GitHub
1. Click the **"..."** menu in Source Control panel
2. Select **"Push"**
3. If prompted, sign in to GitHub
4. Your files will be uploaded to GitHub!

---

## Method 2: Using VS Code GitHub Extension (Recommended)

### Install GitHub Extension
1. Click the Extensions icon in the left sidebar (puzzle piece)
2. Search for "GitHub"
3. Install the official "GitHub" extension by GitHub
4. Also install "GitHub Pull Requests and Issues" extension

### Using the Extension
1. After installing, you'll see a GitHub icon in the left sidebar
2. Click it to sign in to GitHub
3. Once signed in, you can:
   - Create new repositories directly from VS Code
   - Push to existing repositories
   - View pull requests and issues

### Create Repository from VS Code
1. Click the GitHub icon in sidebar
2. Click **"+"** → **"Create Repository"**
3. Enter repository name and description
4. Choose if it should be public or private
5. Click **"Create"**
6. VS Code will automatically connect and push your files!

---

## Method 3: Using Command Palette

VS Code has keyboard shortcuts for Git operations:

### Quick Git Commands via Command Palette
1. Press `Ctrl+Shift+P` (Windows/Linux) or `Cmd+Shift+P` (Mac)
2. Type "Git:" to see all Git commands

Common commands:
- **"Git: Initialize Repository"** - Start Git in current folder
- **"Git: Add All"** - Stage all files
- **"Git: Commit"** - Commit staged files
- **"Git: Push"** - Push to remote repository

---

## Choosing Which Repository to Push To

### If You Have Multiple Repositories:

1. **Check Current Remote:**
   - In Source Control panel, click **"..."** → **"Remote"** → **"Show Remote"**
   - This shows which GitHub repository you're connected to

2. **Change Remote Repository:**
   - Click **"..."** → **"Remote"** → **"Remove Remote"** (to remove current)
   - Then **"Remote"** → **"Add Remote"** (to add new one)
   - Enter the new repository URL

3. **Push to Different Branch:**
   - Click the branch name at bottom left
   - Select or create a new branch
   - Push that branch to GitHub

---

## VS Code Git Interface Overview

### Source Control Panel Icons:
- **✓** (checkmark) - Commit staged files
- **+** - Stage files (add to commit)
- **-** - Unstage files
- **↻** - Discard changes
- **...** - More options menu

### Status Indicators:
- **U** - Untracked (new file)
- **M** - Modified
- **A** - Added (staged)
- **D** - Deleted

---

## Troubleshooting

### "No repository found"
- Make sure you're in the correct folder
- Check if there's a `.git` folder in your project directory

### "Authentication failed"
- Sign out and sign back in to GitHub
- Use a Personal Access Token instead of password
- Go to GitHub Settings → Developer settings → Personal access tokens

### "Push rejected"
- Pull latest changes first: **"..."** → **"Pull"**
- Then try pushing again

### "Repository already exists"
- Choose a different repository name
- Or push to a different branch

---

## Quick Reference: VS Code Git Workflow

1. **Open project** → Source Control icon
2. **Initialize** → Click "Initialize Repository"
3. **Stage files** → Click "+" next to files or "Stage All Changes"
4. **Commit** → Enter message → Click ✓
5. **Add remote** → "..." → Remote → Add Remote → Enter GitHub URL
6. **Push** → "..." → Push

---

## Tips for VS Code Git

- **Auto-save:** Enable auto-save to avoid losing changes
- **GitLens extension:** Install for advanced Git features and history
- **Sync:** Use "Sync" button to pull and push in one click
- **Branches:** Create feature branches for different work
- **Compare:** Right-click files to compare versions

---

## Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `Ctrl+Shift+G` | Open Source Control |
| `Ctrl+Enter` | Commit with current message |
| `Ctrl+Shift+P` | Command Palette |
| `Ctrl+K Ctrl+S` | Keyboard Shortcuts |

---

**Remember:** VS Code's Git integration makes version control much easier than command line! Start with Method 1, then try the GitHub extension for even more features.
