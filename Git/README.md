# Git commands

## Ask for help

1 - `git --help`;   

2 - `git (command) --help`;   

## Most used

Require no comments...   

1 - `git init (directory)` or `git init`;    

2 - `git clone (repository url)`;   

3 - `git status`;   

4 - `git add (directory)` or `git add .`;   

5 - `git commit -m "(message)"`;   

6 - `git pull (origin) (branch)`;   

7 - `git push (origin) (branch)`;   

8 - `git remote add (origin)`;   

9 - `git remote remove (origin)`;   

10 - `git branch`;   

11 - `git checkout -b (branch)`;   

12 - `git checkout (branch)`;   

13 - `git merge (branch)`;   

14 - `git branch -d (branch)`;   

15 - `git branch -M (branch)`;   


## Good to know

### 1. `git revert (commit)`
Creates a new commit that undoes the changes of the specified commit.

#### Example:
`git revert a1b2c3d`

### 2. `git reset (option) (commit)`
Moves the current branch pointer (HEAD) and adjusts the working directory or staging area based on the option.

Options:   
- `--soft`: Moves the HEAD to the specified commit, keeping all changes staged.
- `--mixed`: Moves the HEAD and unstages changes, but keeps them in the working directory.
- `--hard`: Moves the HEAD, discarding both staged and working directory changes.

#### Moving the HEAD to a specific commit:
To move the HEAD back to a specific commit, use `git reset` followed by the desired commit hash.

#### Example:   
`git reset --hard a1b2c3d`   
`git reset --soft HEAD~1` 


### 3. `git fetch (remote) (branch)`
Downloads commits from the remote repository but doesn't merge them.

#### Example:
`git fetch origin main`

### 4.`git push (remote) (branch) -f`
Forces the push of local changes to the specified remote repository and branch, overwriting any conflicts.

#### Example:
`git push origin main -f`

### 5. `git diff HEAD`
Shows the differences between the current working directory and the latest commit (HEAD).

#### Example:
`git diff HEAD`


### 6. `git log --(limit)`
Displays the commit history with a specified limit on the number of commits shown.

#### Example:
`git log --max-count=5`


### 7. `git log --grep=(pattern)`
Filters the commit history to show only commits that contain a specified keyword or pattern in their commit message.

#### Example:
`git log --grep="fix"`   

### 8. `git commit --amend`
Modifies the most recent commit. This command allows you to change the commit message or include new changes to the last commit without creating a new commit.   
**OBS**: Not recommended if the commit is already in the remote repository.

#### Example:
To modify the commit message:
`git commit --amend -m "New commit message"`




