Master
text
git commit
Creates a new commit from staged files.

text
git push
Sends your commits to the remote repository.

Commit-One-File
text
git add <file>
Stages a specific file for commit.

Commit-One-File-Staged
text
git restore --staged <file>
Removes a file from the staging area without deleting changes.

Ignore-Them
A .gitignore file lists files and folders Git should skip.

text
touch .gitignore
Makes a new .gitignore file.

text
nano .gitignore
Opens .gitignore for editing in the terminal.

text
*.extension
Skips all files with a certain extension.

text
directories/
Excludes the directories folder from tracking.

Chase-Branch
text
git merge escaped
Merges the escaped branch; if chase is its ancestor, no issues occur.

Merge-Conflict
If a merge conflict happens, resolve it by editing the files, then use:

text
git merge
to finish merging.

Save-Your-works
text
git stash
Saves your current changes temporarily.

text
git stash pop
Restores the stashed changes.

Typical flow: stash changes, fix and commit a bug, pop the stash, finish your work, and commit again.

Change-Branch-History
text
git rebase hot-<branch>
Moves your branch’s commits to start after the latest commit on hot-<branch>.

Remove-Ignored
text
git rm <file>
Deletes a file from the repository and stages its removal.

Case-Sensitive-Rename
text
git mv <oldname> <newname>
Renames a file and stages the change.

Fix-Typo
text
git commit --amend -am "fixed typo"
Amends the previous commit with a new message after fixing a typo.

Forge-Date
text
git commit --amend --no-edit --date="1987-01-01T00:00:00"
Changes the date of the last commit without editing its message.

Fix-Old-Typo
text
git rebase -i HEAD~2
Starts an interactive rebase for the last two commits.

Change the second line from pick to edit, fix the typo, commit, then:

text
git rebase --continue
to apply the changes and finish rebasing.
