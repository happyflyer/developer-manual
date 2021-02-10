# [Git 使用](https://www.liaoxuefeng.com/wiki/896043488029600)

## 1. 全局配置

```bash
git config --global user.name "your_name"
```

```bash
git config --global user.email "your_email@example.com"
```

```bash
# 提交时转换为LF，检出时不转换
git config --global core.autocrlf input
```

```bash
# 拒绝提交包含混合换行符的文件
git config --global core.safecrlf true
```

## 2. 日常使用

```bash
git clone git@github.com:github/gitignore.git
```

```bash
git init
```

```bash
git add doc.txt
```

```bash
git commit -m "add doc.txt"
```

```bash
git status
```

```bash
git diff doc.txt
```

## 3. 日志和切换

```bash
git log
```

```bash
git log --pretty=oneline
```

```bash
git log --oneline --graph --decorate --all
```

```bash
git reflog
```

```bash
git reset --hard commit_id
```

## 4. 撤销和丢弃

### 4.1. 撤销暂存区的修改

```bash
git reset HEAD doc.txt
```

### 4.2. 丢弃工作区的修改

```bash
git checkout -- doc.txt
```

- `doc.txt` 自修改后还没有被放到暂存区，撤销修改就回到**和版本库一模一样的状态**。
- `doc.txt` 已经添加到暂存区后，又作了修改，撤销修改就回到**添加到暂存区后的状态**。

## 5. 删除和恢复

### 5.1. 删除工作区和版本库的文件

```bash
rm doc.txt
git rm doc.txt
git commit -m "del doc.txt"
```

### 5.2. 删除了工作区的文件后，从版本库恢复

```bash
rm doc.txt
git checkout -- doc.txt
```

## 6. 分支

```bash
git checkout -b dev
```

```bash
git checkout dev
```

```bash
git checkout master
```

```bash
git merge dev
```

## 7. 关联远程仓库

```bash
ssh-keygen -t rsa -C "your_message"
```

将公钥 `~/.ssh/id_rsa.pub` 添加到 github / gitlab / gitee / .. 账户的 SSH 公钥。

```bash
ssh -T git@github.com
```

```bash
git remote add origin git@server_name:username/repo_name.git
```

```bash
git remote set-url origin git@server_name:username/repo_name.git
```

```bash
git remote
```

```bash
git remote -v
```

## 8. [拉取和推送](https://www.cnblogs.com/xiaopangjr/p/7469687.html)

### 8.1. pull

```bash
git pull origin next:master
```

pull = fetch + merge

> git pull <远程主机名> <远程分支名>:<本地分支名>

```bash
git push -u origin master
```

### 8.2. push

```bash
git push origin master
```

```bash
git push origin --all
```

```bash
git push origin --tags
```

> git push <远程主机名> <本地分支名>:<远程分支名>

## 9. 标签

```bash
git tag 0.1.0
```

```bash
git checkout 0.1.0
```

```bash
git tag -d 0.1.0
git push origin :refs/tags/0.1.0
```
