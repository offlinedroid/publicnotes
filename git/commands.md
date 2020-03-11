- [Global Configuration](#Global-Configuration)
- [Merge Local With Remote Existing Repo](#Merge-Local-With-Remote-Existing-Repo)
- [Merge Remote changes to local branch](#Merge-Remote-changes-to-local-branch)
- [Get branch from Remote and optionally merge changes from master](#Get-branch-from-Remote-and-optionally-merge-changes-from-master)

# Global Configuration
- git config [--global] user.name "\<name>"
- git config [--global] user.email \<email>

# Merge Local With Remote Existing Repo
 1. cd \<folder> 
 2. git init
 3. Add gitignore if needed
 3. git add .
 5. git commit -m "commit message"
 6. git remote add origin https|ssh:path/to/the/repository.git
 7. git pull origin master
 8. If you get `fatal: refusing to merge unrelated histories` after 7, do `git pull origin master --allow-unrelated-histories`

# Merge Remote changes to local branch
1. git checkout master
2. git pull origin master
3. git checkout <branch name>
4. git merge master

# Get branch from Remote and optionally merge changes from master

1. git clone <url>
2. git checkout master (optional)
3. git pull origin master (optional)
4. git branch -a (display all including remote branch. Or -r to display remote 5. branch)
6. git branch <branchName> origin/<branchname>
7. git checkout <branchname>
8. git merge master
 
# Undo changes to a specific file
git checkout -- \<filename>
(use quotes if file name has spaces)
