#### 建立github本地关联链接

##### 	1、安装git【百度】

```python
sudo apt-get install git
```

##### 	2、创建SSH KEY

​		第一步：在用户主目录下，看看有没有.ssh目录，如果有，再看看这个目录下有没有`id_rsa`和`id_rsa.pub`这两个文件，如果已经有了，可直接跳到下一步。如果没有，在命令窗口输入：

```bash
ssh -keygen -t rsa -C "youremail@example.com"
```

这里的youremail@example.com是你github账号的邮箱

​		第二步：将新生成的key添加到ssh-agent中

```bash
ssh-add ~/.ssh/id_rsa
```

​		第三步：登陆GitHub，打开“settings”，“SSH Keys”页面，点“Add SSH Key”，填上任意Title，在Key文本框里粘贴`id_rsa.pub`文件的内容，点“Add Key”，你就应该看到已经添加的Key。

##### 	3、建立链接

```bash
git remote add study git@github.com:yangjunXTU/study.git
```

现在就可以正常的使用git命令管理github项目了