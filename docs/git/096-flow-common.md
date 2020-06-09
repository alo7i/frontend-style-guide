# flow common
> 通用的流程。

## gitflow 
> git flow 的 各个流程描述。

### hotfixs
1. 这里 gitflow 会在 master 分支拉取代码
2. 最终会合并代码回 develop/master 分支上去?(这里又涉及权限问题)
3. `git flow` 起一个 `hotfix-1` 的临时分支
4. 开发: 修复好相关的 `bug`
5. git push --set-upstream origin hotfix/hotfix-1 到远程
6. git hotfix finish hotfix-1


### releases<Maintainer>
1. 项目分支 master 为 relase 分支
2. 一般项目的 master 有特定的人会有这个权限来做这个操作。
3. 确定版本号: git flow release start 1.21.0
4. git flow release finish 1.21.0
5. 这个时候会产生新的 tag ，需要 push 到远程: git push origin --tags

### tag<Maintainer>
1. 会在上述 `release` 操作中产生新的 tag
2. 可以在 gitlab 再详情补充 release notes.

--- 

## gitlab
> 与 gitlab 结合部分。

### develop 
- 这个分支原则上开发可以 `相对自由` 的操作
- 相对自由: 大部分操作可以用 `git flow` 的流程，命令完成

### bete(gitlab-有权限保护)
- 开发在 `develop` 上起 `feature` 分支 (gff标准流程)
- gff-finish的时候，会自动合并代码到 develop 分支，等待用户推送/处理 conflict
- 手动 develop -> beta ，这个过程需要 (code review)
- 最终完成 develop -> beta 版代码合并

### staging(gitlab-有权限保护)
- 还是保持原样
- 这里 developer 还是保持原来的流程; 手动写 merge requst 来完成 beta 到 staging 的合并
- Mantainer 可以直接 merge；但一般推荐和 develop 走一样的流程

### master(gitlab-有权限保护)
- 这个过程其实是一个 release 的过程
- git flow release start 1.20.0
- 可能存在 conflict (理论上不应该出现)
- git flow release finish 1.20.0
- git push
- 权限问题: 所以这个操作需要 Mantainer 来进行

### resources
- https://www.git-tower.com/learn/git/ebook/cn/command-line/advanced-topics/git-flow
- https://zhangmengpl.gitbooks.io/gitlab-guide/content/whatisgitflow.html
- https://danielkummer.github.io/git-flow-cheatsheet/index.zh_CN.html
- https://www.jianshu.com/p/b4a060acda10
- https://www.tapd.cn/forum/view/86212
- https://s0docs0gitlab0com.icopy.site/ee/user/project/protected_branches.html
