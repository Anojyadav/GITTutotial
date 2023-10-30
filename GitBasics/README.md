### Start with Git

## git status
The git status command is used in Git to display information about the current state of your working directory and the status of your Git repository

```
git status
```

Running the above command gives information on Modified, untracked, and staged files

## git add
The git add command is used in Git to stage changes for the next commit

1. To stage specific file
```
git add filename
```
2. To stage all changes in the working directory for the next commit
```
git add .
```
3. Stage changes in a specific directory and its subdirectories
```
git add directory/
```
4. Stage all changes, including untracked files, for the next commit
```
git add -A
```
5. Stage all modification and deletion in the currently tracked files, excluding untracked files for the next commit 
```
git add -u
```
6. Stage changes interactively (useful for reviewing and selecting specific changes)
```
git add -i
```

### git commit 

The git commit command is used in Git to create a new commit that captures the current state of your project. Commits are snapshots of your code at a specific point in time, and they are a fundamental part of Git's version control system.

```
git commit
```

Running the above command will commit the staged by git add, also will open the default text editor(vim) to write the commit messages. 

To change the default text editor globally  use (In my case vscode)
```
git config --global core.editor "code --wait"
```
This would open the vscode whenever git commit command is executed, the terminal will wait until the file opened in the vscode is saved and closed, once the message is edited, save and close the file. 

Opening a text editor for everytime you commit can be bit annoying sometimes, You can also commit with a message with option '-m' with brief description of your changes for the particular commit. 

```
git commit -m "Your commit message here"
```

It is good to have atomic commit practice, which means one commit message for particular unit implementation or a particular bug fix, it is easy to track. 

The git log command is used to view the commit history of a Git repository. 

```
git log
```
Note: Press q to exit

-> To see a compact one-line view of the commit history, use:
```
git log --oneline
```

If you have made some typos in your commit message or you forgot to include add a file use amending commits

In case you forgot to add a file,
```
git add "forgotten file name"
```

then
```
git commit --amend
```

this will open the text editior (default), to change the editor to vscode see the steps above

make changes in the file opened in the text editor save and close.

### git push

The git push command is used in Git to send your local branch's commits to a remote repository.

```
git push origin branch _name
```
