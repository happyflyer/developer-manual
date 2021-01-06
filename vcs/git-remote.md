# git

## 1. 关联远程仓库

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

## 2. [拉取和推送](https://www.cnblogs.com/xiaopangjr/p/7469687.html)

### 2.1. pull

```bash
git pull origin next:master
```

pull = fetch + merge

> git pull <远程主机名> <远程分支名>:<本地分支名>

```bash
git push -u origin master
```

### 2.2. push

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

## 3. 标签

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
