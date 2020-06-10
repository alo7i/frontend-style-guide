# flow common
> 通用的流程。

## gitflow 
> git flow 的 各个流程描述。

### gitlab branches
| branch  | permission | need_merge | default_branch | description              |
| ------- | ---------- | ---------- | -------------- | ------------------------ |
| develop | public     | false      | true           | gitflow-develop          |
| beta    | protected  | true       | false          | 一般给测试人员使用的分支 |
| staging | public     | false      | false          | 这是是预发布环境         |
| master  | protected  | true       | false          | 线上稳定的代码           |


### hotfixs
1. 这里 gitflow 会在 master 分支拉取代码
2. 最终会合并代码回 develop/staging 分支上去?(这里又涉及权限问题)
3. `git flow` 起一个 `hotfix-1` 的临时分支
4. 开发: 修复好相关的 `bug`
5. git push --set-upstream origin hotfix/hotfix-1 到远程
6. git hotfix finish hotfix-1
7. 这时代码会合并到 develop/staging 分支
8. 检查没有 conflict 之后，git push --all -u 推到线上


### releases<Maintainer>
1. 项目分支 staging 为 relase 分支
2. 一般项目的 staging 会交给 git flow 来管理
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

### staging
- 这个过程其实是一个 release 的过程
- git flow release start 1.20.0
- 可能存在 conflict (理论上不应该出现)
- git flow release finish 1.20.0
- git push
- 这个权限是 public，所以可以完全交给 gitflow 来维护

## master(gitlab-有权限保护)
- 这里永远是 staging -> master
- 这里需要通过 mergeRequst方式完成
- NoOne可以直接进行操作

### master(hotfix/protected)
- https://github.com/petervanderdoes/gitflow-avh/issues/358

### resources
- https://www.git-tower.com/learn/git/ebook/cn/command-line/advanced-topics/git-flow
- https://zhangmengpl.gitbooks.io/gitlab-guide/content/whatisgitflow.html
- https://danielkummer.github.io/git-flow-cheatsheet/index.zh_CN.html
- https://www.jianshu.com/p/b4a060acda10
- https://www.tapd.cn/forum/view/86212
- https://s0docs0gitlab0com.icopy.site/ee/user/project/protected_branches.html
