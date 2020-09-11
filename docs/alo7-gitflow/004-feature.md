# feature


## steps
1. start feature
> git flow feature start abc(注意，这里不带 aric/xxx 类似这种前缀)
> git flow feature publish (这后面可以不跟abc,git flow会自己找到当前分支的名字)

2. develop
> balalba...

3. publish(实际上在start完成也可以publish,这一步实际上是把 feature分支推送到 origin)
> git flow feature publish abc

4. push code
> git add --all && git commit -m "feat: abc start & finish" && git push

