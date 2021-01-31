fix #issue	
close #issue
resolve #issue

<!-- undo commit / unstage -->
git reset HEAD^~1 --soft  	# undo local commit
git reset								# unstage
git reset <file>					# unstage file

<!-- merge upstream into local master -->
git fetch upstream
git checkout master
git merge upstream/master

<!-- checkout branch and merge into it master -->
git checkout dev git merge

<!-- same as above single lineer --> 
git merge dev master 

<!-- rebase dev on top of master - best practice, not for public repos -->
git checkout dev git rebase master

<!-- interactive for above - best practice, not for public repos -->
git checkout dev git rebase -i master

<!-- rebase or merge feature within feature branch -->
...

<!-- fix author -->
git config --global --edit
git commit --amend --reset-author
