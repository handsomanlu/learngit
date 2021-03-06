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

1.6 Verify difference
Note: git commit是把file从stage放进master!!!!!
    git add <file> 是把file从working area放进stage!!!
	而working area就是working directory，里面的file一改动存档后，file就变了。
	可以用git diff HEAD -- <file> 去看看working area和master的版本差异。

$ git diff: to verify the difference of between of file in between working area and stage.
$ git diff HEAD -- <file>: to verify the difference of file in between working area and master.

1.7. Roll back changes:
$ git reset --hard HEAD^: roll back to last version for the file both in working area and master!
    记得：是同时把工作区和版本库的版本都变回前一个版本了！
$ git reset --hard <commit_id>: roll back to the version of commit_id in both of working area and master.
    记得：是同时改动工作区和版本库的版本了！
$ git reset HEAD -- <file>: unstage file to working area!
$ git checkout -- <file>: discard changes

1.8 delete a file
$ rm <file>: delete files in working area
 --> un-delete: $ git checkout -- <file>
$ git rm <file>: delete files from working area and from index (stage).
 --> (1) $ git restore --staged <file>
     (2) $ git checkout -- <file>
	 
***Minemap: link to 'Git 3-area minemap.jpg'

1.9 分支管理
git branch <branch_name>: create branch
git checkout <branch_name>: change to branch_name
git branch: show branch tree
git merge <branch_name>: merge branch_name to current branch
git branch -d <branch_name>: delete branch_name
git checkout -b <branch_name>: build branch_name and then change to it

1.10 log history
git log
git log -10
git reflog
git log --oneline
git log --graph
git log --reverse --oneline
git log --oneline --before={3.weeks.ago} --after={2020-4-1} --no-merges
q: to quit log

1.11 git tag
git tag -a <tag_name>: ex. git tag -a v1.0 to current HEAD
git tag -a <tag_name> <commit_id>: add tag to <commit_id>
git tag: show tag list
git tag -a <tag_name> -m "tag_cmment"

