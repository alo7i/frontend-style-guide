# kellis
> Kellis的基本开发规范。

## 编码规范
1. 编辑器: vscode/idea/vim 均可，习惯就行，安装好相应的插件
2. 新文件: 每个文件长度控制在 300 行代码以内
3. 旧文件: 尽可能少的增加代码
4. 新建文件: 推荐这种方式 `abc-component.tsx`
5. 其它: 遵循业界标准

## 源码解惑
1. 里面的 `nx`，一个工具，`window.nx` 可以直接调用; 类似于 `lodash` 的工具
2. `View`: 一个更快写 `StyledComponent` 的工具，有疑问先不要使用
3. `@jswork` 开头的包，是 [aric.zheng](aric.zheng@alo7.com) 写的，有问题可以直接联系
4. 其它: 前人挖坑，后人填坑

## 开发/git
- 安装 gitflow
- 分支介绍
   1. master: 线上代码，上线使用
   2. develop: 开发最新代码
   3. beta: beta环境代码，上beta环境使用
   4. staging: 预发布环境
- 开发一个功能
   1. 可以利用git flow 产生一个分支: `feature/{nickname}/my-new-feature`
   2. 提交到线上管理: `git flow feature publish my-new-feature` 
   3. `balabala` 开发功能
- 上线到测试环境(beta)
  1. 合并自己的 `feature/hotfix` 分支到 `beta` 即可; `rebase/merge` 方式任选
  2. 合并，经过同伴 `review` 经过 `ci` 自动执行，`beta` 发布成功
- 上线到预发布环境(staging)
  1. 合并 `beta` 分支到 `staging` 即可; `rebase/merge` 方式任选
  2. `staging` 发布成功
- 上线到生产环境(master)
  1. 合并 `beta` 分支到 `staging` 即可; `rebase/merge` 方式任选
  2. `staging` 发布成功
- 修复线上bug
  1. 从 `master` 切一个新的分支 `hotfix/{nickname}/nickname-missing`
  2. `balabala` 修复bug
  3. 合并代码到 `staging`
  4. 经过 qa 验证，
     1. 代码由 `staging -> master`: 发布上线
     2. 代码用 `cherry-pick` 方式合并到: `develop` 分支
- 分支清理: [git-sweep](https://github.com/afeiship/git-sweep)
  1. 以debug方式查看要清理的分支情况: `git-sweep -lr -f "aric" -d`
  2. 上述步骤如果没有问题，可以执行清理: `git-sweep -lr -f "aric"`
  3. **特别注意**：每次执行 `git-sweep` 之后，分支会自动切到 `master` 分支；谨慎操作。
