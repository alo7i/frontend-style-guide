# gitlab init


## initialize
```shell
# 1. create branches
git branch develop
git branch beta
git branch staging

# 2. push to original
git push --set-upstream origin beta staging

# 3. how to delete orginal branch
git push origin --delete beta staging develop
```
