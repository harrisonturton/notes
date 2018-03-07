# Git

## Branching

#### Listing Branches

```
git branch
```

To list all remote branches, run `git branch -a`

#### Creating a Branch

```
git branch <name>
```

To simultaneously create & checkout a new branch, run `git checkout -b <name>`.

#### Deleting a Branch

```
git branch -d <name>
```

This is a 'safe' operation. Git won't let you delete a branch with unmerged changes.

To force delete a branch \(e.g. if you don't care about the changes\), run `git branch -D <name>`

To delete a remote branch, run `git push origin --delete <name>`

---

## Moving the HEAD

We move between commits by moving the `HEAD` - a reference to a commit. The files we see are determined by which commit the `HEAD` is pointing to.



#### Moving to a Branch

```
git checkout <branch>
```

This will move the `HEAD` ref to a different branch, and the files will change to match the files in this branch.

```
git checkout <hash>
```

This can move the `HEAD` ref to a previous commit. This will put you into a "detatched head" state, where you can commit & make changes without affecting downstream commits & branches.

```
git checkout <tag>
```

This is the same as `git checkout <hash>` , but uses a `tag` as an alias for the hash.

---



