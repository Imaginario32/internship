## Prerequsite

* Git 2.28 or greater

## Tasks

* fork the current repository

* clone it, find the commit "failed changes commit, revert me" and revert them!

*Please note that after completing this task, the number of folders with tasks must change!*

* after passing all the questions from all folders, make a pull-request with the results of the task and the tag Done-current date (e.g. `Done-01-01-2021`)


## Questions

1. What command can I use to view the commit history?
	git log

2. What command can I use to undo the last commit?
	git reset --soft HEAD~1

3. What command can I use to create a new branch and a new tag?
	git checkout -b newbranche newtag

4. How do I exclude a file / folder from a commit?
	In .gitignore, add the path to the file / folder
	or
	git add -u
	git reset -- folder/file

5. In case of a merge conflict, what commands can be used to resolve it?
  	git mergetool
	or
	edit conflict
	git commit -m  "added commit"
	git add

6. `*` What are pre-commit hooks and post-commit hooks, and what are they for?
	Hooks are custom scripts when certain important actions
	pre-commit is meant primarily for notification
	post-commit is for notification, and cannot affect the outcome of git commit

7. `*` How do I change the last commit without adding a new commit?
	git commit --amend
