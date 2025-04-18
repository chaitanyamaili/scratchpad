# 🧠 Git Cheat Sheet

A quick reference guide to the most common Git commands.

---

## 🔧 Setup

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
git config --global core.editor "vim"  # Or your preferred editor



⸻

📁 Creating a Repo

git init                     # Start a new Git repo
git clone <url>              # Clone an existing repo



⸻

📄 Basic Workflow

git status                   # Check status of your files
git add <file>               # Stage file(s)
git add .                    # Stage all changes
git commit -m "Message"      # Commit staged changes



⸻

🔄 Branching

git branch                   # List branches
git branch <name>            # Create new branch
git checkout <name>          # Switch to branch
git checkout -b <name>       # Create & switch to new branch
git merge <branch>           # Merge branch into current
git branch -d <name>         # Delete branch



⸻

🔍 Viewing History

git log                      # Full commit history
git log --oneline            # Condensed history
git log --graph --oneline    # Visual branch structure
git show <commit>            # Details of a commit



⸻

🚀 Remote Repos

git remote -v                # List remotes
git remote add origin <url> # Add a remote repo
git push origin main         # Push to remote
git pull                     # Pull from remote



⸻

🧹 Undo Changes

git restore <file>           # Discard local changes
git reset <file>             # Unstage a file
git reset --soft HEAD~1      # Undo last commit (keep changes)
git reset --hard HEAD~1      # Undo last commit (discard changes)



⸻

🧪 Stashing

git stash                    # Save changes temporarily
git stash pop                # Reapply saved changes
git stash list               # View stashes



⸻

📦 Tagging

git tag                      # List tags
git tag <name>               # Create a tag
git tag -a <name> -m "msg"   # Annotated tag
git push origin <tagname>    # Push a tag



⸻

⚡ Shortcuts

git commit -am "msg"         # Add and commit in one step
git checkout -               # Switch to previous branch
git diff                     # See unstaged changes
git diff --staged            # See staged changes



⸻

🧠 Pro Tips
	•	Use .gitignore to exclude files from tracking.
	•	Use git reflog to recover lost commits.
	•	Use git bisect to find bugs by binary search.
