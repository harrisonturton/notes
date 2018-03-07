# Git

Git is a decentralised version control system.

#### Initialization

To create a new repository, run `git init` inside the root directory.

By default you cannot push to an empty git repo. To allow this, initialize with `git init --bare`.

#### Basics

| Behaviour | Command |
| :--- | :--- |
| Initialize repo | `git init` |
| Stage files | `git add <filename>` |
| Stage all new & modified files | `git add .` |
| Commit changes | `git commit -m "commit message"` |
|  |  |

#### Branching

| Behaviour | Command |
| :--- | :--- |
| List all branches | `git branch` |
| Create new branch | `git branch <name>` |
| Checkout \(enter\) branch | `git checkout <name>|<hash>` |
| Create new branch & checkout \(enter\) | `git checkout -b <name>` |



#### Reverting Changes





