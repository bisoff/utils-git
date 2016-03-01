#!/bin/bash
msg=$1
#pwd | tr 'a-z' 'A-Z'
. lib-git
#echo -e "\033[0;34;48m sss \033[m"
echo -e "BRANCH: $green$(current_branch)$norm"

#test not staged and echo!

if [[ "$msg" == "" ]]; then
	[[ "$GITHOST" == "" ]] && echo "\$GITHOST not defined!" && exit
	msg="$(echo $GITHOST)-up"
  fi
git commit -m "$msg" # $(date +'%d.%m.%y_%k:%M')
#gilf 1
# exit
