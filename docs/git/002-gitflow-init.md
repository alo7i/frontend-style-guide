# gitflow init


## initialize
```shell
# 1. init
git flow init

# 2.
# Which branch should be used for bringing forth production releases?
- staging (由于master是protected，所以这里要选预发布分支)
# Which branch should be used for integration of the "next release"?
- develop 

# 3. others
# How to name your supporting branch prefixes?
# Feature branches? [feature/]
# Bugfix branches? [bugfix/]
# Release branches? [release/]
# Hotfix branches? [hotfix/]
# Support branches? [support/]
# Version tag prefix? []
# Hooks and filters directory? [C:/testzee/nodejs/Koala/.git/hooks]
```

## remove
```shell
git config --remove-section "gitflow.path"
git config --remove-section "gitflow.prefix"
git config --remove-section "gitflow.branch"
```
