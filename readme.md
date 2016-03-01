## GIT TOOLS

### Overview:
- g*			aliases for lunch GIT commands (ex. for button bar in Total Commander)
- gitsw			switch git version by renaming folder if you use some versions of CLI git.
			  warning: to use it correctly (w/o context loose) run it as ". sw-git" and reopen shell
- lib			find_branch() current_branch() 
- g-help		print the file
- gitsw			MSYS: change git version

### Config/Status
- gib			git branch -vv  	# show local branches	
- gibn          		git branch --no-merged  # show not-merged branches (new)
- gibr 	<remote>	git branch -r -vv 	# show remotes
- giba			git branch -vv -a 	# all branches - local and remote
- gibr			git branch -vv		# only remote branches	
- gir			git remote -v		# show remotes
- gis			git status --ignored	# files including untracked
- gic			ed gitconfig		# global params (aliases, colors, etc.)

### Diff
- gid			git diff		# gis show??
- gid	<hash>		git diff "$1" "$1~1"	# diffs in commit
- gos	<hash>		git show $1		# work <-> HEAD | <hash>

### Commit Fetch Push Pull 
- gef			git fetch -vv		# fetch all remote branches
- gull			git pull
- gad	<msg>		git add -A .; git commit -m "$(echo $GITHOST)-$msg"
- gok	<msg>		goc "$*"; git push 
- gush			git push $curr_remote(only remote) $curr_branch -u

### Branch (lookuped by substring !)
- gib	<branch>	git checkout <branch> 	# switch to by branch
- gim	<branch>	git merge $branch>	# merge from branch
- gimr	<branch>	git merge $branch>	# merge from branch (with pull remote)
- gimto	<branch>	git checkout $branch; 	# merge current branch with another
			git merge $currbranch; 
			git checkout $currbranch

### Stash
gst			git stash
gpo			git pop
gsl			git stash list

### Log
gih			git log --pretty=format:"%h %ad | %s%d [%an]" --graph --date=short
gil	<commits_num>	git log --graph -n $commits_num --full-history --all --date=iso --color --pretty=format:".......
gilf	<commits_num>	git log --all --full-history --decorate --date=iso --pretty=format:"%C(red)%h - %C(g......
gilg			git log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d.....
gilg+			git log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit --date=relative -p
gils	<commits_num>	git log -n $commits_num -last --pretty=format:"%h%x09%Creset%an%x09%x09%s" --decorate --numstat | grep -v "^$"  | grep -vE "^[0-9a-f]{7}" | grep -vE "^-"
gils+	<commits_num>	git log -n $commits_num --pretty=format:"%C(yellow)%h%Cred%d\\ %Creset%s%Cblue\\ [%cn]" --decorate --numstat

