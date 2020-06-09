# flow for alo7
> Git flow for frontend team.

### 特点
1. 大部分功能已经开发完毕
2. 大部分是bug修复为主

### feature
1. `git flow` 起一个 `feature` 的临时分支
2. 开发功能/git 提交代码
3. git flow finish 相应的 feature
4. 建议用 nickname/feat 方式命名

```shell
# 1. 起一个 parser 的功能分支
git flow feature start aric/parser

# 2.开发功能 balalba
git add --all
git commit -m "feat: parser done."
git push

# 3. Finsh `aric/parser`
git flow feature finish aric/parser
```
