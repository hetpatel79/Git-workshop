# Git Exercises (Beginner-friendly)

Each exercise includes steps and expected results. Run commands in a terminal inside the repository.

Exercise 1 — Initialize and commit
1. Create a new folder `exercise-1` and a file `hello.txt` with some text.
2. Run: `git init`, `git add .`, `git commit -m "chore: add hello.txt"`
Expected: A `.git` folder appears and `git log --oneline` shows your commit.

Exercise 2 — Clone and inspect
1. Clone any public repo: `git clone https://github.com/git/git.git` (or a small public repo)
2. Run: `cd git` and `git log --oneline | head -n 5`
Expected: Repository copies and you can see recent commits.

Exercise 3 — Branch and merge
1. On your repo, create branch: `git switch -c feature-x`
2. Edit or add `feature.txt`, `git add`, `git commit -m "feat: feature-x"`
3. Switch back: `git switch main` (or `master`), then `git merge feature-x`
Expected: Merge completes; `git log --oneline --graph` shows branch merged.

Exercise 4 — Fix a mistake with revert
1. Make a commit that introduces a small change.
2. Use `git revert <commit>` to undo it (creates a new commit).
Expected: History still shows the original commit and a new commit that undoes it.

Exercise 5 — Use stash when switching context
1. Make an unfinished change in a file but do not stage it.
2. Run `git stash` then `git switch other-branch`.
3. Return and run `git stash pop`.
Expected: Your local changes are saved and reapplied after popping.

Exercise 6 — Collaborate: remote push and pull
1. Add a remote: `git remote add origin <your-fork-url>`
2. Push a branch: `git push -u origin feature-x`
3. On another machine or clone, run `git pull origin feature-x`
Expected: Remote contains your branch; other clone receives changes.

Hints & checks
- Use `git status` and `git log` frequently.
- If unsure, create a disposable test repo to try commands safely.
