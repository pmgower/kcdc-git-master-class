# Git `master` Class

"It's just version control." Or is it? When I started using `git-svn` more than
five years ago, I never imagined how fundamentally Git would change the way I
develop software. This session will cast new light on the basic Git commands
you already know as a first step into a hands-on exploration of the more
advanced tools at our disposal to develop software on our terms. Topics covered
will include local and distributed workflows, history inspection and
manipulation, and a glimpse into the power available through tools like
filter-branch`.

## Agenda

0:00 Introductions
0:15 Git Environment
0:30 git init & Core Concepts
1:20 <Break>

## Keith Dahlby

* E-Commerce Architect @ Motorsport Aftermarket Group
* https://github.com/dahlbyk/posh-git
* https://github.com/libgit2/libgit2sharp
* Go Cyclones!
* @dahlbyk

## Git Environment

### Configuration

- `git help config`
- Scopes
  - Repository (`[--local]`) in `.git/config`
  - User (`--global`) in `$XDG_CONFIG_HOME/git/config` or `~/.gitconfig`
  - System (`--system`) in `$GIT_INSTALL_DIR/etc/gitconfig`
- `git config -e <scope>`

```
# git config core.editor vim
[core]
	editor = vim

# git config branch.master.rebase true
[branch "master"]
	remote = origin
	merge = refs/heads/master
	rebase = true
```

#### Suggestions

- `diff.renames = copies`
- `difftool.prompt = false`
- `mergetool.prompt = false`
- `mergetool.keepBackup = false`
- `help.autocorrect = 5`
- `log.date = relative`

### Aliases

- `git config alias.ds "diff --stat"
- `git ds` => `git diff --stat`
- `git ds dev` => `git diff

#### Suggestions

- `alias.lg = log --oneline --decorate ----graph
- `alias.new = log --oneline --decorate --reverse master..`
- http://bit.ly/better-git-svn

## git init & Core Concepts

### Working Directory

### Index

### Commit
Takes the current index and turns it into something stored for all time.

#### Blob
Just the content.  During renames it just compares blobs.

Blobs are attached to a tree at some path.  Trees are case sensitive.

#### Tree
Tree is the content at is in a Commit

#### Metadata
##### hooks
##### info
##### objects
###### info
Blobs are stored here
###### pack
##### refs
###### heads
Branches are stored here.
###### tags
Tags are a fixed point in time

### HEAD

### Checkout

### History
