# flow for alo7

## 新功能开发
1. git flow 起一个 feature 的临时分支
2. 开发功能
3. git 提交代码
4. gitlab 手动新建一个 merge request
5. 互相或者leader `review` 代码
6. 没问题的情况下，完成 code merge到 develop 分支
7. git flow finish 相应的 feature

```shell
# 1. 起一个 parser 的功能分支
git flow feature start aric/parser

# 2.开发功能 balalba
git add --all
git commit -m "feat: parser done."
git push

# 3. Go to gitlab new Merge Request
# 4. Wait code review
# 5. Merge code to develop
# 6. Finsh `aric/parser`
git flow feature aric/parser
```

## 紧急BUG修复

## 发版，Tag