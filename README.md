# git-hub-initials

--Inntial setup
--- git config --global user.name "name"
--- git config --global user.email "email"
--- git config --global core.editor "code --wait"
--- git config --global core.autocrlf

# Making git available in our project :--
--- git init

# Stages of any changes in our Local git repo :--
U - untracked
A - Added or staged
C - Commited

# Making a checkpoint or saved point :--
Adding a file
Staging a file
Commiting a file

# Checking saved point whatever made while change in codebase :--
--- git log --oneline

# Going back to some previous saved points :--
-- It has three option reset --hard/soft/mixed 
--- git reset --hard HEAD~1

## There are two types of command used for going back to some previous saved points :--
1. --- git reset
2. --- git revert

```
The git reset and git revert commands in Git are both used to undo changes in a repository, but they achieve this in different ways and have different implications:
```

1. git reset
Purpose: git reset is primarily used to reset the current branch to a specific state. It moves the HEAD (and optionally the index and working directory) to a specified commit.

Effects:
Changes HEAD: Moves the HEAD pointer to the specified commit.
Index: Depending on the reset type (--soft, --mixed, --hard), it can reset the index (staging area) and working directory to match the specified commit.

Uncommitted Changes: With --soft, retains changes in the working directory and index. With --mixed, resets the index but keeps changes in the working directory. With --hard, resets the index and working directory to match the specified commit, discarding changes.
*** Permanent: Changes made with git reset are more aggressive and can permanently delete commits or changes if not careful.

2. git revert
Purpose: git revert is used to create a new commit that undoes a previous commit or range of commits. It does this by applying a new commit that inverses the specified commit(s).

Effects:
Commit History: Adds a new commit that undoes the changes introduced by a previous commit or series of commits, creating a new commit history.

Safe: It's safer in the sense that it doesn't alter existing commits; instead, it adds new ones that effectively undo changes.
Reversibility: The revert commit itself can be reverted if needed, allowing for easier management of mistakes or changes in decision.
Key Differences:
Nature of Changes:

git reset modifies the repository's history by moving the HEAD and possibly changing the index and working directory. It can alter the commit history and is more powerful but also more dangerous.
git revert keeps the existing commit history intact and adds new commits to undo specific changes. It's safer and more suitable for reverting changes already shared with others.
Undo Mechanism:

git reset undoes changes by modifying the current branch's state directly, potentially losing commits permanently (with --hard).
git revert undoes changes by creating a new commit that reverses the effect of a previous commit, preserving the commit history and making the process safer and more transparent.

When to Use Each:
Use git reset when you need to completely remove commits from the current branch or reset the branch's state entirely. This is useful for local branches or branches not shared with others.

Use git revert when you want to undo changes in a way that keeps the commit history intact and does not affect collaborators. This is crucial for shared branches or when changes have already been pushed to a remote repository.

In summary, git reset is used for altering branch history and can be more aggressive, while git revert is used for creating new commits that undo specific changes, preserving commit history and being safer for collaborative environments.

# git status/git status -s
--git status batata hai commit ke pahle and commit ke baad ke file stage.

# git log/git log --online
--git log batata hai saare commit histories ko.

# Branching :--
--- git branch
--- git branch feature/navbar
--- git switch feature/navbar
