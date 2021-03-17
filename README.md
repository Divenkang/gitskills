# gitskills

一些常规操作：

- 配置用户名

  ```
  $ git config --global user.name "yourname"
  ```

- 配置邮箱

  ```
  $ git config --global user.email "youremil@example.com"
  ```

- 创建SHH Key：

  ```
  $ shh-keygen -t rsa -C "youremail@example.com"
  ```

  在主目录里找到 **.shh** 目录，里面有 **id_rsa（私钥）**  和 **id_rsa.pub（公钥）**

- 在本地仓库运行以下命令，关联远程仓库

  ```
  $ git remote add origin git@github.com:<yourIDname>/<projectname>.git
  ```

- 把本地库的所有内容推送到远程库上：

  ```
  $ git push -u origin master
  ```

  把本地库的内容推送到远程，用`git push`命令，实际上是把当前分支`master`推送到远程。

  由于远程库是空的，我们第一次推送`master`分支时，加上了`-u`参数，Git不但会把本地的`master`分支内容推送的远程新的`master`分支，还会把本地的`master`分支和远程的`master`分支关联起来，在以后的推送或者拉取时就可以简化命令。

- ```
  $ git remote -v # 查看远程库信息
  ```

## 从远程克隆，更新文件后提交

- 从远程仓库克隆

  ```
  $ git clone git@github.com:<yourIDname>/<projectname>.git
  ```

- 合并

  ```
  $ git pull
  ```

- 添加

  ```
  $ git add -A # -A 表示所有修改文件
  # 或者单独传
  $ git add filename
  ```

- commit

  ```
  $ git commit -m "修改了什么内容" # 修改注释会添加到所有add的文件中
  ```

- push

  ```
  $ git push
  ```

  

git