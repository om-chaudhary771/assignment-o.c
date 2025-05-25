1. master
Initialize the exercise.
Use git start to make your initial commit.
Verify your setup using git verify.

2. commit-one-file
Add a file by running git add A.txt.
Commit your changes with git commit -m "commit message".
Check your work with git verify.

3. commit-one-file-staged
Unstage all files using git reset.
Add the file you want to commit with git add A.txt.
To unstage a specific file, use git reset B.txt.
Commit with git commit -m "commit message".
Verify using git verify.

4. ignore-them
Create a .gitignore file with touch .gitignore and add these lines:
*.exe
*.o
*.jar
libraries/
Stage and commit the .gitignore file:
git add .gitignore
git commit -m "add .gitignore"
git verify

5. chase-branch
Merge the escaped branch using git merge escaped.
Check the result with git verify.

6. merge-conflict
Run git merge another-piece-of-work to create a conflict.
Manually resolve equation.txt.
Then run:
git add equation.txt
git commit -m "merge another-piece of work"
git verify

7. save-your-work
Save your current changes with git stash.
Fix the bug and commit:
git add bug.txt
git commit -m "fix bug"
Apply your stashed changes with git stash pop.
Update bug.txt as needed.
Add all files with git add .
Commit and verify:
git commit -m "update files"
git verify

8. change-branch-history
Rebase onto hot-bugfix and change-branch-history with git rebase hot-bugfix change-branch-history.
Verify with git verify.

9. remove-ignored
Remove a file from tracking:
git rm ignored.txt
git commit -m "untrack file"
git verify

10. case-sensitive-filename
Rename File.txt to file.txt:
git mv File.txt file.txt
git commit -m "rename file"
git verify

11. fix-typo
Edit file.txt to fix the typo.
Stage and amend the commit:
git add file.txt
git commit --amend -m "Add Hello world"
git verify

12. forge-date
Amend the commit date:
git commit --amend --date=1987 -m "add work.txt"
git verify

13. fix-old-typo
Start an interactive rebase with git rebase -i.
Change pick to edit for the commit you want to update.
Edit file.txt as needed.
Stage the file with git add file.txt.
Amend the commit with git commit --amend -S -m "Add Hello world".
If there is a conflict, resolve it, then run:
git add file.txt
git rebase --continue
git verify

