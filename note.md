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

    -git commit -m '注释，我新增了a' #把暂存区的所有都提交到版本库
    -需要增加作者信息
        git config --global user.email 'you@example.com'
        git config --global user.name 'Your name'

        然后在C:\Users\<你的用户名>\.gitconfig 可以查看信息

    -把 1.txt的新增提交到版本管理后
    -新建2.txt,在1.txt中新增一行
    -git checkout . #恢复到提交版本的位置，
    1.txt是空的，2.txt没有被管理所以不会有变化
    如果修改后代码已经git add . 那么不会被回滚

    -git log #查看版本管理的日志
    -git reset --hard 版本号

    -get rest . 把暂存区的东西放回工作区

#红色表示未被管理
#绿色表示提交到暂存区了

#忽略文件
    -空文件夹不被管理
    -指定某些文件或文件夹不被git管理
    -在项目根路径，跟.git文件夹一个路径，新建.gitignore在里面配置
        windows中新建一个.gitignore.
    -语法：
        #号是注释，没有用
        文件夹名字，表示文件夹忽略，不被管理
        例如 .gitignore. 里面输入 note.md 那就表示忽略note文件
            .gitignore. 里面输入 c 那就表示忽略c文件夹
        /dist 表示根路径下的dist文件夹，不被管理
        *.py  表示有后缀名号的文件都被忽略
        *.log* 表示忽略log文件

# 分支操作
    -查看分支   git branch  查看所有分支，如果是绿色表示在当前分支上

    -创建分支   git branch dev
    -创建并切换到某个分支 git checkout -b dev
    -删除分支   git branch -d dev
    -切换分支   git checkout dev
    -合并分支
