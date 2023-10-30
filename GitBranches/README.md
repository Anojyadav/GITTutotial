### Git Branch

The git branch command is used in Git to list, create, and manage branches in your Git repository. When you run git branch without any additional options, it will display a list of all the branches in your repository. 

To create a new branch 

```
git branch <branch_name>
```

the above command will only create a new branch from the branch you are currently at (for example if at main, then this would create a branch from main branch)

To switch to the new branch created, you use checkout or switch

```
git checkout <branch_name>
```

After switching the branch the HEAD will point to the commit made on this branch, if no commits has been made after checkout, the HEAD will point to the last commit on the master branch before creating the branch. The commits will we carry forwarded to this branch as well. 

If a new commit has been made on this branch, then HEAD will point to the latest commit on this branch only not the master. 

To check use 
```
git log 
```

To check the HEAD to the particular commit id or hash 

```
git rev-parse HEAD
```

Alternatively, you can create and switch to a new branch in a single step using the -b option

```
git checkout -b <new_branch_name>
```

To check to which branch you are currently on, 
```
git branch
```

the *followed with branch name is the current branch 


