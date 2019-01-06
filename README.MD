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
- tag
- index
- file mode (tracked, ignored, untracked)
- .gitignore, recursive !
- detailed view on page 58
- atomic, absolute named commits


 
- Part three Using git



