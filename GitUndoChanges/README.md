### Undochanges and Time Travel

Checkout is not just used to switch between branches but also can be used for mulitple purposes like, going to the past commit or discard changes 

## Checkout to go the previous commits
Remember you can use 
```
git log --oneline
```
to list your commits in that particular branch or your directory. 


```
git checkout commit#
```

Dont panic when you see the following message 
"You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard ...."

Detached Head ?? - you can look around, make some experimental changes and commit them. 

Once you have checked out to a particular commit and you want to make a change you can branch off to a new branch by 

```
git checkout -b new_branch
```
Your head Re-Attached again from the detached head state. HEAD would now be at the this new branch created. 

You can also reference commits relative to HEAD

```
git checkout HEAD~1 
```
HEAD~1 is the commit before the HEAD (parent)
HEAD~2 is two commit before the HEAD (grandparent)

To go back to the previous branch you were on you can do 
```
git checkout - 
```
## Checkout to Discard Changes

Suppose you have made multiple commits and HEAD is at the branch with the latest valid commit. You went ahead and made some changes locally (not stagged or committed them)for some reason you want to undo the changes and go back to the same status as the HEAD. ofcourse you can use the cltr + z or undo or even remove them manually but git does it for you as well why not use it

```
git checkout HEAD filename
```
or
```
git checkout -- filename
```

## Restore

Discard changes in the repo 
```
git restore filename
```

## Reset
actually moves the pointer(HEAD) backwards and eliminating commits

If you have stagged a file and want to unstage it you can do 
```
git reset HEAD filename
```
If you want to reset your changes to the particular commit, this will remove the commits and changes
```
git reset --hard HEAD~1
```

If you want to remove the commits and keep the changes you can run (just remove --hard)
```
git reset HEAD~1
```
and now you can commit to another branch
```
git checkout -b bad_stuffs
```
If you want to reset your complete branch to the one same in the repo and dischard all your local changes

```
git fetch --all
```
```
git reset --hard origin/branch_name
```

## Revert

Create a brand new commit which reverses/undos the changes from a commit, because it results in a new commit you will be asked to enter a commit message




