# Basic Version Control

## What is Version Control?

Version control is a system that tracks and records changes to files over time. It lets you revisit earlier versions, see who changed what, and collaborate with others without overwriting each other's work. Think of it like an "undo history" for your entire project but one that never disappears and that multiple people can use at once.

## Difference Between Git and GitHub

**Git** is a version control tool that runs locally on your computer. It handles all the tracking, branching, and merging of your code.

**GitHub** is a cloud-based platform that hosts Git repositories online, making it easy to share code, collaborate with others, and manage projects through features like pull requests, issues, and code reviews.

In short: Git is the engine, GitHub is the garage where you park and share your work.

## GitHub Alternatives

1. **GitLab** — A DevOps platform that offers built-in CI/CD, issue tracking, and self-hosting options.
2. **Bitbucket** — An Atlassian product that integrates tightly with Jira and supports both Git and Mercurial repositories.
3. **Gitea** — A lightweight, self-hosted Git service that is open-source and easy to set up.

## Difference Between `git fetch` and `git pull`

`git fetch` downloads new changes from the remote repository but does not merge them into your local branch. It simply updates your local copy of the remote's state so you can review the changes first.

`git pull` does both in one step: it fetches the changes and immediately merges them into your current branch.

Use `fetch` when you want to check what's new before integrating. Use `pull` when you're ready to update right away.

## Git Rebase

Rebase moves your branch's commits on top of another branch's latest commits, as if you started your work from that newer point. It creates a cleaner, linear project history without extra merge commits.

**Command:**

```bash
git rebase main
```

Runn this while on your feature branch. It replays your commits on top of the latest `main` branch.

## Git Cherry-Pick

Cherry-pick lets you grab a specific commit from another branch and apply it to your current branch — without merging everything else from that branch. It's useful when you only need one particular change.

**Command:**

```bash
git cherry-pick <commit-hash>
```

Replace `<commit-hash>` with the actual hash of the commit you want to apply (e.g., `git cherry-pick a1b2c3d`).
