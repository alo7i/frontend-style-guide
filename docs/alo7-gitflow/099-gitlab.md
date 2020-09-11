# gitlab

## 分支权限设置
- https://git.saybot.net/aric.zheng/gitlab-flow/-/settings/repository

## settings
<img width="800" src="https://tva1.sinaimg.cn/large/007S8ZIlgy1gimtrzrivcj31by0gidi9.jpg" />


## staging/develop
- Maintainers 可以任意的操作
- 特别是 hotfix 这个操作，处理完之后，需要 merge 回 develop 和 staging 上去
- 熟悉的项目如 chao/aric 在 ng 项目的情况，两个人都设置成 maintainer 权限
- 如果是不熟悉项目的新同事，都设置成 develop 权限，进行正常操作，hotfix 可以让老同事，新建合并等操作
