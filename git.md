touch README.md		//创建

git init		//初始化

git add README.md	//添加

git commit -m "first commit" //commit本地

git remote add orgin https://github.com/fazhongxu/ZxingDemo.git    //远程remote 源头orgin

git push -u orgin master

//Push an existing repository from the command line

git remote add orgin https://github.com/fazhongxu/ZxingDemo.git
git push -u orgin master

git add . //添加整个目录

git commit -m "commit message"

git clone https://github.com/fazhongxu/MVPDemo.git

//Readme.md不在本地 执行 git push -u orgin master失败

可以通过如下命令进行代码合并 [注：pull=fetch+merge]

git pull --rebase origin master
