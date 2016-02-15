#### GIT tools

- g*		- aliases for lunch GIT commands (ex. for button bar in Total Commander)
- gitsw		- switch git version by renaming folder if you use some versions of CLI git.
		  warning: to use it correctly (w/o context loose) run it as ". sw-git" and reopen shell

gec			git fetch
gef			git fetch
gek			git pull
gib	<branch>	git branch -vv -a  OR  git checkout <branch by first chars>
gibl	<branch>	git branch -vv  OR  gib $1
gibn			git branch --no-merged
gibr			git branch -r -vv #all
gid			git diff
gif			git fetch
gih			git log --pretty=format:"%h %ad | %s%d [%an]" --graph --date=short
gil	<commits_num>	git log --graph -n $commits_num --full-history --all --date=iso --color --pretty=format:".......
gilf	<commits_num>	git log --all --full-history --decorate --date=iso --pretty=format:"%C(red)%h - %C(g......
gilg			git log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d.....
gilg+			git log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit --date=relative -p
gils	<commits_num>	git log -n $commits_num -last --pretty=format:"%h%x09%Creset%an%x09%x09%s" --decorate --numstat | grep -v "^$"  | grep -vE "^[0-9a-f]{7}" | grep -vE "^-"
gils+	<commits_num>	git log -n $commits_num --pretty=format:"%C(yellow)%h%Cred%d\\ %Creset%s%Cblue\\ [%cn]" --decorate --numstat
gim	<branch>	git merge $branch
gimto	<branch>	git checkout $branch; git merge $currbranch; git checkout $currbranch
gir			git remote -v
gis			git status --ignored
gitsw			MSYS: change git version
goc	<msg>		git add -A .; git commit -m "$(echo $GITHOST)-$msg"
gok	<msg>		goc "$*"; git push 
gos	<hash>		git show $1
gost			git pop
gust			git stash
lib			find_branch() current_branch() 
