## GIT TOOLS

### Overview: -----------------
- g*			aliases for lunch GIT commands (ex. for button bar in Total Commander)
- gitsw			switch git version by renaming folder if you use some versions of CLI git.
			  warning: to use it correctly (w/o context loose) run it as ". sw-git" and reopen shell
- lib			find_branch() current_branch() 
- g-help		print the file
- gitsw			MSYS: change git version


### Config/Status -----------------
- gib			# show local branches			git branch -vv  	
- gibnm          	# show not-merged branches (new)	git branch --no-merged  
- gibr 	<remote>	# show remotes				git branch -r -vv 	
- giba			# show local and remote branches  	git branch -vv -a 	
- gibr			# only remote branches			git branch -vv		

- gir			# show remotes				git remote -v		
- gis			# files including untracked		git status --ignored	

- gec			# global git params 			ed ~/.gitconfig
- gect			# repo params 				ed ./.git/config
- geh			# edit readme.md			ed "$(dirname $0)/readme.md"


### Diff -----------------
- gid			# gis show??				git diff
- gid	<hash>		# diffs in commit			git diff "$1" "$1~1"	
- gos	<hash>		# work <-> HEAD | <hash>		git show $1		


### Commit Fetch Push Pull -----------------
- gef			# fetch all remote branches		git fetch -vv		
- gull		# pull (fetch and merge)		git pull
- gus			# push 					git push $curr_remote(only remote) $curr_branch -u

- ga	<mask>		# stage all or by mask			git add -A .  OR  git add <mask>
- gac	<msg> 		# stage all and commit 			git add -A .; git commit -m "$msg"  # [[ "$msg" == "" ]]; $msg="$(echo $GITHOST)-up"
- gacm  <msg>		# stage all & commit ammend		git commit --amend -m "$1"
- gc    <msg>		# commit staged				git commit -m "$msg"
- gcm   <msg>		# commit ammend				git commit --amend -m "$1"
- gok	<msg>		# commit staged & push			git add -A . ; git commit -m "$msg"; git push 


### Branch (name looked up by substring ) ----------
- gib	<branch>	# switch to by branch			git checkout <branch> 	
- giba	<branch>	# switch to by branch		  	git checkout <branch> 	
- gibd  <branch>	# delete branch				git branch -d <branch>  # возможно если ветка была смержена
- gibdd <branch>	# delete branch				git branch -D <branch>  # удалить в любом случае 
- gim	<branch>	# merge from branch			git merge <branch>	
- gimr	<branch>	# merge from branch (with pull remote)	git merge <branch>	
- gimto	<branch>	# merge current branch with another	git checkout <branch>	
								  git merge $currbranch
								  git checkout $currbranch
- gibn	<branch>	# create new branch			git checkout -b <branch> 

### Stash ------------------
- gst			git stash
- gsp			git pop
- gsl			git stash list


### Log -----------------
- gilh			git log --pretty=format:"%h %ad | %s%d [%an]" --graph --date=short	
- gil	<commits_num>	git log --graph -n $commits_num --full-history --all --date=iso --color --pretty=format:".......
- gilf	<commits_num>	git log --all --full-history --decorate --date=iso --pretty=format:"%C(red)%h - %C(g......
- gilg			git log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d.....
- gilg+			git log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit --date=relative -p
- gils	<commits_num>	git log -n $commits_num -last --pretty=format:"%h%x09%Creset%an%x09%x09%s" --decorate --numstat | grep -v "^$"  | grep -vE "^[0-9a-f]{7}" | grep -vE "^-"
- gils+	<commits_num>	git log -n $commits_num --pretty=format:"%C(yellow)%h%Cred%d\\ %Creset%s%Cblue\\ [%cn]" --decorate --numstat

