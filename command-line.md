## Git

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

To simultaneously create & checkout a new branch, run :

```
git checkout -b <name>
```

By default, this branches from the current `HEAD` ref. Use `git checkout -b <new-branch> <existing-branch>` to branch from a different branch.

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

`HEAD` points to the current ref, `HEAD~` points to the previous commit, and `HEAD~n` points to the _nth_ previous commit.

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

This is the same as `git checkout <hash>` , but uses a `tag`  alias for the hash.

---

## Reverting Changes

#### Changing a commit

```
git commit --amend
```

To change the previous commit, add you new changes, and `git commit --amend`. If you don't need to change the commit message, you can use the `--no-edit` flag.

If you only want to change the commit message, simply run `git commit --amend -m "New Message"`.

#### Using \`git checkout\`

Use `git checkout` to go to the last valid commit. This should put you in the "Detached HEAD" state. Run `git checkout -b <name>` to branch from the valid commit. You can start making edits from here, and 'forget' about the invalid commits \(which will be orphaned and cleared\).

#### Using \`git revert\`

```
git revert HEAD
```

This will create a commit reversing the changes. This is best for public commits, as it will show in the history. If you want to revert the changes without commiting, you can run `git revert HEAD --no-commit`

#### Using \`git reset\`

```
git reset HEAD~
```

Reset to the previous commit.

* `--soft` The staged snapshot and working directory are not affected.
* `--mixed` \(default\) The staged snapshot matches the specified commit.
* `--hard` The staged snapshot & working directory matches the specified commit.

#### Undoing filelevel changes with \`git checkout\`

```
git checkout HEAD <filename>
```

This will revert the file to the commit specified by `HEAD`.

