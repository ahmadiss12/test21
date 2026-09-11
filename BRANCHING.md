# Branching workflow

Never commit to `main`. Every feature/fix gets its own branch.

## Steps

1. Get the latest main:
   git checkout main
   git pull origin main

2. Create the feature branch:
   git checkout -b feature/short-description

3. Do the work, then stage + commit:
   git add .
   git commit -m "Add short description"

4. Push it (first push needs -u to link the remote branch):
   git push -u origin feature/short-description

5. Open a Pull Request on GitHub: feature/short-description -> main.
   Get it reviewed, then merge.

6. Clean up after merge:
   git checkout main
   git pull origin main
   git branch -d feature/short-description

## Useful commands

- git branch                 list local branches
- git branch -a              list local + remote branches
- git branch --show-current  which branch am I on
- git switch main            move back to main
- git log --oneline -5       recent commits

## Naming

feature/...  new functionality
fix/...      bug fixes
chore/...    tooling, deps, docs

## Where to see branches on GitHub

- Repo page -> branch dropdown (top-left, above the file list)
- Repo page -> "Branches" link / https://github.com/ahmadiss12/test21/branches
- Pushed branches also show a yellow "Compare & pull request" banner
- Pull Requests tab shows open PRs for those branches
