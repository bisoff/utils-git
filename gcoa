#!/bin/bash
[[ "$GITHOST" == "" ]] && echo "\$GITHOST not defined!" && exit
msg=$1
#pwd | tr 'a-z' 'A-Z'
. lib-git
#echo -e "\033[0;34;48m sss \033[m"
echo -e "BRANCH: $green$(current_branch)$norm"

git add -A .
[[ "$msg" == "" ]] && msg=up
git commit -m "$(echo $GITHOST)-$msg" # $(date +'%d.%m.%y_%k:%M')
#gilf 1
# exit
