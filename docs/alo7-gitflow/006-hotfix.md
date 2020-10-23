# hotfix
> 热修复。


## steps
1. 新建一个 hotfix 分支
  ```shell
  git flow hotfix start 1.22.1
  ```
2. publish 到线上
  ```shell
  git flow hotfix publish
  ```
3. develop 开发，修复代码，提交
  ```shell
  git add --all && git commit -m "fix: xxx" && git push
  ```
4. finish这个修复
  ```shell
  # 因为这个会自动打tag, 这个是 tag 的msg
  git flow hotfix finish -p -m "1.22.12"
  
  # 各种填信息，然后就完成了
  ```
5. 没问题的情况下，测试通过
   1. 提交 mr: staging -> master
   2. 等delopy，然后上线测试

> 如果希望严格一点的，可以第4步走这个流程
~~~
4 . 各种提交 merge request
   1. hotfix/1.22.1 -> develop
   2. hotfix/1.22.1 -> beta
   3. hotfix/1.22.1 -> staging 
   4. 然后: 提交测试 -->
~~~
