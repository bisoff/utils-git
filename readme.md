## GIT TOOLS

### Overview:
- g*			aliases for lunch GIT commands (ex. for button bar in Total Commander)
- gitsw			switch git version by renaming folder if you use some versions of CLI git.
			  warning: to use it correctly (w/o context loose) run it as ". sw-git" and reopen shell
- lib			find_branch() current_branch() 
- g-help		print the file
- gitsw			MSYS: change git version

### Commit Fetch Push Pull 
 gec			~ gif
 gef			~ gif
  gfe?
gif			git fetch -vv		# fetch all remote branches
gek			git pull
goc	<msg>		git add -A .; git commit -m "$(echo $GITHOST)-$msg"
gok	<msg>		goc "$*"; git push 
guk			git push $curr_remote(only remote) $curr_branch -u

### Branch (lookuped by substring !)
gib	<branch>	git checkout <branch>  #switch to by
gim	<branch>	git merge $branch>
gimto	<branch>	git checkout $branch; git merge $currbranch; git checkout $currbranch

### Log
gih			git log --pretty=format:"%h %ad | %s%d [%an]" --graph --date=short
gil	<commits_num>	git log --graph -n $commits_num --full-history --all --date=iso --color --pretty=format:".......
gilf	<commits_num>	git log --all --full-history --decorate --date=iso --pretty=format:"%C(red)%h - %C(g......
gilg			git log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d.....
gilg+			git log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit --date=relative -p
gils	<commits_num>	git log -n $commits_num -last --pretty=format:"%h%x09%Creset%an%x09%x09%s" --decorate --numstat | grep -v "^$"  | grep -vE "^[0-9a-f]{7}" | grep -vE "^-"
gils+	<commits_num>	git log -n $commits_num --pretty=format:"%C(yellow)%h%Cred%d\\ %Creset%s%Cblue\\ [%cn]" --decorate --numstat

### Config/Status
gib			git branch -vv  	# only local branches	
gibn          		git branch --no-merged  
gibr 	<remote>	git branch -r -vv 	# info from remotes
giba			git branch -vv -a 	# all branches - local and remote
gibr			git branch -vv		# only remote branches	
gir			git remote -v		# show remotes
gis			git status --ignored	# files including untracked

### Diff
gid			git diff		# gis show??
gos	<hash>		git show $1		# work <-> HEAD | <hash>

### Stash
gost			git pop
gust			git stash
gib
