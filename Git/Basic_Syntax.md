# GitHub & Git 常用操作手册
> 日常仓库管理、代码提交、分支协作及端口排查速查

## 一、基础配置
1. **配置用户名**
```bash
git config --global user.name "Your Name"
```
2. **配置邮箱**
```bash
git config --global user.email "your-email@example.com"
```
3. **查看全局配置**
```bash
git config --global --list
```

## 二、仓库初始化与克隆
1. **本地创建空 Git 仓库**
```bash
git init
```
2. **克隆远程 GitHub 仓库**
```bash
git clone 仓库地址
```
3. **克隆仓库并自定义本地文件夹名称**
```bash
git clone 仓库地址 本地文件夹名
```

## 三、文件暂存与提交
1. **查看文件状态**
```bash
git status
```
2. **简洁查看文件状态**
```bash
git status -s
```
3. **添加单个文件至暂存区**
```bash
git add 文件名
```
4. **添加所有修改文件至暂存区**
```bash
git add .
```
5. **提交代码到本地仓库**
```bash
git commit -m "提交备注信息"
```
6. **补充修改到上一次提交（不新增记录）**
```bash
git commit --amend
```

## 四、分支管理
1. **查看本地所有分支**
```bash
git branch
```
2. **查看本地+远程所有分支**
```bash
git branch -a
```
3. **新建分支**
```bash
git branch 分支名
```
4. **新建并直接切换到新分支**
```bash
git checkout -b 分支名
```
5. **切换已有分支**
```bash
git checkout 分支名
```
6. **删除本地分支**
```bash
git branch -d 分支名
```
7. **强制删除本地分支**
```bash
git branch -D 分支名
```

## 五、远程仓库拉取与推送
1. **拉取远程仓库最新代码**
```bash
git pull
```
2. **拉取指定远程分支代码**
```bash
git pull 远程仓库名 分支名
```
3. **推送本地代码到远程仓库**
```bash
git push
```
4. **首次推送并关联远程分支**
```bash
git push -u 远程仓库名 分支名
```
5. **强制推送（谨慎使用）**
```bash
git push --force
```

## 六、分支合并
1. **将指定分支合并到当前分支**
```bash
git merge 待合并分支名
```

## 七、撤销与版本回退
1. **撤销单个文件暂存**
```bash
git reset HEAD 文件名
```
2. **撤销全部文件暂存**
```bash
git reset HEAD .
```
3. **版本回退（保留本地文件修改）**
```bash
git reset --soft HEAD^
```
4. **版本回退（清空本地所有修改，高危操作）**
```bash
git reset --hard HEAD^
```
5. **放弃工作区所有未提交修改**
```bash
git checkout -- .
```

## 八、查看提交日志
1. **查看完整提交日志**
```bash
git log
```
2. **精简单行日志**
```bash
git log --oneline
```
3. **查看所有操作记录（恢复丢失提交）**
```bash
git reflog
```

## 九、远程仓库管理
1. **查看已关联的远程仓库**
```bash
git remote -v
```
2. **关联新的远程仓库**
```bash
git remote add 远程仓库名 仓库地址
```
3. **修改远程仓库地址**
```bash
git remote set-url 远程仓库名 新仓库地址
```
4. **解除远程仓库关联**
```bash
git remote remove 远程仓库名
```

## 十、临时储藏代码
1. **储藏当前未提交的修改**
```bash
git stash
```
2. **查看所有储藏记录**
```bash
git stash list
```
3. **恢复最近一次储藏（保留储藏记录）**
```bash
git stash apply
```
4. **恢复并删除最近一次储藏**
```bash
git stash pop
```
5. **清空所有储藏记录**
```bash
git stash clear
```

## 十一、Windows 端口查询命令
1. **查看所有端口及对应进程**
```bash
netstat -ano
```
2. **仅查看监听状态端口**
```bash
netstat -ano | findstr LISTENING
```
3. **查询指定端口占用情况**
```bash
netstat -ano | findstr "端口号"
```
4. **根据 PID 查看进程名称**
```bash
tasklist | findstr "PID编号"
```
5. **强制结束占用端口进程（管理员权限）**
```bash
taskkill /F /PID PID编号
```

## 十二、重要注意事项
1. `git reset --hard`、`git push --force` 为高危命令，执行前务必确认，防止代码丢失。
2. 多人协作时，提交代码前先执行 `git pull` 同步远程最新内容，避免冲突。
3. 提交备注尽量简洁规范，方便后续版本追溯与问题排查。
4. 端口相关命令建议在管理员 CMD 中运行，权限不足会导致执行失败。

