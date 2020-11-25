## Restore uncommited changes in a file

```js
    git restore <file name>
```

---

## Restore all uncommited changes in whole folder structure and back to clean working dir

```js
    git restore <.>
```

---

## Add a new message in prev commit

```js
    git commit --amend -m "new message"
```

---

## To reset commit **MEAN: if you want to time travel back in time a go back to prev working commit and discard all commits that comes after of working commit**

```js
    git reset --hard <commit hash eg: 193...fabda88>
```

flags: `--hard` and `--mixed`

### _--hard_ mean I need clean working directory

### _--mixed_ mean keep all prev changes **MEAN: It revert changes but keep all files in your working dir in form of uncommited**

---

## If you want to check a specific file history over the commits locally.

```js
    git restore --source <commit hash> <file name>
```

---

## Track every movement of HEAD pointer **USE: recover deleted commits and branch atleast I know**

```js
    git reflog
```

---

## A quite good practicle feature of reflog command as I say you will recover deleted commits or branches through reflog command so here is an example.

_After execute git reflog you will get all movement of your head pointer so copy the hash of the commit you want to restore and create a new branch and whalllah! you will get all of your deleted work _

> NOTE: do not restore lost commit in your master branch

```js
    git reflog
    git branch <branch name> <commit hash>
```

---
