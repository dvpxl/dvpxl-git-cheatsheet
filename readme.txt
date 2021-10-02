=========================
# commit comments with issue ref

fix     #issue
close   #issue
resolve #issue

=========================
# new repository worksflows
git branch -M master       # change branch, force (-M, caps) if exists
git push -u origin master  # push and also set the upstream (-u)

=========================
# revert vs reset
revert: undo and creates commit
reset:  undo without commit

=========================
# undo commit of earlier, staged files, undo a staged file
git reset HEAD^~1 --soft  	# undo local commit, still staged
git reset				    # unstage

# remove (unstage) a staged file
git reset <file>		    # unstage file
=========================

# merge upstream into local master
git fetch upstream
git checkout master
git merge upstream/master

# checkout branch and merge into it master
git checkout dev git merge

# same as above single liner
git merge dev master

# rebase dev on top of master - best practice, not for public repos
git checkout dev git rebase master

# interactive for above - best practice, not for public repos -->
git checkout dev git rebase -i master

# rebase or merge feature within feature branch
...

# fix author
git config --global --edit
git commit --amend --reset-author
