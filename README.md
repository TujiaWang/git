# git常用命令


初始化一个Git仓库：git init

添加文件到git仓库：git add <file1> <file2> ...

把文件提交到仓库:git commit -m <message>

查看命令历史：git reflog

版本回退：git reset --hard commit_id

查看分支：git branch

创建分支：git branch <name>

切换分支：git checkout <name>

创建+切换分支：git checkout -b <name>

合并某分支到当前分支：git merge <name>

删除分支：git branch -d <name>

把当前工作现场“储藏”起来，等以后恢复现场后继续工作：git stash

工作现场：git stash list

恢复的同时把stash内容也删了：git stash pop

恢复某一个工作现场：git stash apply stash@{0}

丢弃一个没有被合并过的分支，强行删除：git branch -D <name>

打标签：git tag <name>

查看所有标签：git tag

对某次commit id打标签：git tag <name> commit_id

合并分支解决冲突：1.git add    2.git rebase --continue



.gitignore只能忽略原来没有被跟踪的文件，因此跟踪过的文件是无法被忽略的。因此在网页上可以看到target等目录的存在。
解决方法就是先把本地缓存删除（改变成未track状态），然后再提交:
git rm -r --cached .
git add .
git commit -m ‘update .gitignore’




feat：新功能
fix：修复bug
doc：文档改变
style：代码格式改变
refactor：某个已有功能重构
perf：性能优化
test：增加测试
build：改变了build工具 如 grunt换成了 npm
revert：撤销上一次的commit
