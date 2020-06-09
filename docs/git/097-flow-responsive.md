# flow for responsive
> 快速响应型的项目流程。

### 特点
1. 项目变化比较快，典型的就是互联网项目
2. 经常会有很多 feature 出现，但可能到截止日期前，部分功能上线，部分功能被砍掉

### features
1. 新功能1: `git flow` 起一个 `feature-1`
2. 新功能2: `git flow` 起一个 `feature-2`
3. 开发: feature-1 功能
4. 开发: feature-2 功能
5. 发布: `git flow feature publish feature-1`;
6. 发布: `git flow feature publish feature-2`;
7. 项目决定发布 feature-1 而放弃 feature-2
8. git flow feature finish feature-1

