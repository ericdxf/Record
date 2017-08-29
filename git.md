### 提交代码之后修改ignore无效解决办法  
把某些目录或文件加入忽略规则，按照上述方法定义后发现并未生效，原因是.gitignore只能忽略那些原来没有被追踪的文件，如果某些文件已经被纳入了版本管理中，则修改.gitignore是无效的。<font color="#17da4d">那么解决方法就是先把本地缓存删除（改变成未被追踪状态），然后再提交：</font>  

git rm -r --cached .  
git add .  
git commit -m 'update .gitignore'  
# Sharp标题1
![boy2.jpg](C:\Users\duxiaofeng\Pictures\boy2.jpg)
