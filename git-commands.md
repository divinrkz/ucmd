# GIT GUIDE
## SETUP
### Configuring user information used across all local repositories.

- Sets a name that is identifiable for credit when review version history.
```bash
git config --global user.name "[firstname lastname]"
```
- Sets an email address that will be associated with each history markery.
```bash
git config --global user.email "[valid-email]"
```
- Sets automatic command line coloring for Git for easy reviewing.
 ```bash
 git config --global color.ui auto
 ```
<br>

## INITIALISE
### Configuring user information, initializing and cloning repositories.
- Initialize an existing directory as a Git repository.
```bash
git init
```
- Retrieve an entire repository from a hosted location via URL.
 ```bash
git clone [url]
```
<br>


## STAGE & SNAPSHOT
### Working with snapshots and the Git staging area.
- Shows modified files in working directory, staged for your next commit.
```bash
git status
```
- Adds a file as it looks now to your next commit (stage).
```bash
git add [file]
```
- Unstages a file while retaining the changes in working directory.
```bash
git reset [file]
```
- Differences of what is changed but not staged.
```bash
git diff
```
- Differences of what is staged but not yet commited.
```bash
git diff --staged
```
- Commits your staged content as a new commit snapshot.
```bash
git commit -m “[descriptive message]”
```

<br>

## BRANCH & MERGE
### Isolating work in branches,changin context, and integration changes.
- Lists your branches. a * will appear next to the currently active branch.
```bash
git branch
```
- Creates a new branch at the current commit.
```bash
git branch [branch-name]
```
- Switches to another branch and check it out into your working directory.
```bash
git checkout
```
- Merges the specified branch’s history into the current one.
```bash
git merge [branch]
```
- Shows all commits in the current branch’s history.
```bash
git log
```

<br>

## INSPECT & COMPARE
### Examining logs, diffs and object information.
- Shows the commit history for the currently active branch.
```bash
git log
```
- Shows the commits on branchA that are not on branchB.
```bash
git log branchB..branchA
```
- Shows the commits that changed file, even across renames.
```bash
git log --follow [file]
```
- Shows the difference of what is in branchA that is not in branchB.
```bash
git diff branchB...branchA
```
- Shows any object in Git in human-readable format.
```bash
git show [SHA]
```

<br>

## TRACKING PATH CHANGES
### Versioning file removes and path changes.
- Deletes the file from project and stage the removal for commit.
```bash
git rm [file]
```
- Changes an existing file path and stage the move.
```bash
git mv [existing-path] [new-path]
```
- Shows all commit logs with indication of any paths that moved.
```bash
git log --stat -M
```

<br>

## IGNORING PATTERNS
### Preventing unintentional staging or commiting of files.
- Save a file with desired paterns as .gitignore with either direct string
matches or wildcard globs.
```bash
logs/
*.notes
pattern*/

```
- System wide ignore patern for all local repositories.
```bash
git config --global core.excludesfile [file]
```
- Shows all commit logs with indication of any paths that moved.
```bash
git log --stat -M
```

<br>

## SHARE & UPDATE
### Retrieving updates from another repository and updating local repos.
- Adds a git URL as an alias.
```bash
git remote add [alias] [url]
```
- Fetchs down all the branches from that Git remote.
```bash
git fetch [alias]
```
- merge a remote branch into your current branch to bring it up to date.
```bash
git merge [alias]/[branch]
```
- Transmit local branch commits to the remote repository branch.
```bash
git push [alias] [branch]
```
- Fetchs and merges any commits from the tracking remote branch.
```bash
git pull
```

<br>

## REWRITE HISTORY
### Rewriting branches, updating commits and clearing history.
- Applies any commits of current branch ahead of specified one.
```bash
git rebase [branch]
```
- Clears staging area, Rewrites working tree from specified commit.
```bash
git reset --hard [commit]
```

<br>

## TEMPORARY COMMITS
### Temporarily store modified, tracked files in order to change branches.
- Saves modified and staged changes.
```bash
git stash
```
- Lists stack-order of stashed file changes.
```bash
git stash list
```
- Writes working from top of stash stack.
```bash
git stash pop
```
- Discards the changes from top of stash stack.
```bash
git stash drop
```










