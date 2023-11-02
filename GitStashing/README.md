### Git Stashing

Why do we need Stash?

- git stash is helpful when you want to temporarily save changes in the working directory without commiting them to a branch. 

For example: If you are working on a branch_b and have made some changes/fix on this particular branch but you are not completed and do not want to commit them and you are asked to make some fix on branch_a, checking out to the branch_a will cause to issues, either your changes will be carried forward to the branch_a or might result into a conflict here is where git stash comes to your rescue. 

```
git stash
```

Once you have made the fix on branch_a, you can checkout back to branch_b and execute 
```
git stash pop
```

git stash pop bring backs the changes that were temporarily stored and it deletes the particular stash from the stash list

If you want to keep the stash for future and do not want to delete it from the stash list use
```
git stash apply
```

if you used git stash apply and want to delete the stash from the list use
```
git stash drop 
```

Yes!!!! you guessed it right, git stash pop is like the combination of both git stash apply and git stash drop


