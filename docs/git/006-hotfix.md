# hotfix


## steps
1. 处在 `develop` 分支
2. 使用 `git flow hotfix start 1.22.1`
3. 生成分支，从 `staging` (我们是把 staging 设置为常用的 master 作用) 生成
   ~~~
    $ feizheng
    develop
  * hotfix/1.22.1
    staging
   ~~~
4. 直接在这个上面进行开发，如果开发新功能有新的
5. 如果开发完成，发布上线之后，可以用： `git flow hotfix finish 1.22.1`

## test
1. 测试的时候，直接把 hotfix/1.22.1 提 mr 到 beta 上进行测试
