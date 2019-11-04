git config -global user.name "名字"  // 名字
git config -global user.email "1@1.com"

mkdir 空文件夹 // 建一个空文件夹
pwd // 查看当前目录
git init // 建仓库

git add test1.txt  // 提交修改的文件1
git add test2.txt  // 提交修改的文件2
git commit -m "说明"  // 对提交的文件做说明
git diff [test1.txt]  // 可查看具体修改内容,在add之前查看  如出现(END) 点击q退出
git status // 可查看当前状态
git log [--pretty=oneline]   // 可查看版本更新记录[版本号]
git reset --hard head^ // 回退前一个版本 Head表示当前版本号
git reset --hard 版本号 // 回退特定版本号
git reflog  // Git 记录你操作的每一次命令
git diff head -- rest1.txt  // 把当前版本和更改后文件作比较
git rm test1.txt  // 从版本库删除某文件 之后也得提交 git commit
ls -al ~/.ssh  // 查看本地是否有ssh密钥文件
ssh-keygen -t rsa -C "自己的@qq.com"  // 如果没有可以新建，会生成id_rsa和id_rsa.pub两个文件，之后复制id_rsa.pub(公钥)文件中内容到GitHub中
git remote add origin(远程库名，可以自己起名字) git@github.com:GitHub用户名/learnGit.git //添加远程仓库  
(码云：git remote add origin git@gitee.com:dy/learngit.git)
git remote  // 查看远程信息
git remote rm origin  // 删除关联的远程库

git push [-u](第一次推送需要加-u) origin(远程库) master(本地分支) // 发布到自己的GitHub
git clone git@github.com:duXueZha/design-resource.git // 往本地克隆

git checkout -b dev(分支名)  // 新建分支dev，并切换到该分支
git branch name // 新建分支dev
git branch  // 查看分支
git checkout master/dev   // 切换分支
git pull origin(远程库) dev(本地库) // 拉取远程库到某分支
git merge master // 当前为dev分支，该命令合并master到当前分支
git reset --hard head // 如果 状态为(dev|MERGING), 退出该状态到head当前分支
git branch -d dev  // 删除该分支
git branch -D dev // 强行删除该分支

git tag tagname(随便起)  // 建立标签
git tag  // 查看标签
git show tagname   // 查看某个标签的具体操作
git tag -d tagname  // 删除标签
git push origin tagname/--tags   // 把标签推送到远程服务(--tags表示推送全部标签)

Git的官方网站：http://git-scm.com
Git有意思：https://git-scm.com/book/zh/v2