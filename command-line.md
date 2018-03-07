# Git

#### Basics

| Behaviour | Command |
| :--- | :--- |
| Initialize new repository | `git init` |
| List branches | `git branch` |
| Create a new branch | `git branch <branch-name>` |
| Checkout \(enter\) a branch | `checkout <branch-name>` |
| Create & checkout a new branch | `git checkout -b <name>` |
| Stage all new & modified files \(but not deleted\) | `git add .` |
| Commit changes | `git commit -m "Commit message"` |

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

