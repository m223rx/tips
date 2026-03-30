Git is a distributed version‑control system for tracking changes in source code (and other files). Below are the most frequently used commands to get you started:

| Task | Command | Example |
|------|---------|---------|
| Initialize a new repo | `git init` | `git init my‑project` |
| Clone an existing repo | `git clone <url>` | `git clone https://github.com/user/repo.git` |
| Check status | `git status` | `git status` |
| Stage changes | `git add <file|.>` | `git add .` |
| Commit staged changes | `git commit -m "Message"` | `git commit -m "Add login feature"` |
| View commit history | `git log` | `git log --oneline` |
| Create a branch | `git branch <name>` | `git branch feature-x` |
| Switch branches | `git checkout <name>` | `git checkout feature-x` |
| Create & switch in one step | `git checkout -b <name>` | `git checkout -b feature-x` |
| Merge a branch | `git merge <branch>` | `git merge feature-x` |
| Pull remote changes | `git pull` | `git pull origin main` |
| Push local commits | `git push` | `git push origin main` |
| Resolve conflicts (edit files, then) | `git add <resolved>` | `git add conflicted_file` |
| Discard local changes | `git checkout -- <file>` | `git checkout -- config.yml` |
| Reset to a previous commit | `git reset --hard <commit>` | `git reset --hard HEAD~1` |

**Quick cheat sheet**

```bash
# Start a repo
git init
git remote add origin <url>

# Common workflow
git add .
git commit -m "Your message"
git pull   # integrate remote changes
git push   # share your commits
```

Feel free to ask if you need details on a specific command or a more advanced Git topic!