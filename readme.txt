# readme.txt

Git is a distributed version control system.
Git is free software.

1. Git Bash:
1.1 Getting start:
$ git config --global user.name "Your Name"
$ git config --global user.email "email@xxx.com

1.2 Create working area, add files, show commit logs, commit the changes
$ git --help: to get help list, common Git commands
$ git init: to start a working area, to create an empty Git repository ...
$ git add: add file contents to the index
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