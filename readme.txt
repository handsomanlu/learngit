# readme.txt
# Learning Git, resource from https://www.liaoxuefeng.com/wiki/896043488029600

Git is a distributed version control system.
Git is free software.

1. Git Bash:
1.1 Getting start:
$ git config --global user.name "Your Name"
$ git config --global user.email "email@xxx.com"

1.2 Create working area, add files, show commit logs, commit the changes
$ git : to get help
$ git --help: to get help list, common Git commands
$ git init: to start a working area, to create an empty Git repository ...
$ git add: add file contents to the index (stage)
$ git log: to show commit logs
$ git commit -m "this is my comment": to record changes to the repository

Conclusion:
1. to create an empty git repository: $ git init
2. 2 steps to add files to git repository: 
    step 1: $ git add <file>, such as 
        $ git add file1.txt
		$ git add file2.txt file3.txt
    step 2: $ git commit -m <message>
	
1.3 Show changes, check the working tree status, re-add/commit
$ git diff <file>
$ git status

1.4 Version rolling back:
$ git log --pretty=oneline: to show simple log
$ git reflog: to show all the commit_id
$ git reset --hard HEAD^: roll back to last version
$ git reset --hard <commit_id>: roll back to the assigned commit_id version
$ cat <file>: to show file contents

1.5 Working area, Stage (Index), Branch Master (git的三个区：工作区、暂存区、主分支）
$ git add <file>: add file from Working area to Stage
$ git restore --staged <file>: to unstage
$ git commit -m <message>: to commit file from stage to master
$ git reset --hard HEAD^
$ git reset --hard <commit_id>

