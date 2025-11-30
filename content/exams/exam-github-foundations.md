# GitHub Foundations

> These are **NOT real questions** from the exam but quite close enough to what you can get to help you to prepare it and obtain the certification

## Skills measured

- [Introduction to Git and GitHub](#introduction-to-git-and-github) (15% of the exam)
- [Working with GitHub Repositories](#working-with-github-repositories) (15% of the exam)
- [Collaboration Features](#collaboration-features) (20% of the exam)
- [Modern Development](#modern-development) (15% of the exam)
- [Project Management](#project-management) (15% of the exam)
- [Privacy, Security, and Administration](#privacy-security-and-administration) (10% of the exam)
- [Benefits of the GitHub Community](#benefits-of-the-github-community) (10% of the exam)

## Introduction to Git and GitHub

### What is Git?

<details><summary>show</summary>
<p>

Git is a distributed version control system (DVCS) that tracks changes in source code during software development. It allows multiple developers to work on a project simultaneously without overwriting each other's changes.

</p>
</details>

### What is the difference between Git and GitHub?

<details><summary>show</summary>
<p>

- **Git** is a version control system that runs locally on your computer
- **GitHub** is a cloud-based hosting service that lets you manage Git repositories

GitHub provides additional features like pull requests, issues, project boards, and GitHub Actions on top of Git's version control capabilities.

</p>
</details>

### What does the command `git clone` do?

<details><summary>show</summary>
<p>

`git clone` creates a local copy of a remote repository on your computer. It downloads the entire repository history and files.

```bash
git clone https://github.com/owner/repository.git
```

</p>
</details>

### What is the difference between `git fetch` and `git pull`?

<details><summary>show</summary>
<p>

- **git fetch**: Downloads changes from the remote repository but doesn't merge them into your working branch
- **git pull**: Downloads changes from the remote repository AND merges them into your current branch

`git pull` is essentially `git fetch` + `git merge`.

</p>
</details>

### What is a Git commit?

<details><summary>show</summary>
<p>

A commit is a snapshot of your repository at a specific point in time. Each commit has:
- A unique SHA hash identifier
- Author information
- Timestamp
- Commit message describing the changes
- Pointer to parent commit(s)

</p>
</details>

### What is the purpose of a .gitignore file?

<details><summary>show</summary>
<p>

A `.gitignore` file specifies intentionally untracked files that Git should ignore. Common use cases include:
- Build output directories
- Dependency folders (node_modules, vendor)
- IDE configuration files
- Environment files with secrets
- Log files

</p>
</details>

### What is a Git branch?

<details><summary>show</summary>
<p>

A branch is a lightweight movable pointer to a commit. It allows developers to work on features or fixes in isolation without affecting the main codebase. The default branch is typically called `main` or `master`.

</p>
</details>

### What is the difference between `git merge` and `git rebase`?

<details><summary>show</summary>
<p>

- **git merge**: Combines two branches by creating a new merge commit that has two parent commits
- **git rebase**: Moves or replays commits from one branch onto another, creating a linear history

Merge preserves history as it happened, while rebase creates a cleaner, linear history.

</p>
</details>

## Working with GitHub Repositories

### What are the three visibility options for GitHub repositories?

<details><summary>show</summary>
<p>

- **Public**: Visible to everyone on the internet
- **Private**: Only visible to the owner and collaborators they explicitly share access with
- **Internal**: Only visible to members of the organization (Enterprise only)

</p>
</details>

### What should a good README.md file contain?

<details><summary>show</summary>
<p>

A good README should include:
- Project title and description
- Installation instructions
- Usage examples
- Configuration options
- Contributing guidelines
- License information
- Contact information or links to documentation

</p>
</details>

### What is a repository template?

<details><summary>show</summary>
<p>

A repository template allows you to create a starter repository that others can use as a base for their own projects. When you create a new repository from a template, it:
- Copies all files and folders
- Does NOT copy the commit history
- Creates a fresh repository with a single initial commit

</p>
</details>

### What is the GitHub Archive Program?

<details><summary>show</summary>
<p>

The GitHub Archive Program preserves open source software for future generations. It includes:
- Arctic Code Vault: Stores code in a decommissioned coal mine in the Arctic
- Multiple partner archives around the world
- Automatic archiving of public repositories

</p>
</details>

### What is the purpose of the CODEOWNERS file?

<details><summary>show</summary>
<p>

The CODEOWNERS file defines individuals or teams that are responsible for code in a repository. When someone opens a pull request that modifies code owned by these code owners, they are automatically requested as reviewers.

```
# Example CODEOWNERS file
*.js @frontend-team
/docs/ @docs-team
```

</p>
</details>

### What are GitHub repository topics?

<details><summary>show</summary>
<p>

Topics are labels that help classify and discover repositories. They appear at the top of your repository page and help others find projects related to a specific subject. Examples: javascript, react, machine-learning, tutorial.

</p>
</details>

## Collaboration Features

### What is a pull request?

<details><summary>show</summary>
<p>

A pull request (PR) is a proposal to merge changes from one branch into another. It allows:
- Code review before merging
- Discussion about the proposed changes
- Automated checks and tests
- Collaborative feedback on the code

</p>
</details>

### What is the difference between a fork and a clone?

<details><summary>show</summary>
<p>

- **Fork**: Creates a copy of a repository under your own GitHub account (server-side copy)
- **Clone**: Downloads a repository to your local machine (local copy)

Forks are commonly used for contributing to open source projects where you don't have write access to the original repository.

</p>
</details>

### How do you link a pull request to an issue?

<details><summary>show</summary>
<p>

You can link a pull request to an issue using keywords in the PR description or commit message:
- closes #123
- fixes #123
- resolves #123

When the PR is merged, the linked issue will automatically be closed.

</p>
</details>

### What are GitHub Discussions?

<details><summary>show</summary>
<p>

GitHub Discussions is a collaborative communication forum for a repository community. Unlike issues, discussions are meant for:
- Q&A with the community
- Open-ended conversations
- Announcements
- Polls
- Ideas and brainstorming

</p>
</details>

### What is a draft pull request?

<details><summary>show</summary>
<p>

A draft pull request indicates that the PR is not ready for review. It:
- Cannot be merged until marked as "Ready for review"
- Helps communicate work in progress
- Allows early feedback without formal review
- Disables required reviewers notifications

</p>
</details>

### What are assignees and reviewers in a pull request?

<details><summary>show</summary>
<p>

- **Assignees**: People responsible for working on the pull request (typically the author or someone taking ownership)
- **Reviewers**: People requested to review and approve the code changes

A PR can have multiple assignees and reviewers.

</p>
</details>

### What is a merge conflict and how can you resolve it?

<details><summary>show</summary>
<p>

A merge conflict occurs when Git cannot automatically merge changes because the same lines were modified in different ways on different branches. To resolve:

1. Identify conflicting files
2. Open the files and look for conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`)
3. Manually edit the file to combine changes
4. Remove conflict markers
5. Stage and commit the resolved file

</p>
</details>

## Modern Development

### What is GitHub Actions?

<details><summary>show</summary>
<p>

GitHub Actions is a CI/CD platform that allows you to automate your build, test, and deployment pipeline. You can create workflows that:
- Build and test your code on every push
- Deploy to production
- Run on a schedule
- Respond to various GitHub events

</p>
</details>

### What is GitHub Codespaces?

<details><summary>show</summary>
<p>

GitHub Codespaces provides cloud-hosted development environments that can be launched directly from a GitHub repository. Benefits include:
- Pre-configured development environment
- Access from any device with a browser
- Consistent environment for all team members
- Integration with VS Code

</p>
</details>

### What is GitHub Copilot?

<details><summary>show</summary>
<p>

GitHub Copilot is an AI pair programmer that offers code suggestions as you type. It:
- Uses AI to suggest code completions
- Can generate entire functions based on comments
- Works in multiple programming languages
- Integrates with popular IDEs

</p>
</details>

### What is the basic Markdown syntax for creating headings, lists, and links?

<details><summary>show</summary>
<p>

```markdown
# Heading 1
## Heading 2
### Heading 3

- Bullet point
- Another bullet point

1. Numbered item
2. Another numbered item

[Link text](https://example.com)

![Image alt text](image-url.png)

**Bold text**
*Italic text*
```

</p>
</details>

### What is GitHub Mobile used for?

<details><summary>show</summary>
<p>

GitHub Mobile allows you to:
- Review and merge pull requests
- Respond to issues and discussions
- Receive push notifications
- Browse code and repositories
- Manage notifications
- Review CI/CD status

</p>
</details>

## Project Management

### What is the difference between GitHub Projects (classic) and GitHub Projects (new)?

<details><summary>show</summary>
<p>

- **Classic Projects**: Board-based project management with columns and cards, tied to a single repository
- **New Projects**: Flexible project management with tables, boards, and roadmaps; can span multiple repositories and has built-in fields, custom fields, and automation

</p>
</details>

### What are GitHub milestones?

<details><summary>show</summary>
<p>

Milestones are a way to track progress on groups of issues or pull requests in a repository. They:
- Group related issues together
- Show completion percentage
- Have optional due dates
- Help plan releases or sprints

</p>
</details>

### What are GitHub labels used for?

<details><summary>show</summary>
<p>

Labels are tags that can be applied to issues and pull requests to:
- Categorize work (bug, feature, documentation)
- Indicate priority (high, medium, low)
- Show status (needs review, help wanted)
- Filter and search issues/PRs efficiently

</p>
</details>

### How do you create a task list in GitHub?

<details><summary>show</summary>
<p>

Task lists are created using Markdown syntax in issues or pull request descriptions:

```markdown
- [x] Completed task
- [ ] Incomplete task
- [ ] Another task to do
```

Task lists show a progress bar and can be checked off directly in the GitHub UI.

</p>
</details>

### What are GitHub Insights?

<details><summary>show</summary>
<p>

GitHub Insights provide analytics about your repository:
- **Contributors**: Who has contributed and how much
- **Traffic**: Views and clones of your repository
- **Commits**: Commit activity over time
- **Code frequency**: Additions and deletions over time
- **Dependency graph**: Repository dependencies
- **Network**: Fork and branch visualization

</p>
</details>

## Privacy, Security, and Administration

### What is two-factor authentication (2FA)?

<details><summary>show</summary>
<p>

Two-factor authentication adds an extra layer of security by requiring:
1. Something you know (password)
2. Something you have (phone/security key)

GitHub supports:
- TOTP apps (Google Authenticator, Authy)
- SMS messages
- Security keys (hardware tokens)
- GitHub Mobile app

</p>
</details>

### What is a Personal Access Token (PAT)?

<details><summary>show</summary>
<p>

A Personal Access Token is an alternative to using passwords for authentication with GitHub. PATs:
- Can have specific scopes/permissions
- Can be set to expire
- Should be used instead of passwords for Git operations
- Can be revoked at any time

Types:
- Fine-grained PATs (repository-specific access)
- Classic PATs (broader scope)

</p>
</details>

### What is the purpose of SSH keys in GitHub?

<details><summary>show</summary>
<p>

SSH keys provide secure authentication without typing a password. They consist of:
- **Private key**: Stored on your computer (never shared)
- **Public key**: Added to your GitHub account

SSH keys are commonly used for:
- Git push/pull operations
- Connecting to remote servers
- Signing commits

</p>
</details>

### What are branch protection rules?

<details><summary>show</summary>
<p>

Branch protection rules enforce certain workflows before code can be pushed to a branch. Common rules include:
- Require pull request reviews
- Require status checks to pass
- Require signed commits
- Require linear history
- Include administrators
- Restrict who can push

</p>
</details>

### What is the difference between organization members and outside collaborators?

<details><summary>show</summary>
<p>

- **Organization members**: People who belong to the organization and can access multiple repositories based on team membership
- **Outside collaborators**: External users who have access to specific repositories only, not organization-wide access

</p>
</details>

## Benefits of the GitHub Community

### What is GitHub Sponsors?

<details><summary>show</summary>
<p>

GitHub Sponsors allows the community to financially support developers and organizations maintaining open source projects. Sponsors can:
- Make one-time or recurring payments
- Get recognition and special perks
- Support maintainers directly on GitHub

</p>
</details>

### What is the GitHub Stars program?

<details><summary>show</summary>
<p>

GitHub Stars are people who inspire the developer community through their leadership, contributions, and dedication. They:
- Share knowledge with the community
- Advocate for open source
- Receive special recognition from GitHub
- Get access to exclusive events and resources

</p>
</details>

### What are community health files?

<details><summary>show</summary>
<p>

Community health files help maintain healthy open source projects:
- **CODE_OF_CONDUCT.md**: Expected behavior for contributors
- **CONTRIBUTING.md**: Guidelines for contributing
- **SECURITY.md**: Security policy and vulnerability reporting
- **SUPPORT.md**: Where to get help
- **ISSUE_TEMPLATE**: Templates for creating issues
- **PULL_REQUEST_TEMPLATE**: Template for creating PRs

These files can be stored in a `.github` repository to apply to all repositories in an organization.

</p>
</details>

### What is GitHub Explore?

<details><summary>show</summary>
<p>

GitHub Explore helps discover interesting projects and repositories:
- Trending repositories
- Topics and collections
- Featured projects
- Personalized recommendations based on your interests

</p>
</details>

### How can you contribute to an open source project you don't have write access to?

<details><summary>show</summary>
<p>

The typical workflow is:

1. **Fork** the repository to your account
2. **Clone** your fork locally
3. Create a **branch** for your changes
4. Make your changes and **commit**
5. **Push** to your fork
6. Create a **pull request** to the original repository
7. Respond to review feedback
8. Once approved, the maintainer merges your PR

</p>
</details>

### What is a good first issue?

<details><summary>show</summary>
<p>

A "good first issue" is a label used by maintainers to identify issues that are suitable for newcomers to a project. These issues typically:
- Have clear descriptions
- Require limited knowledge of the codebase
- Are of limited scope
- May include hints or guidance for solving them

</p>
</details>