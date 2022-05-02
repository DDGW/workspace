### 基础Linux命令

```
1. clear：清除屏幕 快捷键ctrl+l
2. echo 'test content':往控制台输出信息
   echo'test content'>test.txt
3. ll(L小写)：将当前目录下的子文件&子目录平铺在控制台
   ll -a(查看隐藏目录)
4. find目录名：将对应目录下的子孙文件&子孙目录平铺在控制台
5. find目录名-type f：将对应目录下的文件平铺在控制台
6. rm文件名：删除文件
7. mv源文件 重命名文件：重命名
8. cat文件的url:查看对应文件的内容
9. vim文件的url(在英文模式下)
   按i进插入模式进行文件的编辑
   按esc键&按:键进行命令的执行
   q! 强制退出（不保存）
   wq 保存退出
   set nu 设置行号
   yy是复制 p是粘贴(退出编辑状态)
10. ctrl+insert 复制 shift+insert粘贴
11. mkdir 文件夹名  添加文件夹
```



![image-20220502112600827](C:\Users\asus\AppData\Roaming\Typora\typora-user-images\image-20220502112600827.png)

### 设置用户签名

```
git config --global user.name 用户名
git config --global user.email 邮箱
git config --list 查看
```

### 初始化本地库

```
git init
```

### 查看当前目录下的文档

```
ll(小写的L)
ll -a(隐藏文件)
```

### 查看本地库状态

```
git status
```

### 编辑文件

```
vim 文件名
按i编辑模式
按esc键&按:键进行命令的执行
	q! 强制退出（不保存）
   	wq 保存退出
   	set nu 设置行号
   	yy是复制 p是粘贴(退出编辑状态)

```

### 查看文件内容

```
cat 文件名
```

### 添加暂存区

```
git add 文件名
```

### 删除暂存区文件

```
git rm --cached 文件名
从暂存区删除，工作区还存在文件
```

### 添加本地库

```
git commit -m "日记信息" 文件名
```

### 编辑文件需要再次添加暂存区提交本地库

### 历史版本

```
1. 查看历史版本
git reflog 查看版本信息
git log 查看版本详细信息

2. 版本穿梭
git reset --hard 版本号
```

### 分支操作

```
git branch 分支名     创建分支
git branch -v        查看分支
git checkout 分支名   切换分支
git merge 分支名      把指定的分支指定到当前分支上
冲突合并：合并分支时，两个分支在同一个文件的同一个位置有两套完全不同的修改。Gt无法替我们决定使用哪一个。必须人为决定新代码内容。(手动打开合并文件修改)->(添加暂存区)->(提交本地库,这时不带文件名)
```

### Git Hub操作

![image-20220502120758179](C:\Users\asus\AppData\Roaming\Typora\typora-user-images\image-20220502120758179.png)

```
clone不需要登录账号 
clone会做如下操作。1、拉取代码。2、初始化本地仓库。3、创建别名
push需要登录账号(邀请合作者)
邀请：仓库settin->manage access->invite search->pending invite
```

### SSH免密登录

```
ssh-keygen -t rsa -C GitHub账号邮箱
在指定目录生成文件
复制公钥->用户settings->SSH keys
```

### push整个文件夹

```
git init
git add .
git commit -m “你的提交信息”
git push 远程库地址名 远程分支名
```

### 修改并push某个文件夹下的文件

```
mkdir updatafile 创建文件夹
cd 文件名(当前路径下)
cd ./文件夹名/文件名(当前兄弟文件夹下文件)

git add ./文件夹名/文件名
git commit -m "你的提交信息"
git push xxx xxx
(可以单独修改某一文件，只需要add路径正确)
```

### 直接修改文件夹下的全部文件

```
git add ./文件夹名
git commit -m "你的提交信息"
git push xxx xxx
```

### VSCode

```
问题：failed unable to access ‘***.git/‘:OpenSSL SSL_read: Connection was reset, errno 10054

解决：终端输入 git config --global http.sslVerify "false"
```







