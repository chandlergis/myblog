## 使用git的一些场景
### 导入项目
这个很简单
```
git clone 
```
### 添加修改
```
git add .
git commit -m "Add some code"
```
添加修改前可以看下状况
```
git status
```
### 保存项目
```
git push 
```
### 新建分支
```
git branch test
git checkout test
git checkout -b test
```
### 合并分支到主分支
 确保主分支是最新的
首先，切换到你的主分支（这里假设主分支名为main，在一些仓库中可能是master）：
```
git checkout main
```
然后，从远程仓库拉取最新的主分支内容，确保你本地的主分支是最新的：
```
git pull origin main
```
2. 合并分支
现在，主分支已经是最新的了，你可以将目标分支（假设名为feature-branch）合并到当前的主分支中。执行以下命令：
```
git merge feature-branch
```
这个命令会将feature-branch分支的更改合并到当前分支（这里是main）。

3. 解决可能出现的合并冲突
如果合并过程中出现冲突，Git会停止合并并要求你手动解决这些冲突。你可以通过查看Git的输出信息找到冲突文件，然后在编辑器中打开它们，寻找标记为冲突的部分（通常会被<<<<<<<、=======和>>>>>>>所包围），手动解决这些冲突。

解决冲突后，你需要重新添加这些文件到暂存区，并继续合并过程：
```
git add .
git commit
```
这会打开一个编辑器让你输入合并提交的信息。保存并关闭编辑器会完成合并提交。

4. 推送更改到远程仓库
合并完成后，你可以将更改推送到远程主分支：
```
git push origin main
```
