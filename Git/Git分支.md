## Git分支操作
### git checkout
首先，我们创建dev分支，然后切换到dev分支：
```
PS C:\workspace\AtomSpace\MarkDowns> git checkout -b dev
Switched to a new branch 'dev'
```
`git checkout`命令加上`-b`参数表示创建并切换，相当于以下两条命令：

`git branch dev`
`git checkout dev`

### git branch
`git barnch`命令是查看分支状态，如下面的调用，显示的是所有的分支，以及当前所在的分支是 dev
```
PS C:\workspace\AtomSpace\MarkDowns> git branch
* dev
  master
```
