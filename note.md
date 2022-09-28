#1.协同开发，版本管理
#2.svn(集中式管理) ,git(分布式管理)
#3 git装完，既有客户端，又有服务端，即使一个服务端挂掉，也能把别的客户端选为服务端，正常提供服务
#4 git的工作流程

    -工作区，暂存区，版本库


    工作区：写代码的地方,创建、编写、删除文件的地方
                    | (git add .)
    暂存区：写好代码暂时存放的地方，内存中临时存储
                    |git.commit -m *提交的信息注释
    版本库：本地开发的代码

    从暂存区拿回到工作区或者说取消已缓存的内容 git reset HEAD

    回滚 git checkout . 就是后面写的没了，直接回滚到最后有版本管理的位置
    比如在提交版本库后，又写了t.txt.打了git checkout . t.txt文件没了

    版本回滚：git reset --head 版本号

#5 远程仓库：github，码云，公司内部（gitlab）

#6 安装：一路下一步
#7 右键 --git bash here
#8 git 命令
    -初始化 git init 文件夹名
    -初始化 git init #当前路径全被管理

    -git status 查看状态
    -git add a.txt #把a提交到暂存区
    -git add . 把当前路径下所有的都提交到暂存区
