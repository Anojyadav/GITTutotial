### Git Merge Tutorials

'git merge' is a Git command used to integrate changes from one branch into another. It combines the changes made in a source branch (usually a feature or topic branch) into a target branch (usually the main or master branch). This is a common operation in Git when you're working on a software project with multiple contributors or when you're managing different features or bug fixes in separate branches.

```
git merge <feature-branch>
```

Note: You need to be at the branch to which you want to merge the new feature. For example A is your main branch and B is your feature branch and you want to merge the feature branch into main branch, then you need to checkout to the main branch and perform git merge. 


There can be merge conflict, which needs to be solved manually, to decide which changes you want to keep which you want discard or keep both. 

git merge uses various strategies such as Fast Forward, Recursive strategies(Default). 

1. Fast Foward strategy - A fast-forward merge occurs when Git can simply move the branch pointer of the target branch (e.g., main branch) to the same commit as the source branch, effectively bringing the changes from the source branch into the target branch without creating a new merge commit.
    e.g when a branch B is created from a main branch, and some commits have been made on the branch B while there is no commits made on the main branch since branch B was created then merging branch B into main by git merge would perform Fast Foward Merge


2. Recursive Strategy -  A recursive merge, also known as a three-way merge, is used when Git needs to create a new merge commit because the source branch and the target branch have diverged. It's the default merge strategy in Git.
    e.g when a branch B is created from a main branch, and some commits have been made on the branch B while there are new files(untracked files) added in the main branch since branch B was created then merging branch B into main by git merge would perform recursive strategy. 

--no-ff: This option forces Git to create a new merge commit, even if a fast-forward merge is possible. This is useful for creating a clear history of branch merges.

```
git merge --no-ff feature_branch
```

--squash: This option combines all the changes from the source branch into a single commit on the target branch, effectively squashing all the commits in the source branch into one.

```
git merge --squash my-feature
```

--abort: If you start a merge but encounter conflicts that you can't resolve or if you change your mind about the merge, you can use git merge --abort to cancel the merge operation.
```
git merge --abort
```