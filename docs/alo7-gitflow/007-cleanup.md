# cleanup
> 分支清理。

## tips
- **这个操作需要比较谨慎**，默认不会删除重要分支如 develop/staging/beta/alpha/develop 等。
- 如果不熟悉流程，请使用 -d(debug) 或者 -i(interactive) 参数

## tools
```shell
npm install -g @feizheng/git-sweep
```

## interactive
```shell
git-sweep -i
```

## debug
```shell
git-sweep -l -r -d
```

## clean local
```shell
git-sweep -l
```

## clean remote
```shell
git-sweep -r
```

## clean all
```shell
git-sweep -lr
```

