# How to Contribute with Pull Requests

This guide will walk you through the basics of creating a pull request for this project.

## What is a Pull Request?

A pull request (PR) is how you propose changes to the project. It allows others to review your work before it's merged into the main codebase.

## Step-by-Step Guide

### 1. Clone the Repository

If you haven't already, clone the repository to your local machine:

```bash
# Clone the repository
git clone <repository-url>
cd PAM-bmad
```

### 2. Create a New Branch

**Never work directly on the `main` branch!** Always create a new branch for your changes:

```bash
# Make sure you are on the main branch and have the latest changes
git checkout main
git pull

# Create and switch to a new branch
git checkout -b fix/typo-in-readme
# or
git checkout -b feature/add-new-agent
```

**Branch naming tips:**

- `fix/description` - for bug fixes
- `feature/description` - for new features
- `docs/description` - for documentation changes

### 3. Make Your Changes

- Edit the files you want to change.
- Keep your changes small and focused on a single task.

### 4. Commit Your Changes

Commit your changes with a clear and descriptive message.

```bash
# Add your changes to be staged for commit
git add .

# Commit with a clear message
git commit -m "Fix: Correct typo in README.md"
# or for a feature
git commit -m "Feat: Add new agent for XYZ"
```

**Good commit messages:**

- "Fix: Correct typo in installation instructions"
- "Feat: Add example for new agent usage"
- "Docs: Update broken link"

### 5. Push Your Branch

Push your new branch to the central repository:

```bash
# Push your branch
git push origin fix/typo-in-readme
```

### 6. Create the Pull Request

1.  Go to the repository in your web browser.
2.  GitHub will usually show a prompt to create a pull request for your recently pushed branch. Click the "Compare & pull request" button.
3.  If you don't see the prompt, go to the "Pull requests" tab and click "New pull request".
4.  Set the base branch to `main` and the compare branch to your new branch (e.g., `fix/typo-in-readme`).
5.  Write a clear title and description for your pull request. Explain *what* you changed and *why*.
6.  Click "Create pull request".

### 7. Request a Review

Once your pull request is created, please request a review from one of the project maintainers. They will review your changes and may request modifications before merging.

## What Makes a Good Pull Request?

✅ **Good PRs:**

-   Change one thing at a time.
-   Have clear, descriptive titles.
-   Explain what and why in the description.
-   Include only the files that need to change.

❌ **Avoid:**

-   Changing formatting of entire files.
-   Multiple unrelated changes in one PR.
-   Changes without explanation.

---

**Remember**: If you have questions about the process, please reach out to one of the project maintainers.