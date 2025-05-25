# 1

```
git start master
```

# 2
Here, we want to commit just one file, so we stage the specific file and then commit.

```
git add A.txt
git commit -m 'Add A.txt'
```

# 3

To ensure only one of the staged files gets committed, we unstage the one we don't want and then commit the remaining.
```
git restore --staged B.txt
git commit -m 'Add A.txt'
```

# 4

For this step, we need Git to ignore certain files. This is handled by creating a .gitignore file.
```
touch .gitignore
nvim .gitignore
```

Add the following to `.gitignore`

```
*.exe
*.o
*.jar
libraries/
```
This setup will make Git skip tracking files with those extensions and the libraries directory.

Now, stage all the files you want and commit them:
```
git add .
git commit -m "Add .gitignore and file.txt"
```

# 5

Here, we merge the current branch with the escaped branch, which is ahead by two commits, using the merge command.

```
git merge escaped
```

# 6

In this task, merging with another-piece-of-work will create conflicts. You'll need to resolve these conflicts manually before you can finish the merge.
```
git merge another-piece-of-work
nvim equation.txt
```

After editing the file and resolving conflicts, stage and commit your changes.

```
git add equation.txt
git commit -m "Merge another-piece-of-work"
```

# 7

We need to temporarily set aside our incomplete work, so we stash it, fix the bug, and then bring our changes back.
```
git stash
nvim bug.txt
git add bug.txt
git commit -m "fix(bug)"
```

After the bug fix, retrieve your stashed work and finish up:

```
git stash pop
git add .
git commit -m "Finish work"
```

# 8

To incorporate a bugfix from a different branch, we use the rebase command.

```
git rebase hot-bugfix
```

# 9

To stop tracking files that are now in .gitignore, we use git rm to untrack them and then commit.
 

```
git rm ignored.txt
git commit -m "Remove ignored.txt"
```

# 10

For renaming a file (including case changes), we use git mv so Git recognizes the rename.

```
git mv File.txt file.txt
git commit -m "Rename File.txt to file.txt"
```

# 11

If you spot a typo in your last commit, you can fix it and amend the previous commit instead of making a new one.

```
nvim file.txt
git add file.txt
git commit --amend
```

# 12

To change the date on a commit, use the --date flag with git commit --amend, using the date format shown in git log.

```
git commit --date "Sun May 18 18:46:55 1987 +0530" --amend
```

# 13

If you need to correct an older commit, start an interactive rebase, edit the commit, and amend it as needed.

```
git rebase -i
```

Mark the commit for editing by changing pick to edit, then save and exit.
After fixing the typo in file.txt, stage and amend the commit:

```
git add file.txt
git commit --amend '-S'
```

Continue the rebase and resolve any conflicts that come up:

```
git rebase --continue
nvim file.txt
git add file.txt
git rebase --continue
```
