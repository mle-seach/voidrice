# Voidrice local bin only

The purpose of this repository is to provide `.local/bin` scripts from [voidrice](https://github.com/LukeSmithxyz/voidrice).

# How does it work ?

Basically im just using [git-filter-repo](https://github.com/newren/git-filter-repo)

```sh
git checkout master
git pull
git branch filtered-branch
git filter-repo --subdirectory-filter .local/bin --refs filtered-branch --force
git checkout local-bin-only
git merge filtered-branch
```
