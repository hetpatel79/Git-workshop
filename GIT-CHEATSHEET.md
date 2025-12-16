# Git Cheatsheet

Quick reference of common git commands and short examples.

Setup
- git init: initialize a repository
- git clone <url>: clone remote repo

Basic workflow
- git status: show current state
- git add <file|.>: stage changes
- git commit -m "message": record staged snapshot
- git log --oneline --graph --decorate: commit history

Branching
- git branch <name>: create branch
- git checkout <name>: switch branch
- git switch -c <name>: create and switch (modern)
- git merge <branch>: merge branch into current
- git rebase <branch>: reapply commits onto branch (advanced)

Remotes & Collaboration
- git remote -v: list remotes
- git remote add origin <url>: add remote
- git push -u origin <branch>: push branch and set upstream
- git pull: fetch and merge remote changes
- git fetch: fetch remote refs (no merge)

Undoing changes
- git restore <file>: discard unstaged changes
- git restore --staged <file>: unstage file
- git reset --soft <commit>: move HEAD (keep changes staged)
- git reset --hard <commit>: move HEAD and discard working changes (dangerous)
- git revert <commit>: create a new commit that undoes a commit

Stashing
- git stash: save working changes
- git stash pop: reapply and drop stash
- git stash list: show stashes

Viewing differences
- git diff: unstaged changes
- git diff --staged: staged vs last commit

Helpful tips
- Use descriptive commit messages: "feat: add login form"
- Use branches for features and PRs for review
- Run `git status` often to avoid surprises
