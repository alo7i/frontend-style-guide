# feature/bugfix
> 以下是 feature/bugfix的开发步骤

## steps
1. start feature
  ```shell
  # 注意，这里不带 aric/xxx 类似这种前缀
  git flow feature start abc

  # 这后面可以不跟abc,git flow会自己找到当前分支的名字
  git flow feature publish
  ```

2. develop
  > balalba...

3. push code
  ```shell
  git add --all && git commit -m "feat: abc start & finish" && git push
  ```

4. finish develop
  > 找到 gitlab ，创建 MR

5. MR之后，会存在下面的问题
   ~~~
    Branches 'develop' and 'origin/develop' have diverged.
    Fatal: And branch 'develop' may be fast-forwarded.
   ~~~

6. review通过之后(注意，这里不能直接使用 git finish)(6/7任选一种适合自己的方案即可)
  ```shell
  git branch -d feature/abc
  git checkout develop
  ```

7. 或者使用下面的方式(理论上这一步之后，不应该有任何的git push)(6/7任选一种适合自己的方案即可)
  ```shell
  # 这个过程，可能需要处理 conflict
  git checkout develop && git pull && git checkout
  git flow finish
  ```
