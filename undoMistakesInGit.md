## Restore uncommited changes in a file

```
    git restore <file name>
```

---

## Restore all uncommited changes in whole folder structure and back to clean working dir

```
    git restore <.>
```

---

## Add a new message in prev commit

```
    git commit --amend -m "new message"
```

---

## To reset commit **MEAN: if you want to time travel back in time a go back to prev working commit and discard all commits that comes after of working commit**

```
    git reset --hard <commit hash eg: 193...fabda88>
```

flags: `--hard` and `--mixed`

### _--hard_ mean I need clean working directory

### _--mixed_ mean keep all prev changes **MEAN: It revert changes but keep all files in your working dir in form of uncommited**

---

## If you want to check a specific file history over the commits locally.

```
    git restore --source <commit hash> <file name>
```

---

## Track every movement of HEAD pointer **USE: recover deleted commits and branch atleast I know**

```
    git reflog
```

---

## A quite good practicle feature of reflog command as I say you will recover deleted commits or branches through reflog command so here is an example.

_After execute git reflog you will get all movement of your head pointer so copy the hash of the commit you want to restore and create a new branch and whalllah! you will get all of your deleted work _

> NOTE: do not restore lost commit in your master branch

```
    git reflog
    git branch <branch name> <commit hash>
```

---

## For move commit into different branch **eg: master -> <some other branch> OR <some other branch> -> master**

```
    git checkout <some other branch>
    git cherry-pick <commit SHA>
    git checkout master
    git reset --hard HEAD~1
```

---

# This is interactive rebase

## Change commit name far back in commit history **NOTE: This is do you by --amend command but it takes you back in history only 1 step** and if you want to go back more deep in commit history so here is some command for you

```
    git rebase -i HEAD~<number of steps you want to go deep in history like: 3>
```

## After you execute that command a pop window will apper. **Here something you should keep in mind 1: The window will show all your commits before the number of steps you provide in rebase command and the order will be reverse _MEAN: the first commit become last_ 2: You don't change commit message directely on that popup window to change commit name you should add this **reword** before the hash you will show on your window _eg: reword <hash 8bcf233> <commet message_ and save and closed after marking that line with that keyword and finally an another window will apper with your prev message where you should change your message after change message save and closed that window**

---

## Drop/delete a commit

```
    git rebase -i HEAD~<number of steps>
```

## here you need to use _drop_ keyword in front of hash of popup window

---

## Combine multiple commits

```
    git rebase -i HEAD~<number of steps>
```

## here you need to use **squash** keyword _please google how to use squash casuse it is quite easy_

> NOTE: when you use squash keyword It create a new commit and new commit mean you again need to provide new commit message
