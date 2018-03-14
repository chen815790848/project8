# Git学习
## 首先选用一个远程仓库，这里选的是github作为远程仓库
注册账号，建立仓库project8，会出现运程仓库的url
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



## 删除分支
        git branch -d dev1
或者

        git branch -D dev1
强制删除

        git push origin :dev1
远程仓库删除操作


## 待定
## 


### 其他
#### 直接使用git pull和git push的设置,两种方式：意思是默认将本地的dev分支的推送到origin/dev
        git branch --set-upstream-to=origin/dev dev
        git branch --set-upstream dev origin/dev
        git config --global push.default matching