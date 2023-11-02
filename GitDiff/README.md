### Git Diff

git diff is a command used in git to compare differences between various states of your codebase, typically between commits or between your working directory and the most recent commit.

git diff lists all the chnages in our working directory that are not staged for the next commit

```
git diff
```

If you want to list all the changes stagged / unstagged 
```
git diff HEAD 
```

To view only stagged changes
```
git diff --staged
```
```
git diff --cached
```

Diff - ing specific files
```
git diff HEAD filename
```
```
git diff --staged filename
```

Diff-ing Branches
```
git diff branch_1 branch_2
```
Note: here the order has a meaning in the command, for the command above ---a will be the branch_1 and +++b will be the branch_2

To compare the specific file b/w two branches
```
git diff <branch1> <branch2> -- <filename>
```

To compare b/w commits
```
git diff commit_1 commit_2
```

