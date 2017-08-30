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
### git merge
dev分支上做的改动，在切换回master之后是看不到的，因为这是在这个分支上进行的改动。那么当我们切换回master后如何把分支上的代码合并过来呢，就是通过调用`git merge dev`这个命令了。
```
PS C:\workspace\AtomSpace\MarkDowns> git merge dev
Updating eb19384..079e10c
Fast-forward
 "Git/Git分支.md" | 18 ++++++++++++++++++
 1 file changed, 18 insertions(+)
```
合并了之后，再调用`git checkout master`切换回master后，就能在主干上看到所有改动了。
### git branch -d ***
分支合并了之后就会要删除不用的分支，这就是删除分支的指令了。
```
PS C:\workspace\AtomSpace\MarkDowns> git branch -d dev
Deleted branch branch_test (was 079e10c).
PS C:\workspace\AtomSpace\MarkDowns> git branch
* master
```
**注意：上面说的所有的分支操作都是在本地仓库进行的，只有在`git push`之后远程仓库才会有相应变化**
