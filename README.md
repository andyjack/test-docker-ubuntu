## Steps to run

```
docker build -t mytag .
docker run -d -it --name test mytag
docker exec -it --user testuser test /bin/bash -il

# now inside container. Wait 60 seconds at the prompt to be automatically
# logged out. Rerun 'docker exec' command to log back in.

cd $HOME
git clone https://github.com/magicmonty/bash-git-prompt.git
cd bash-git-prompt
. gitprompt.sh

# wait 60 seconds... no automatic logout occurs

# Try the same with git's git-prompt.sh
cd $HOME
git clone https://github.com/git/git
cd git/contrib/completion
. git-prompt.sh
# then add the prompt - setting this var runs the code that has 'while read'
export GIT_PS1_SHOWUPSTREAM="auto"
PROMPT_COMMAND='__git_ps1 "\u@\h:\w" "\\\$ "'
# no automatic logout occurs
```
