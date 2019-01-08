Git Intro
==========

- Part one cmd line env settings
# Preparing env for command line

# Git vs Github

### Working with ssh protocol, setting keys

`ssh-keygen -t rsa -b 4096 -C "your_email@example.com"`
`ls -l  ~/.ssh/`

### Install git cmd addons

install [git-completion.bash](https://github.com/git/git/blob/master/contrib/completion/git-completion.bash)
install [git-prompt.sh](https://github.com/git/git/blob/master/contrib/completion/git-prompt.sh)

### First time config
(first time config)[https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup]
aliases 

```Bash
[barak@barak-nixos:~/dev/gitinto]$ more ~/.gitconfig 
[user]
        email = barak.bar@gmail.com
        name = Barak Bar Orion
[include]
    path = /home/barak/gitalias.txt
[core]
        editor = emacs

more /home/barak/gitalias.txt
```

- Part two git concepts



### Git Model

#### Git Object Types

- Blobs
- Trees
- Commits
- Tags
- Index

#### Content-Addressable Names

##### commands that we are going to use to learn git internals (most of them  are not the commands we are working with in our day to day git work)

* find .
* git cat-file -p 
* git rev-parse
* git ls-files -s
* git write-tree
* git commit-tree
* git hash-object file


* git add 
* git status
* git rm
* git commit
* git log --follow

Talk about:
- sha
- objects
- tree
- commit
- index
- file mode (tracked, ignored, untracked)
- .gitignore, recursive !
- detailed view on page 58
- atomic, absolute named commits

- refs / symref
- relative commits names ^ ~
   - git show-branch --more=35 | tail -10
   - git rev-parse master~3      
   - git log -> git log HEAD
   - git log HEAD~2
   - git log master~2
   - git log -1 -p
   - git log --stat   
   - git show master
   - git show master:myDir
- commit graphs   
  - git log --graph
  - git log -300 --graph --all
- commit ranges
  - start..end  -- start is exclude while end is include
  - actually the presize defination is the set of node that reachable from start and not reachable from end
  - master~12..master~10 -> master~11, master~10
  - git log --stat master~1..master
- git bisect 
- git blame
- git log -S"barak"
- tags
- branch
  - git checkout -b
  - git checkout
  - git branche
  - git merge-base
  - git show-branch
  - git show-branch branch1 branch2
  - detached head
  - git branch -d   
- merge
  - git merge branch/commit
  - example of merge, with view of git show-branch and git log --graph --stat
  - example of conflict with the same tools.
  - git status to view unmarge files, git ls-files -u
  - git reset --hard HEAD
  - 
- diff
   - git diff [working dir and the index]
   - git diff commit [working dir vs commit]
   - git diff --cached commit [index and commit]
   - git diff commit commit
   - git diff --stat
   - git diff master~5 master Documentation/git-add.txt
  
- altering commits
  - git reset --soft commit (change only head, wf and index left as is)
  - git reset --mix (default, change index as well)
  - git reset --hard (change wf as well)
  - git reflog
  - git cherry-pick 
  - git revert
  - git commit --amend
  - git rebase branch1 branch2
  - git rebase -i 
  - rebase vs merge
  
- remote
  - git clone
  - git remote -v
  - .git/config
  - git ls-remote
  - git fetch
  - git pull
  - git push
  - git remote add
  - git remote remove
  - git branch -a
  - altering history !!!!
  - 
- other commands 
  - add -i / -p
  - stash
  - patch
    - git format-patch
	- git apply
	- git am



