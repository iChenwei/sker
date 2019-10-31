<center><h1>Git & GitHub笔记</h1></center>
<p align="right">电气信息系 计算机科学与技术17级 陈巍</p>

1. 安装 Git && 申请 GitHub账号，并创建一个仓库repository

2. 本地与GitHub连接

    * 打开ssh使用命令`ssh-keygen`生成ssh密钥

    * 使用命令：

        `ssh-keygen`

    * 到`.ssh`目录下找到`id_rsa.pub`,打开并复制内容

    * 将复制好的内容粘贴到 Github 的个人账号中 Setting页面的`SSH and GPG keys`选项中的`SSH keys`中

3. 初始化文件夹并与GitHub建立链接

    * 建立文件夹，用来和GitHub建立连接（所有操作都在建立的文件夹的路径下执行）

    * 使用命令：

        ​	`git init`

    * 生成了一个文件夹`.git`，它是`git本地仓库`

    * 将建立的文件夹和GitHub对应的仓库建立链接

        * 复制远程仓库的地址

            点击`clone of download` -> `Clone With HTTPS`

        * 使用命令将本地仓库和远程仓库建立连接

            `git remote add origin https://github.com/iChenwei/sker.git `

        * 使用命令拉取远程仓库的文件

            `git pull origin master`

    * 当我们在当前目录下看到创建仓库时默认创建的`README.md`时，就说明链接成功

4. 编辑本地git信息

    `git config --global user.name “iChenwei”`

    `git config --global user.email “willchan1020@gmail.com”`

5. 请自行了解git原理

6. git相关命令

    - 查看当前git状态

        `git status`

    - 文件追踪与准备提交

        - 追踪所有更改过的文件，并改为“准备提交状态”

            `git add .`

        - 追踪某个更改过的文件，并改为“准备提交状态”

            `git add [filename]`

            当文件首次被改为“准备提交状态”，就视为`追踪`

        - 解除对某个文件的追踪

            `git rm --cached [filename]`

    - 文件提交与相关备注信息

        - 提交到本地仓库并添加备注

            `git commit -m [updated message]`

        - 提交到本地仓库并添加备注

            `git commit`

            会进入到与本次提交有关的文件编辑页面，从一第行开始添加备注

    - 将本地仓库的文件提交到相关联的GitHub中

        `git push -u origin master`

    - 忽略、不提交部分文件

        首先，在仓库目录下创建文件`.gitignore`

        然后，使用文本编辑器对`.gitignore`进行编辑
    
        最后，在`.gitignore`的编辑页面，将需要`忽略/不提交`的文件写到里面，每个文件一行
    
        注意：忽略文件之前，要解除对文件的追踪