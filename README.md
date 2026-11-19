# azure-sre-automation

Git Practice (Day 1)

A small practice repository for the everyday Git and GitHub workflow: clone, branch, commit, push, pull request, merge and sync. It is part of a hands-on learning plan covering Linux, Bash, Python and Git for cloud and SRE automation.

Goals
Repeat the full branch-to-merge workflow until it feels natural.
Practise good habits from the start: small commits, clear messages, and never committing secrets.
Keep a record of what I practised and what I learned.
Environment
Item	Value
OS	Ubuntu on WSL2 (Windows)
Editor	VS Code with the WSL extension
Git remote	GitHub, over SSH
Tools	Git, Python 3, Azure CLI
Workflow practised
Create the repo on GitHub with a README.
Clone it over SSH and check that the working tree is clean.
bash
git clone git@github.com:<username>/<repo-name>.git
cd <repo-name>
git status
Add a .gitignore before adding anything else, so secrets and temporary files are never tracked.
Create a branch for one small change. Never work directly on main.
bash
git switch -c <branch-name>
Make the change, then review it before staging.
bash
git status
git diff
Stage and commit with a clear message.
bash
git add <files>
git commit -m "Short, clear description of the change"
git log --oneline
Push the branch and link it to the remote.
bash
git push -u origin <branch-name>
Open a pull request on GitHub, review the "Files changed" tab as if someone else wrote it, then merge.
Sync and tidy up.
bash
git switch main
git pull
git branch -d <branch-name>
Repository structure
text
.
├── README.md
├── .gitignore
├── notes/        # short notes on what I practised
└── scripts/      # small practice scripts
Quick reference
Task	Command
See what changed	git status, git diff
Stage files	git add <files>
Commit	git commit -m "message"
View history	git log --oneline
New branch	git switch -c <name>
Switch branch	git switch <name>
Push a new branch	git push -u origin <name>
Update main	git switch main && git pull
Delete a merged branch	git branch -d <name>
Safety checklist
Run git status before git add . and make sure only the files I intend to commit are listed.
Never commit passwords, tokens, .env files, or private SSH keys (anything like id_ed25519 without .pub).
Keep .gitignore in place from the first commit.
Only the public key (.pub) is ever shared with GitHub.
Practice log

Tick each item once done.

[ ] Created a new repo and cloned it over SSH
[ ] Added a .gitignore before the first real commit
[ ] Created a branch, committed, and pushed it
[ ] Opened, reviewed and merged a pull request
[ ] Switched to main, pulled, and deleted the merged branch
[ ] Repeated the loop a second time with a different change
[ ] Edited a file on GitHub, then pulled it down locally
[ ] Created and resolved a merge conflict on purpose
[ ] Undid an uncommitted change and an unpushed commit
What I learned

Add a few notes here in my own words, for example:

What staging, committing, pushing and merging each do.
One mistake I made and how I fixed it.
One thing I want to practise again.
