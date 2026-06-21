# Version Control System - Forking Workflow Simulation

Welcome to the **Forking Workflow** simulation repository! This repository serves as the **upstream repository** for learning and practicing the Git forking workflow.

## 🎯 Learning Objectives

By the end of this exercise, you will understand how to:

- Fork a repository on GitHub
- Clone your forked repository
- Configure upstream remote
- Create feature branches
- Make changes and commit them
- Push changes to your fork
- Create Pull Requests
- Sync your fork with upstream changes

## 📋 Prerequisites

- Git installed on your machine
- GitHub account
- Basic understanding of Git commands

## 🔄 Forking Workflow Overview

The forking workflow is ideal for open source projects and distributed teams. Here's how it works:

```
┌─────────────────┐    Fork     ┌─────────────────┐
│   Upstream      │ ────────►   │   Your Fork     │
│   Repository    │             │   (Origin)      │
│   (This Repo)   │             │                 │
└─────────────────┘             └─────────────────┘
         │                               │
         │                               │ Clone
         │ Pull Request                  ▼
         │                       ┌─────────────────┐
         └─────────────────────  │   Local Copy    │
                                 │   (Your Machine)│
                                 └─────────────────┘
```

## 🚀 Getting Started

### Step 1: Fork This Repository

1. Click the **"Fork"** button at the top right of this repository page
2. Select your GitHub account as the destination
3. Wait for GitHub to create your fork

### Step 2: Clone Your Fork

```bash
# Replace YOUR_USERNAME with your actual GitHub username
git clone https://github.com/YOUR_USERNAME/version-control-system-hari-senin.git

# Navigate to the project directory
cd version-control-system-hari-senin
```

### Step 3: Configure Upstream Remote

```bash
# Add the original repository as upstream
git remote add upstream https://github.com/madewantara/version-control-system-hari-senin.git

# Verify remotes
git remote -v
```

You should see:

```
origin    https://github.com/YOUR_USERNAME/version-control-system-hari-senin.git (fetch)
origin    https://github.com/YOUR_USERNAME/version-control-system-hari-senin.git (push)
upstream  https://github.com/madewantara/version-control-system-hari-senin.git (fetch)
upstream  https://github.com/madewantara/version-control-system-hari-senin.git (push)
```

## 🛠 Your Assignment

### Task: Add Yourself to the Contributors List

1. **Create a new branch** for your changes:

   ```bash
   git checkout -b add-your-name
   ```

2. **Edit the `contributors.yaml` file** and add your information:

   ```yaml
   # Add your entry following the existing format
   - name: "Your Full Name"
     github: "your-github-username"
     role: "Student"
     batch: "18" # Your batch number
     skills: ["skill1", "skill2", "skill3"]
     favorite_language: "JavaScript" # or your preferred language
     joined_date: "2025-12-20" # Today's date
   ```

3. **Commit your changes**:

   ```bash
   git add contributors.yaml
   git commit -m "Add [Your Name] to contributors list"
   ```

4. **Push to your fork**:

   ```bash
   git push origin add-your-name
   ```

5. **Create a Pull Request**:
   - Go to your fork on GitHub
   - Click "Compare & pull request"
   - Write a descriptive title: "Add [Your Name] to contributors"
   - Add a description of your changes
   - Click "Create pull request"

## 🔄 Keeping Your Fork Updated

### Sync with Upstream

```bash
# Fetch latest changes from upstream
git fetch upstream

# Switch to main branch
git checkout main

# Merge upstream changes
git merge upstream/main

# Push updated main to your fork
git push origin main
```

## 📝 Best Practices

1. **Always create feature branches** - Never work directly on `main`
2. **Sync frequently** - Keep your fork updated with upstream changes
3. **Write clear commit messages** - Describe what and why, not just what
4. **Small, focused PRs** - One feature or fix per pull request
5. **Test before submitting** - Make sure your changes work

## 🔧 Common Git Commands Reference

```bash
# Check current status
git status

# See commit history
git log --oneline

# Check which branch you're on
git branch

# Switch branches
git checkout branch-name

# Create and switch to new branch
git checkout -b new-branch-name

# Add files to staging
git add filename
git add .  # Add all files

# Commit changes
git commit -m "Your commit message"

# Push to your fork
git push origin branch-name

# Pull latest changes
git pull origin main
```

## 🆘 Troubleshooting

### Merge Conflicts

If you encounter merge conflicts:

1. Open the conflicted files
2. Look for conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`)
3. Manually resolve conflicts
4. Remove conflict markers
5. Stage and commit resolved files

### Reset Local Changes

```bash
# Discard uncommitted changes
git checkout -- filename

# Reset to last commit
git reset --hard HEAD

# Reset to upstream main
git reset --hard upstream/main
```

## 📚 Additional Resources

- [Git Documentation](https://git-scm.com/doc)
- [GitHub Forking Guide](https://docs.github.com/en/get-started/quickstart/fork-a-repo)
- [Atlassian Git Tutorials](https://www.atlassian.com/git/tutorials)

## 🎉 Success Criteria

You've successfully completed this exercise when you:

- [x] Forked this repository
- [x] Cloned your fork locally
- [x] Configured upstream remote
- [x] Created a feature branch
- [x] Added yourself to contributors.yaml
- [x] Committed and pushed your changes
- [x] Created a Pull Request
- [x] Successfully merged your PR (instructor will merge)

---

**Happy Coding! 🚀**

_This repository is maintained for educational purposes as part of the Full Stack Developer Course - Batch 18_
