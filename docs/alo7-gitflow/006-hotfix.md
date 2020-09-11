# hotfix
> 热修复。


## steps
1. 新建一个 hotfix 分支
   > git flow hotfix start 1.22.1
2. publish 到线上
   > git flow hotfix publish
3. develop 开发，修复代码，提交
   > git add --all && git commit -m "fix: xxx" && git push
4. finish这个修复
   > git flow hotfix finish -p -m "1.22.12" (因为这个会自动打tag, 这个是 tag 的msg)
   > 各种填信息，然后就完成了
