# Git Cheat Sheet

A curated list of essential Git commands for version control, history visualization, and collaboration.

## 🌲 Tree Visualization (History)
The most common way to see a "tree-like" structure in the terminal:

```bash
git log --graph --oneline --all --decorate
```
**Tip:** Create an alias so you don't have to type it every time:
```bash
git config --global alias.tree "log --graph --oneline --all --decorate"
# Now you can just run:
git tree
```

---

## 🏗️ Branching & Switching
| Command | Description |
| :--- | :--- |
| `git branch` | List all local branches |
| `git branch <name>` | Create a new branch |
| `git checkout <name>` | Switch to a branch (Older way) |
| `git switch <name>` | Switch to a branch (Modern way) |
| `git switch -c <name>` | Create and switch to a new branch |
| `git branch -d <name>` | Delete a branch (Safe) |
| `git branch -D <name>` | Force delete a branch |

---

## 🔗 Merging & Rebase
| Command | Description |
| :--- | :--- |
| `git merge <branch>` | Merge `<branch>` into your current branch |
| `git merge --abort` | Stop a merge if conflicts occur |
| `git rebase <branch>` | Reapply commits on top of another branch (Cleaner history) |
| `git cherry-pick <commit>` | Apply a specific commit from another branch |

---

## 📜 Logging & Inspection
| Command | Description |
| :--- | :--- |
| `git log` | Show commit history |
| `git log -n <N>` | Show last `N` commits |
| `git log --oneline` | Condensed history |
| `git show <commit>` | Show changes in a specific commit |
| `git diff` | Show unstaged changes |
| `git diff --staged` | Show changes ready for commit |
| `git status` | Show current branch and file states |

---

## 💾 Staging & Committing
| Command | Description |
| :--- | :--- |
| `git add <file>` | Stage a file |
| `git add .` | Stage all changes |
| `git commit -m "msg"` | Commit with a message |
| `git commit --amend` | Edit the last commit message or add more files |

---

## 🌍 Remotes & Collaboration
| Command | Description |
| :--- | :--- |
| `git fetch` | Download objects/refs from another repo |
| `git pull` | Fetch and merge (equivalent to `fetch` + `merge`) |
| `git push <remote> <branch>` | Upload local commits to remote |
| `git clone <url>` | Create a local copy of a remote repo |
| `git remote -v` | List all tracked remote repositories |

---

## ⏪ Undoing Changes
| Command | Description |
| :--- | :--- |
| `git restore <file>` | Discard changes in a file (unstaged) |
| `git reset --soft HEAD~1` | Undo last commit, keep changes staged |
| `git reset --hard HEAD~1` | Undo last commit and destroy changes |
| `git revert <commit>` | Create a new commit that undoes a previous one |
