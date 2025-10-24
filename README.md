# DevOps Git Task - Version Control Best Practices

This project demonstrates professional Git and GitHub workflows for DevOps practices.

## 🎯 Objective
Learn and demonstrate version control workflows using Git best practices including branching, committing, merging, pull requests, tags, and documentation.

## 📁 Project Structure
```
devops-git-task/
├── README.md          # Project documentation
├── .gitignore         # Git ignore rules
├── login.md          # Sample feature file
└── index.html        # Sample application file
```

## 🌿 Branching Strategy

### Main Branches
- **`main`** - Production-ready code
- **`dev`** - Development integration branch

### Feature Branches
- **`feature-*`** - Individual feature development
- **`hotfix-*`** - Critical bug fixes
- **`release-*`** - Release preparation

## 🚀 Git Workflow

### 1. Initial Setup
```bash
# Initialize repository
git init

# Set default branch to main
git branch -M main

# Add remote repository
git remote add origin <your-github-repo-url>

# Initial commit
git add .
git commit -m "chore: initial commit with README and .gitignore"
git push -u origin main
```

### 2. Development Workflow
```bash
# Create development branch
git checkout -b dev
git push -u origin dev

# Create feature branch from dev
git checkout -b feature-login dev
# Make changes...
git add .
git commit -m "feat(login): add login feature scaffold"
git push -u origin feature-login
```

### 3. Pull Request Workflow
1. Create Pull Request: `feature-login` → `dev`
2. Review and merge via GitHub
3. Create Pull Request: `dev` → `main`
4. Review and merge via GitHub

### 4. Versioning
```bash
# Create version tag
git tag -a v1.0 -m "v1.0 - initial stable release"
git push origin v1.0
```

## 📝 Commit Message Convention

We follow [Conventional Commits](https://www.conventionalcommits.org/):

- `feat:` - New features
- `fix:` - Bug fixes
- `docs:` - Documentation changes
- `style:` - Code style changes
- `refactor:` - Code refactoring
- `test:` - Adding tests
- `chore:` - Maintenance tasks

### Examples:
```bash
git commit -m "feat(login): add user authentication"
git commit -m "fix(api): resolve timeout issue"
git commit -m "docs(readme): update installation guide"
```

## 🔧 Common Git Commands

### Branch Management
```bash
# List branches
git branch -a

# Create and switch to new branch
git checkout -b feature-name

# Switch branches
git checkout branch-name

# Delete branch
git branch -d branch-name
```

### Commit Management
```bash
# Stage changes
git add .
git add filename

# Commit with message
git commit -m "commit message"

# Amend last commit
git commit --amend -m "new message"
```

### Remote Operations
```bash
# Push to remote
git push origin branch-name

# Pull latest changes
git pull origin branch-name

# Fetch without merge
git fetch origin
```

### Tagging
```bash
# Create annotated tag
git tag -a v1.0 -m "Version 1.0"

# Push tags
git push origin v1.0

# List tags
git tag -l
```

## 📋 Task Checklist

- [x] Initialize Git repository
- [x] Create comprehensive .gitignore
- [x] Set up branching strategy (main, dev, feature)
- [x] Create proper commit messages
- [x] Add Git tags for versioning
- [x] Document workflow in README
- [x] Demonstrate pull request workflow

## 🎓 Learning Outcomes

After completing this task, you will understand:

1. **Version Control**: How to use Git for tracking changes
2. **Branching**: Creating and managing different branches
3. **Collaboration**: Using pull requests for code review
4. **Documentation**: Writing clear project documentation
5. **Best Practices**: Following industry standards for Git workflows

## 🔗 Resources

- [Git Documentation](https://git-scm.com/doc)
- [GitHub Flow](https://guides.github.com/introduction/flow/)
- [Conventional Commits](https://www.conventionalcommits.org/)
- [Git Best Practices](https://github.com/git/git/blob/master/Documentation/SubmittingPatches)

## 📞 Submission

Complete your DevOps Git task and submit at: [https://forms.gle/GmLzk2PcfwCQDMHm8](https://forms.gle/GmLzk2PcfwCQDMHm8)

---

**Note**: This project demonstrates Git best practices for DevOps workflows. The focus is on version control, not application development.
