touch README.md		//创建

git init		//初始化

git add README.md	//添加

git commit -m "first commit" //commit本地

git remote add orgin https://github.com/fazhongxu/ZxingDemo.git    //远程remote 源头orgin

git push -u origin master

//Push an existing repository from the command line

git remote add orgin https://github.com/fazhongxu/ZxingDemo.git

git pull orgin master //先pull再 push

git push -u origin master

git add . //添加整个目录

git commit -m "commit message"

git clone https://github.com/fazhongxu/MVPDemo.git

//Readme.md不在本地 执行 git push -u orgin master失败

可以通过如下命令进行代码合并 [注：pull=fetch+merge]

git pull --rebase origin master

git remote rm origin //移除现有仓库地址

![image](https://imageUrl)           //![image] (url)  README 里面添加图片 把括号里面的imageUrl替换为自己的图片所在的地址就可显示了

git status //查看文件当前管理状态

git 更新.gitignore文件 

vim .gitignore 编辑好要忽略的文件之后保存

git rm -r --cached .   //注意有.        清除缓存区

git add .

git commit -m "update gitignore"

git branch //查看分支

git checkout <name> //拉取分支

git tag v1.0.0 // tag v1.0.0

git push origin v1.0.0 // tag push 

git pull

git push

git stash 正在工作的项目代码 暂存

git stash list 列出存储的代码

git stash pop 出栈第一个 会删除存储的对应出栈的代码

git stash apply stash@{index} 出栈 不会删除存储的对应出栈的代码 index 为 git stash list 列出的索引

git reset HEAD~ 撤销commit 
