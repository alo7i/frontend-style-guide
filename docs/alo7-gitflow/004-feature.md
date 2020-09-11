# feature


## steps
1. start feature
> git flow feature start abc(注意，这里不带 aric/xxx 类似这种前缀)
> git flow feature publish (这后面可以不跟abc,git flow会自己找到当前分支的名字)

2. develop
> balalba...

3. push code
> git add --all && git commit -m "feat: abc start & finish" && git push

4. finish develop
> 找到 gitlab ，创建 MR

5. review通过之后(注意，这里不能直接使用 git finish)
> git branch -d feature/abc
> git checkout develop
