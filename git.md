# **Git commands**

## Workflow (The 3 states)

### .git directory (repository):

is where the metadata and object database for your project is stored.

### Working directory:

is a Copy of a repository version. The files are obtained from a compressed database of the .git directory

### Staging area:

is a file that stores information about what will be on your next commit, sometimes called an index.

<img style="width: 20rem" src="https://raw.githubusercontent.com/MigueAJM/shell-command/master/image/git/states.png?token=GHSAT0AAAAAABV6EFAN7KFIP4VIOZEECVSUYWB33VQ" alt="3 states">

## List

### config name:
#### Un repositorio
`> git config user.name "Username"`
#### Todos los repositorios
`> git config --global user.name "Username"`

### config email:
### Un repositorio
`> git config --global user.email example@example.mx`
#### Todos los repositorios
`> git config --global user.email example@example.mx`

### list configuration:

`> git config --list`

## Note: Ignore files (create .gitignore file)

### Init repo:

`> git init`

### clone repo in local:

`> git clone /path/to/repository `

### clone repo in server remote:

`> git clone git clone username@host:/path/to/repository `

### list branches:

`> git branch`

### create branch:

`> git branch new_branch_name`

### remove branch:

`> git branch -d new_branch_name`

### remove remote branch:

`> git push origin --delete new_branch_name`

### status:

`> git status`

### checkout (navigation between branches or commit):

`> git checkout hash_commit` or `> git checkout branch_name`

### add files to "Stage":

`> git add file.ext` or `> git add .`

### remove files to "Stage":

`> git reset file.ext` or `> git reset .`

### commit:

`> git commit -m "Reference message for the commit"`

### Modify message from last commit (no push)

`> git commit --amend -m "New message"`

### Add more changes to the last commit (no push)

`> git commit --amend -m "Reference message for the commit"`

## Note: The `--amend` parameter only works with the latest commit.

### Delete last commit (unpublished), keeping the changes:

`> git reset --soft HEAD~1`

### Delete last commit (unpublished), without keeping the changes:

`> git reset --hard HEAD~1`

### Uncommit (published): This will create a new commit that will undo all changes from that particular commit.

`> git revert hash_commit`

### log:

`> git log`
#### Parameters:
- `--graph`
- `--stat`
- `--pretty=oneline`
- `--pretty=format:"%h - %an, %ar : %s"`

## Remote

### show remote:

`> git remote`

### show remote and url:

`> git remote -v`

### add remote:

`> git remote add http https://github.com/MigueAJM/shell-command.git` or `> git remote add ssh git@github.com:MigueAJM/shell-command.git`

### rename remote:

`> git remote rename http origin`

### set-url remote:

`> git remote set-url remote_name url`

### delete remote:

`> git remote rm origin`

### fetch(download commits, files and references from a remote repository):

`> git fetch remote_name branch_name`

### merge positioned in master or main(branch merge):

- `> git checkout master`
- `> git merge new_feature`
- `> git branch -d new_feature`

### pull(download commits, files, references from a remote repository and update your local repository(fetch and merge):

`> git pull remote_name branch_name`

### push:

`> git push remote_name branch_name` example `> git push origin branch`

## Alias

`> git config --global alias.co checkout`

> [@MigueAJM](https://twitter.com/migueajm)
