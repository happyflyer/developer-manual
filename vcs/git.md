# [git](https://www.liaoxuefeng.com/wiki/896043488029600)

## 1. 全局配置

```bash
git config --global user.name "your_name"
```

```bash
git config --global user.email "your_email@example.com"
```

- 提交时转换为 `LF`，检出时不转换

```bash
git config --global core.autocrlf input
```

- 拒绝提交包含混合换行符的文件

```bash
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
