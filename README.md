# github_use_rule
Git教程

### 该类型的文章在我的blog也有提及

### 配置自己的邮箱和地址
(第一次使用git，必须配置自己的邮箱和地址)

```
git config --global user.name "Gstring-w"
git config --global user.email "Gstring_w@163.com"
```

#### 拉取项目

```
git clone https://github.com/Gstring-w/github_use_rule.git
```
#### 分支管理
(一般在项目开发中会有2个分支（master和develop）)

- 查看分支 （查看远程分支，去掉-r查看本地分支）
```
git branch -r
```

- 接到开发任务，我们需要从远程仓库中拉取我们的分支
```
git fetch origin x(远程分支):y（本地分支）

```

#### Bash的基本操作
```
cd ..
mkdir 
touch index.html // 创建一个文件
pwd  //当前文件目录
ls
rm index.html
rm -r //删除一个文件夹
mv 
reset
clear
history
exit
```
#### git文件配置
```
--global  //全局
--local  //当前
--system // 系统
git config --global user.name 
git config --global user.email
git config --gloabl alias.ci commit //创建一个别名
```
#### git基础

1. 工作目录（Working Directory）
2. （Stage/Index）
3. 资源库（Repository  Git Directory）
4. 远程仓库（remote repository）

#### git仓库2种方法建立

**1. 建立全新的仓库**
```
git init           //初始化一个本地仓库
git remote add origin https://github/.... // 添加一个远程仓库
```

2. clone一个远程仓库
```
git clone https://github/....
```

#### git文件的4种状态

1. Untracked //没有使用git add 之前 使用之后变成 Stage 
2. Unmodify   // 文件使用git add . git commit -m '' 但是文件内容没有修改
3. Modified   //文件已经被修改 没有进行其他操作
4. Staged 

#### 查看文件的状态

```
git status
```

#### 添加文件/目录
```
git add 
```
#### 移除文件/目录 （撤销add）
```
git rm --cached <file> // 删除暂存区文件，工作目录不变
git reset HEAD <file>  
git checkout //操作危险
```
#### 查看文件修改后的差异（工作区和暂存区）
```
git diff //比较工作区和暂存区 
git diff HEAD~n //比较工作区和repo

```

#### .gitignore git忽略的文件
1. 忽略文件中的空行或以（#）号开始的行
2. 可以使用Linux通配符。（*）代表任意多个字符，（？）代表一个字符
3. （！）表示不被忽略
4. （/）表示要忽略此目录下的文件

#### 提交（git commit）
```
git commit -m "描述文字"

```
#### 修订提交
```
发现有的文件提交错了，可以在工作区中修改文件，然后使用git add <file> 然后使用：
git commit -amend
```

#### 撤销提交 
```
git reset --hard HEAD~n
git revert <commit-id> 把提交的所有修改回滚，并生成一个新的提交
```
#### 日志和历史
```
git log 
git log --graph
git reflog
history
```
#### git分支
```
git branch -d
git branch -dr
git branch -r     // 远程分支
git branch -a     // 所有分支
git branch        // 本地分支
git checkout -b  <branch-name> // 创建一个本地分支并切换过去
git merge <branch-name> // 合并指定分支到当前分支
git pull origin <branch-name> // 更新并合并分支
```
#### 开发到一半，需要切换分支

```
git stash    // 将当前的工作目录 储存
git stash list // 查看
git stash apply stash@{0} //提取
```

