git config -global user.name "名字"  // 名字
git config -global user.email "1@1.com"

mkdir 空文件夹 // 建一个空文件夹
pwd // 查看当前目录
git init // 建号仓库

git add test1.txt  // 提交修改的文件1
git add test2.txt  // 提交修改的文件2
git commit -m "说明"  // 对提交的文件做说明
git diff [test1.txt]  // 可查看具体修改内容  如出现(END) 点击q退出
git status // 可查看当前状态
git log [--pretty=oneline]   // 可查看版本更新记录[版本号]
git reset --hard head^ // 回退前一个版本 Head表示当前版本号
git reset --hard 版本号 // 回退特定版本号
git reflog  // Git 记录你操作的每一次命令
git diff head -- rest1.txt  // 把当前版本和更改后文件作比较