## git切换tag并提交代码

由于公司线上也有多套环境，每次发版本之后会打tag,但是某个环境可能不是master的代码，修复bug时就需要以tag为基准分支作为热修复分支。

tag是只读分支，所以需要重命名为新分支

### 1. fetch 线上所有的tag到本地

```shell
 git fetch --tags
```

### 2. 切换到你需要修复的tag

```shell
git checkout [tag_name]
```

### 3. 将tag重命名为可修改的分支

```shell
git switch -c <new-branch-name> #可以将此版本作为tag的热修复版本，测试没问题之后可以直接发布
```

### 4. 合并代码

将修改的分支合并到其他分支

