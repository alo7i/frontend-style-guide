# actions
> Git commit message 的常用动词。

## basic
~~~
feat: 新增一个完整feature
fix: 修复bug
docs: 仅仅修改了文档，比如README, CHANGELOG, CONTRIBUTE等等
style: 仅仅修改了空格、格式缩进、都好等等，不改变代码逻辑
refactor: 代码重构，没有加新功能或者修复bug
perf: 优化相关，比如提升性能、体验， 偏性能优化
test: 测试用例，包括单元测试、集成测试等
chore: 改变构建流程、或者增加依赖库、工具等
revert: 回滚到上一个/某个版本
~~~

## extension
~~~
add: 新增小功能 如加一个类型或者一个button
~~~

## 关于release-notes
> git log --pretty=oneline --since=2.weeks
> git log --since=2.weeks
> git log --pretty="%h - %s" --since="2020-05-23" --before="2020-06-03"
> 根据这个命令生成相关的 git log

~~~
feat(version): 功能
fix(version): 修复
~~~
