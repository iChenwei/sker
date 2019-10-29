<center><h1>Git & GitHub笔记</h1></center>
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

4. git命令

