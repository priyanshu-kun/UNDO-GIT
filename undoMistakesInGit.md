## Restore uncommited changes in a file

```js
    git restore <file name>
```

## Restore all uncommited changes in whole folder structure and back to clean working dir

```js
    git restore <.>
```

## Add a new message in prev commit

```js
    git commit --amend -m "new message"
```

## To reset commit MEAN: if you want to time travel back in time a go back to prev working commit and discard all commits that comes after of working commit

```js
    git reset --hard <commit hash eg: 193...fabda88>
```

flags: `--hard` and `--mixed`

### --hard mean I need clean working directory

### --mixed mean keep all prev changes
