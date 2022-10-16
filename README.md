## Steps to run

```
docker build -t mytag .
docker run -d -it --name test mytag
docker exec -it --user testuser test /bin/bash -il
# now inside container
cd $HOME
git clone https://github.com/magicmonty/bash-git-prompt.git
```
