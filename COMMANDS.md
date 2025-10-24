
### Step 1: Initialize Repository and Initial Commit

```bash
# Navigate to project directory
cd "C:\Users\vinay yalla\Desktop\taska\task3\devops-git-task"

# Initialize Git repository
git init

# Set default branch to main
git branch -M main

# Add all files to staging
git add .

# Create initial commit
git commit -m "chore: initial commit with README and .gitignore"

# Add remote repository (REPLACE WITH YOUR GITHUB REPO URL)
git remote add origin https://github.com/yourusername/devops-git-task.git

# Push to main branch
git push -u origin main
```

### Step 2: Create Development Branch

```bash
# Create and switch to dev branch
git checkout -b dev

# Add development content to README
echo "Development notes added." >> README.md

# Stage and commit changes
git add README.md
git commit -m "feat: add development notes"

# Push dev branch to remote
git push -u origin dev
```

### Step 3: Create Feature Branch

```bash
# Create feature branch from dev
git checkout -b feature-login dev

# Add content to login.md
echo "This file describes the login feature implementation steps." > login.md

# Stage and commit changes
git add login.md
git commit -m "feat(login): add login feature scaffold"

# Push feature branch to remote
git push -u origin feature-login
```

### Step 4: Create Version Tag

```bash
# Switch to main branch
git checkout main

# Create annotated tag
git tag -a v1.0 -m "v1.0 - initial stable release"

# Push tag to remote
git push origin v1.0
```

### Step 5: Verify Repository Status

```bash
# Check all branches
git branch -a

# Check tags
git tag -l

# View commit history
git log --oneline --graph --all

# Check remote configuration
git remote -v
```

## 📋 Manual Steps (GitHub Web Interface)

### Create Pull Requests

1. **Feature → Dev Pull Request:**
   - Go to your GitHub repository
   - Click "Compare & pull request" for `feature-login` branch
   - Set base branch to `dev`
   - Title: "feat(login): add login feature scaffold"
   - Description: "Add login feature implementation steps"
   - Create pull request
   - Merge the pull request

2. **Dev → Main Pull Request:**
   - Create new pull request: `dev` → `main`
   - Title: "Release v1.0 - Development integration"
   - Description: "Merge development changes to main for v1.0 release"
   - Create pull request
   - Merge the pull request

## 🔧 Additional Useful Commands

### Branch Management
```bash
# List all branches
git branch -a

# Switch between branches
git checkout main
git checkout dev
git checkout feature-login

# Delete local branch (after merge)
git branch -d feature-login

# Delete remote branch
git push origin --delete feature-login
```

### Commit Management
```bash
# Check status
git status

# View changes
git diff

# Stage specific files
git add README.md
git add .gitignore

# Unstage files
git reset HEAD filename

# Amend last commit
git commit --amend -m "new commit message"
```

### Remote Operations
```bash
# Fetch latest changes
git fetch origin

# Pull latest changes
git pull origin main

# Push specific branch
git push origin dev

# Push all branches
git push --all origin

# Push all tags
git push --tags origin
```

### History and Logs
```bash
# View commit history
git log --oneline

# View detailed history
git log --graph --oneline --all

# View specific branch history
git log dev --oneline

# View file history
git log --follow README.md
```

## 🎯 Final Verification Checklist

After running all commands, verify:

- [ ] Repository has `main`, `dev`, and `feature-login` branches
- [ ] All branches are pushed to remote
- [ ] Tag `v1.0` is created and pushed
- [ ] Pull requests are created and merged
- [ ] README.md contains comprehensive documentation
- [ ] .gitignore file is properly configured
- [ ] Commit messages follow conventional format

## 🚨 Troubleshooting

### If you get authentication errors:
```bash
# Configure Git credentials
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

### If remote URL is wrong:
```bash
# Check current remote
git remote -v

# Update remote URL
git remote set-url origin https://github.com/yallavinay/task3.git
```

### If you need to start over:
```bash
# Remove Git history
rm -rf .git

# Start fresh
git init
# ... repeat the workflow
```

---
