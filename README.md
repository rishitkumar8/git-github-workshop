# Git & GitHub Workshop

## Intro
> _ADD LATER_

## Installing Git

To install Git based on your OS:

- **Windows**: [https://git-scm.com/downloads/win](https://git-scm.com/downloads/win)
- **Ubuntu**:  
  ```bash
  sudo apt-get install git
   ```

- **Fedora**:
  For Fedora 21 and below:

  ```bash
  sudo yum install git
  ```

- For Fedora 22 and above:

  ```bash
  sudo dnf install git
  ```
* **macOS**:

  ```bash
  brew install git
  ```

---

## Setting up Git

After installing Git, configure your user information and default branch:

```bash
# Check Git version
git --version

# Set your Git username
git config --global user.name "Your Name"

# Set your Git email
git config --global user.email "your.email@example.com"

# Set 'main' as the default branch for new repos
git config --global init.defaultBranch main
```
---

## Git Commands

```bash
# Initializing a repository
git init

# Checking the current state of the repo
git status

# Adding a single file to the staging area
git add <file-name>

# Adding all files to the staging area
git add .

# Committing staged changes with a message
git commit -m "your commit message"

# Viewing commit history
git log

# Viewing commit history in short form
git log --oneline

# Checking the differences between working directory and last commit
git diff

# Restoring a modified file to the last committed version
git restore <file-name>

# Removing a file from the staging area (unstage)
git restore --staged <file-name>
````

---

## GitHub Integration

```bash
# Connecting local repo to GitHub
git remote add origin https://github.com/your-username/your-repo.git

# Renaming the default branch to main (if needed)
git branch -M main

# Pushing commits to GitHub
git push origin main

# Cloning a repository from GitHub
git clone https://github.com/some-user/some-repo.git

# Pulling latest changes from the main branch
git pull origin main
```

---

## Branching

```bash
# List all branches
git branch

# Create a new branch
git branch new-branch

# Switch to a branch (existing)
git switch branch-name

# Create and switch to a new branch (shortcut)
git switch -c new-branch

# OR using older syntax
git checkout -b new-branch

# Rename a branch (while on it)
git branch -m new-name

# Delete a local branch (only if merged)
git branch -d branch-name
```

---

## Best Practices for Commit Messages

| Prefix   | Purpose                                                      |
|----------|--------------------------------------------------------------|
| `fix:`   | Bug fixes or small corrections in code                      |
| `feat:`  | New features or enhancements                                |
| `ref:`   | Code refactoring (changing structure without changing behavior) |
| `chore:` | Maintenance tasks, code cleanup, or setup improvements      |
| `add:`   | Adding new technologies, libraries, or configurations       |
| `break:` | Breaking changes, usually in global config or API           |
| `doc:`   | Documentation updates                                       |

### Examples:
```bash
git commit -m "fix: fixed a piece of code crashing on load"
git commit -m "feat: added user profile feature"
git commit -m "ref: simplified logic in signup controller"
git commit -m "chore: cleaned up unused imports"
git commit -m "add: introduced ESLint and Prettier configs"
git commit -m "break: updated global config to new API structure"
git commit -m "doc: added setup instructions to README"
```
---

## Good Things to Mention in a Pull Request (PR)

When opening a Pull Request on GitHub, it’s important to clearly explain what your code does. This helps maintainers review your work faster and improves your chances of getting it merged.

### Include the Following in Your PR:

1. **Description**  
   Briefly describe what changes you made and why.  
2. **Screenshot** (if applicable)  
   Include before/after screenshots or a small GIF if your change affects the UI.
3. **Issue it Resolves**  
   Link the issue your PR fixes (if any). Use the format:  
```
Fixes #12 (#12 means issue number 12)
Closes #5
Resolves #8
```
4. **Features to Add (Optional)**  
If your PR lays the groundwork for upcoming features, mention them here.

6. **Tag Maintainers (Optional)**  
If you want feedback or a quicker review, you can politely tag the project maintainers using `@username`.


---

Bonus Tips:

- Be polite and clear in your PR description.
- Use bullet points or markdown formatting for readability.
- If your PR is still a work in progress, add `[WIP]` to the title or use GitHub’s draft PR feature.

---
