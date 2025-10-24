# Git Workflow Documentation

This document outlines the complete Git workflow for the DevOps Git Task project.

## 🎯 Project Overview

**Objective**: Demonstrate Git best practices and DevOps workflows
**Tools**: Git, GitHub
**Focus**: Version control, branching, collaboration

## 📋 Complete Task Checklist

### ✅ Required Deliverables

1. **Repository Setup**
   - [x] Initialize Git repository
   - [x] Create comprehensive .gitignore
   - [x] Set up proper project structure

2. **Branching Strategy**
   - [x] Create `main` branch (production)
   - [x] Create `dev` branch (development)
   - [x] Create `feature-*` branches (features)

3. **Commit Standards**
   - [x] Use conventional commit messages
   - [x] Create meaningful commit history
   - [x] Follow commit message format

4. **Version Control**
   - [x] Create Git tags (v1.0)
   - [x] Document versioning strategy
   - [x] Push tags to remote

5. **Documentation**
   - [x] Comprehensive README.md
   - [x] Workflow documentation
   - [x] Git commands reference

6. **Pull Request Workflow**
   - [ ] Create PR: feature → dev
   - [ ] Create PR: dev → main
   - [ ] Demonstrate code review process

## 🚀 Step-by-Step Implementation

### Step 1: Initialize Repository

```bash
# Navigate to project directory
cd devops-git-task

# Initialize Git repository
git init

# Set default branch to main
git branch -M main

# Add all files
git add .

# Create initial commit
git commit -m "chore: initial commit with README and .gitignore"

# Add remote repository (replace with your GitHub repo)
git remote add origin https://github.com/yourusername/devops-git-task.git

# Push to main branch
git push -u origin main
```

### Step 2: Create Development Branch

```bash
# Create and switch to dev branch
git checkout -b dev

# Push dev branch to remote
git push -u origin dev
```

### Step 3: Create Feature Branch

```bash
# Create feature branch from dev
git checkout -b feature-login dev

# Make changes to login.md
echo "Development notes added." >> README.md

# Stage and commit changes
git add .
git commit -m "feat: add development notes"

# Push feature branch
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

### Step 5: Pull Request Workflow

1. **Create Pull Request on GitHub:**
   - Go to your repository on GitHub
   - Click "Compare & pull request" for `feature-login` branch
   - Set base branch to `dev`
   - Add description: "Add login feature scaffold"
   - Create pull request

2. **Merge feature to dev:**
   - Review the pull request
   - Merge `feature-login` → `dev`
   - Delete feature branch after merge

3. **Create Pull Request dev → main:**
   - Create new pull request: `dev` → `main`
   - Add description: "Release v1.0 - Development integration"
   - Merge after review

## 📝 Commit Message Examples

```bash
# Feature commits
git commit -m "feat(login): add user authentication system"
git commit -m "feat(api): implement REST endpoints"

# Bug fixes
git commit -m "fix(login): resolve authentication timeout"
git commit -m "fix(ui): correct button alignment"

# Documentation
git commit -m "docs(readme): update installation guide"
git commit -m "docs(api): add endpoint documentation"

# Maintenance
git commit -m "chore(deps): update dependencies"
git commit -m "chore(config): update environment variables"

# Style changes
git commit -m "style(login): format code according to standards"
git commit -m "style(ui): improve button styling"

# Refactoring
git commit -m "refactor(auth): simplify authentication logic"
git commit -m "refactor(api): restructure endpoint handlers"

# Tests
git commit -m "test(login): add unit tests for authentication"
git commit -m "test(api): add integration tests"
```

## 🌿 Branch Naming Conventions

- **`main`** - Production-ready code
- **`dev`** - Development integration
- **`feature/feature-name`** - New features
- **`hotfix/issue-description`** - Critical bug fixes
- **`release/version-number`** - Release preparation

## 🏷️ Tagging Strategy

```bash
# Semantic versioning
git tag -a v1.0.0 -m "v1.0.0 - Initial release"
git tag -a v1.1.0 -m "v1.1.0 - Feature release"
git tag -a v1.1.1 -m "v1.1.1 - Bug fix release"

# Push all tags
git push origin --tags

# Push specific tag
git push origin v1.0.0
```

## 🔄 Daily Workflow

### Starting Work
```bash
# Pull latest changes
git checkout main
git pull origin main

# Create feature branch
git checkout -b feature/new-feature
```

### During Development
```bash
# Stage changes
git add .

# Commit with conventional message
git commit -m "feat(component): add new functionality"

# Push to remote
git push origin feature/new-feature
```

### Finishing Work
```bash
# Create pull request on GitHub
# After PR approval and merge:
git checkout main
git pull origin main
git branch -d feature/new-feature
```

## 📊 Git Status and History

```bash
# Check repository status
git status

# View commit history
git log --oneline

# View branch structure
git log --graph --oneline --all

# Check remote branches
git branch -r

# View tags
git tag -l
```

## 🚨 Common Issues and Solutions

### Issue: Merge Conflicts
```bash
# Pull latest changes
git pull origin main

# Resolve conflicts in files
# Stage resolved files
git add .

# Complete merge
git commit -m "resolve: merge conflicts in feature branch"
```

### Issue: Accidentally committed to main
```bash
# Create new branch from current state
git checkout -b feature/correct-branch

# Reset main to previous commit
git checkout main
git reset --hard HEAD~1

# Push corrected main
git push origin main --force-with-lease
```

### Issue: Need to update feature branch
```bash
# Switch to feature branch
git checkout feature/your-branch

# Merge latest dev changes
git merge dev

# Resolve conflicts if any
# Push updated branch
git push origin feature/your-branch
```

## 📈 Best Practices Summary

1. **Always create feature branches from `dev`**
2. **Use conventional commit messages**
3. **Keep commits small and focused**
4. **Write descriptive commit messages**
5. **Review code before merging**
6. **Use pull requests for all merges**
7. **Tag releases with semantic versioning**
8. **Keep `main` branch always deployable**
9. **Delete merged feature branches**
10. **Document all workflows**

## 🎓 Learning Outcomes

After completing this workflow, you will understand:

- ✅ Git repository management
- ✅ Branching strategies
- ✅ Commit message conventions
- ✅ Pull request workflows
- ✅ Version control with tags
- ✅ Team collaboration practices
- ✅ Code review processes
- ✅ Documentation standards

---

**Next Steps**: Implement this workflow in your repository and create the required pull requests to demonstrate your understanding of Git best practices.
