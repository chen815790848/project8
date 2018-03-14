# Git学习
## 首先选用一个托管平台，这里选的是github作为远程托管平台
注册账号，建立仓库project8，会出现运程仓库的url  
托管平台有gitlab,bitbucket,开源中国代码托管，coding.net
## 在本地新project8本地仓库，如下操作
        mkdir project8
        cd project8
        git init
        echo "# project8" >> README.md
        git add README.md
        git commit -m "first commit"

        git remote add origin [url]
        git push -u origin master
这样就可以把README.md上传到远程仓库

也可以直接克隆远程仓库

        git clone [url]

## 添加新分支的 dev1
        git branch dev1
        git branch
        git branch -r
        git push origin dev1

## 切换分支 从master到dev1
        git checkout dev1
或者

        git checkout -b dev1

这是新建并切换到分支dev1

## 合并分支

        git merge [branch]
合并到当前分支

## 解决冲突

        #将dev2合并到dev1，dev1是当前分支
        git merge dev2
        #会有提示Please enter a commit message to explain why this merge is necessary.

        #然后提交到远程仓库
        git push origin dev1



## 删除分支
        git branch -d dev1
或者

        git branch -D dev1
强制删除

        git push origin :dev1
远程仓库删除操作
### 删除本地文件／文件夹
                git rm [file]
                git rm -r [fold]/

## 查看文件修改前后差异
        git diff [filename]
直接

        git diff

## 签出 checkout 比较**危险**的操作
## pull操作，可以从远程仓库取回分支，与本地分支合并
                git pull origin dev1
相当于

                git fetch origin
                git merge origin/dev2


## 待定

## 


### 其他
#### 直接使用git pull和git push的设置,两种方式：意思是默认将本地的dev分支的推送到origin/dev
        git branch --set-upstream-to=origin/dev dev
        git branch --set-upstream dev origin/dev
        git config --global push.default matching

#### 远程分支，远程跟踪分支，跟踪分支
远程跟踪分支是在本地的只读的记录远程分支状态的分支，其指向用户无法移动，当使用git fetch等指令时其指向会依照远程仓库自动移动。跟踪分支是从远程跟踪分支上生成的本地分支

#### 相关图片  

![](https://user-gold-cdn.xitu.io/2017/9/8/5183149719f6e7f7652ece27e6ef2c5e?imageslim)
![](https://user-gold-cdn.xitu.io/2017/9/8/8c67d6a03df64fcde8cac7d3ed0d92e9?imageView2/0/w/1280/h/960/ignore-error/1)
![日常记住的几个命令](https://user-gold-cdn.xitu.io/2017/9/8/c65250b040f69c54c515c0aea36f1d1f?imageslim)
日常记住的几个命令

end.  
...


