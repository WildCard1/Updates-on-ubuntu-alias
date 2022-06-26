# Updates-on-ubuntu-alias
Just a simple alias to update snap, flatpak, apt packages and git stuff in a one liner:

## Updates all flatpak, snap, git and apt packages
alias update=' orgPwd=$(pwd) && sudo printf "************************************ \nChecking for flatpak updates... \n************************************ \n" && sudo flatpak update && printf "************************************ \nChecking for snap updates... \n************************************ \n" && sudo snap refresh && printf "************************************ \nChecking for Ubuntu updates ... \n************************************ \n" && sudo apt update && sudo apt full-upgrade -y && printf "************************************ \nGit pull on everything in ~/github... \n************************************ \n" && cd ~/github && find . -mindepth 1 -maxdepth 1 -type d -print -exec git -C {} pull \; 2>/dev/null && cd $orgPwd'

