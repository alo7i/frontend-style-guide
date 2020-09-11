# gitlab

## 分支权限设置
- https://gitlab.demo.com/gitlab-flow/-/settings/repository

## settings
<img width="800" src="https://tva1.sinaimg.cn/large/007S8ZIlgy1gimtrzrivcj31by0gidi9.jpg" />

## gitlab不要删除远程分支(否则gitlab报错)
- [Enable 'Delete source branch' option by default](https://gitlab.demo.com/gitlab-flow/edit#js-merge-request-settings) 这个关掉，不要主动删除远程分支，让 git-flow 来删除
<img width="800" src="https://tva1.sinaimg.cn/large/007S8ZIlgy1gimugi1bnpj31cm0coq5s.jpg" />

## staging/develop
- Maintainers 可以任意的操作
- 特别是 hotfix 这个操作，处理完之后，需要 merge 回 develop 和 staging 上去
- 熟悉的项目如 chao/aric 在 ng 项目的情况，两个人都设置成 maintainer 权限
- 如果是不熟悉项目的新同事，都设置成 develop 权限，进行正常操作，hotfix 可以让老同事，新建合并等操作
