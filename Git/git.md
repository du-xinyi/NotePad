# 安装与配置
## 安装
- Ubuntu
```
sudo apt-get install libcurl4-gnutls-dev libexpat1-dev gettext
libz-dev libssl-dev
sudo apt-get install git
```
- Windows
安装包下载地址: https://gitforwindows.org/
## 配置
```
git config [<options>] [<setting>]
```
> `<options>`: 可选的命令行选项
> > `--system`: 配置系统级别设置，适用于所有用户和所有仓库，位于/etc/gitconfig文件中
> > `--global`: 配置用户级别设置，仅适用于该用户，位于~/.gitconfig文件中
> > `--local`: 配置仓库级别设置，仅适用于该仓库，位于.git/config文件中(默认)
> > `--list`: 列出当前的配置设置
> > > `git config --list # 获取默认配置，如果当前地址中仓库信息不存在，则查看全局，最后再读取系统配置`
> > > `git config --local --list # 本地仓库配置 高优先级`
> > > `git config --global --list # 全局用户配置 中优先级`
> > > `git config --system --list #系统配置 低优先级`
> > 
> > `--get`: 获取特定的配置设置的值
> > `--get-all`: 获取特定的配置设置的所有值
> > `--replace-all`: 替换特定的配置设置的所有值
> > `-add`: 添加特定的配置设置的值
> > `--unset`: 删除特定的配置设置的值
> > `--unset-all`: 删除特定的配置设置的所有值
> > `--edit`: 打开特定的配置文件以进行编辑
> > `<setting>`: 需要进行配置的设置
> 
> `<setting>`: 可配置的设置
> > `user.name`和`user.email`: 用户名和电子邮件地址，用于标识每次提交的作者，以便可以追踪更改的历史记录
> > > `git config --global user.name "your name"`
> > > `git config --global user.email "your.email@example.com"`
> >
> > `core.editor`: 编辑器，用于写入提交说明等内容
> > `merge.tool`和`diff.tool`: 差异和合并工具，用于合并冲突的工具
> > `push.default`: 推送默认行为，推送到远程仓库时的默认行为
> > `core.excludesfile`: 忽略文件，不希望提交到版本控制的文件的列表
> > `alias.[name]`: 别名，为常用命令定义别名
> > > `git config --global alias.co checkout`
> >
>
# 
# 创建仓库
## 初始化仓库
```
git init <repository-name>
```
> `<repository-name>`: git存储库的名称。如果不指定，则默认为当前目录的名称
> 
## 克隆项目
```
git clone [<options>] <url>
```
> `<options>`: 可选的命令行选项
> > `-b [branch-name]`或`--branch [branch-name]`: 克隆指定的分支，而不是默认的主分支
> > `--depth [depth-number]`: 克隆仅最近的N个提交。
> > `-v`或`--verbose`: 显示详细的克隆过程信息
> > `--progress`: 显示克隆进度信息
> 
> `<url>`: 希望克隆的远程存储库的链接
# 
# 提交与修改
## 添加文件到暂存区
```
git add [<options>] <file>
```
> `<options>`: 可选的命令行选项
> > `-p`或`--patch`: 通过交互式方式选择要添加的每个文件的哪些部分
> > `-u`或`--update`: 仅将已跟踪的文件添加到暂存区，并忽略已删除的文件
> > `-A`或`--all`: 将所有更改(包括已删除的文件)添加到暂存区。
> > `--ignore-errors`: 如果有文件因某种原因无法添加到暂存区，则继续处理其他文件而不停止整个操作
> > `--no-all`: 防止添加所有文件，仅添加明确列出的文件。
>
> `<file>`: 添加到缓存区的文件名
> > `git add <file1> <file2> ... # 添加一个或多个文件到暂存区`
> > `git add <direction> # 添加指定目录到暂存区，包括子目录`
> > `git add . # 添加当前目录下的所有文件到暂存区`
> 
## 查看仓库当前的状态，显示有变更的文件
```
git status [<options>]
```
> `<options>`: 可选的命令行选项
> > `-s`或`--short`: 简洁输出模式，只显示文件名称和状态
> > `-b`或`--branch`: 在状态信息中显示分支名称
> > `--porcelain`: 稳定输出模式，便于解析。
> > `--untracked-files`: 仅显示未跟踪的文件。
> > `--untracked-files=<mode>`: 控制如何显示未跟踪的文件。可用的模式有
> > > - no: 忽略未跟踪的文件
> > > - normal: 显示未跟踪的文件
> > > - all: 显示所有未跟踪的文件
> >
> 
## 比较文件的不同
```
git diff [<options>] <file>
```
> `<options>`: 可选的命令行选项
> > `--cached`: 比较缓存区与HEAD版本之间的差异
> > `--staged`: 等价于`--cached`
> > `--no-index`: 比较两个不同的目录，而不是索引与工作目录的差异
> > `-b`: 忽略空白字符的差异，但仍然考虑换行符的差异
> > `-w`: 忽略所有空白字符的差异，包括换行符
> > `--color`: 在输出中使用颜色显示差异
> > `--name-only`: 只显示文件名，而不是实际的差异
> > `--stat`: 显示文件修改的摘要信息，如文件大小，行数和修改数量
> > `--patience`: 使用“耐心算法”来生成更具可读性的差异
> `<file>`: 需要进行对比的文件名
> 
## 提交暂存区到本地仓库
```
git commit [<options>] <message>
```
> `<options>`: 可选的命令行选项
> > `-m`或`--message`: 指定提交消息
> > `-a`或`--all`: 自动暂存所有已跟踪的文件的更改，不需要执行`git add`命令，直接提交
> > `-e`或`--edit`: 打开默认文本编辑器，以便在提交之前编辑提交消息
> > `--amend`: 修改最后一次提交
> > `--no-verify`: 不要运行钩子(git在某些事件发生时自动运行的脚本)
> `message`: 备注信息
注:
> 在Linux系统中，`message`信息使用单引号`'`，Windows系统，`message`信息使用双引号`"`
## 回退版本
```
git reset [<options>] <commit> <file>
```
> `<options>`: 可选的命令行选项
> > `--soft`: 重置HEAD指针，但保留暂存区和工作目录中的所有内容
> > `--mixed`: 重置HEAD指针和暂存区，但保留工作目录中的所有内容(默认)
> > `--hard`: 重置HEAD指针、暂存区和工作目录，丢弃所有未提交的更改
>
> `<commit>`: 重置缓存区的版本
> > - `HEAD`或`HEAD~0` 当前版本(默认)
> > - `HEAD^`或`HEAD~1` 上一个版本
> > - `HEAD^^`或`HEAD~2` 上上一个版本
> > - `HEAD^^^`或`HEAD~3` 上上上一个版本
> > - 以此类推
>
> `<file>`: 缓存区中指定的文件
> > `git reset --hard origin/master # 将本地的状态回退到与远程相同`
>
## 将文件从暂存区和工作区中删除
```
git rm [<options>] <file>
```
> `<options>`: 可选的命令行选项
> > `-n`或`--dry-run`: 显示将执行的操作，但不会实际删除文件。
> > `-f`或`--force`: 强制删除文件，即使它被标记为只读或未合并的
> > `-r`: 递归删除目录及其内容。
> > `--cached`: 只从git仓库中删除文件，不会从工作目录中删除文件。
>
> `<file>`: 需要删除的文件或目录
>
## 移动或重命名工作区文件
```
git mv <source> <destination>
```
> `<source>`是要移动或重命名的文件或目录
> `<destination>`是文件或目录的新路径和名称
> 如果要重命名文件，`<destination>`只需要包含新的文件名
>
#
# 提交日志
## 查看历史提交记录
```
git log [<options>]
```
> `<options>`: 可选的命令行选项
> > `-p`: 显示每个提交的差异
> > `-<number>`: 仅显示最近的`<number>`次提交
> > `--since=<date>`: 仅显示指定日期`<date>`之后的提交
> > `--until=<date>`: 仅显示指定日期`<date>`之前的提交
> > `--author=<pattern>`: 仅显示指定作者`<pattern>`相关的提交
> > `--grep=<pattern>`: 仅显示包含指定模式<pattern>的提交
> > `--no-merges`: 仅显示没有合并的提交
> > `--graph`: 以图形化方式显示提交历史
> > `--pretty`: 定义提交信息的显示格式
> > `--decorate`: 在输出中包含分支和标签的信息
>
## 查看指定文件的历史修改记录
```
git blame [<options>] <file>
```
> `<options>`: 可选的命令行选项
> > `-L <start>,<end>`: 只显示指定行范围`<start>`到`<end>`的代码历史
> > `-M`: 启用代码移动检测
> > `-C`: 启用代码复制检测
> > `-C -C`: 更加严格的代码复制检测
> > `-w`: 忽略空格和空白变化
> > `-wM`: 忽略空格和空白变化，并启用代码移动检测
> > `-wC`: 忽略空格和空白变化，并启用代码复制检测
> > `-wC -wC`: 更加严格的忽略空格和空白变化，并启用代码复制检测
> > `-f`: 显示完整的文件路径和文件名
> > `-p`: 显示结果以`patch`的格式输出
> > `-t`: 显示结果以 tab 分割的格式输出
> > `-s`: 不显示作者名和提交时间
> > `--root`: 显示文件的第一个提交
> > `--incremental`: 显示文件的历史，而不是只显示最后一次修改
>
> `<file>`: 需要查看的文件
>
# 
# 远程操作
## 操作远程仓库
```
git remote [<options>]
```
> `<options>`: 可选的命令行选项
> > `add`: 添加一个新的远程仓库
> > > `git remote add <remote-name> <remote-url>`
> > 
> > `remove`或`rm`: 移除一个远程仓库
> > > `git remote remove <remote-name>`
> > 
> > `show`: 显示当前仓库配置的所有远程仓库
> > `rename`: 修改远程仓库的名称
> > > `git remote rename <old-name> <new-name>`
> > 
> > > `set-url`: 设置远程仓库的URL
> > `git remote set-url <remote-name> <remote-url>`
> > `get-url`: 获取远程仓库的URL
> > > `git remote get-url <remote-name>`
> >
> 
## 从远程获取代码库
```
git fetch [<options>] <remote> <branch>
```
> `<options>`: 可选的命令行选项
> > `-p`或`--prune`: 在获取最新的提交记录后，自动清理已经不存在于远程仓库的引用(分支或标签)
> > `-v`或`--verbose`: 显示详细的获取信息，包括获取了哪些分支和提交记录等
> > `--tags`: 下载远程仓库的标签到本地
> `<remote>`: 远程仓库的名称，默认为`origin`
> `<branch>`: 需要获取的远程分支名称，默认为`refs/heads/*:refs/remotes/<remote>/*`
>
## 下载远程代码并合并
```
git pull [<options>] <remote> <branch>
```
> `<options>`: 可选的命令行选项
> > `--rebase`: 使用`git rebase`而不是`git merge`合并代码，避免产生不必要的合并提交
> > `--no-rebase`: 不要使用`git rebase`。如果本地分支已经存在，`git pull`默认会使用`git merge`
> > `--no-commit`: 在拉取后不要自动创建新的提交，即使远程分支有新提交
> > `--squash`: 将所有拉取的提交压缩为单个提交
> > `--depth <depth>`: 限制拉取历史记录的深度，只获取指定深度`<depth>`以内的提交
> > `--quiet`: 抑制输出，不会显示拉取的提交和更新的分支
> > `--verbose`: 显示详细的输出，包括拉取的提交和更新的分支
> `<remote>`: 远程仓库的名称，默认为`origin`
> `<branch>`: 需要获取的远程分支名称，默认为`refs/heads/*:refs/remotes/<remote>/*`
>
## 上传远程代码并合并
```
git push [<options>] <remote> <branch>
```
> `<options>`: 可选的命令行选项
> > `-u`或`--set-upstream`: 将本地分支与远程分支关联起来，可以使之后的`push`或`pull`操作不用指定分支名
> > `-f`或`--force`: 强制推送，会覆盖其他人的提交记录
> > `--dry-run`: 执行一个模拟的`push`操作，查看会发送哪些数据到远程仓库
> > `--porcelain`: 输出易于解析的格式，便于程序处理
> > `--tags`: 推送标签到远程仓库
> > `--delete`: 删除远程分支或标签
> > `--all`: 推送所有分支到远程仓库
> > `--mirror`: 将本地仓库镜像到远程仓库，包括所有分支和标签，并删除远程仓库上已经不存在的分支和标签
> `<remote>`: 远程仓库的名称，默认为`origin`
> `<branch>`: 要推送的本地分支的名称
> 
#
# 分支管理
## 创建分支
```
git branch [<options>] <branch>
```
> `<options>`: 可选的命令行选项
> > `-r`: 显示远程分支
> > `-a`: 显示所有分支
> > `-d`: 删除分支
> > `-m`: 重命名当前分支
> > `--list`: 列出所有分支
> > `-v`: 显示每个分支的最新提交信息
> > `-vv`: 显示每个分支的详细信息，包括与远程分支的关联信息
> > `--merged`: 列出已经合并到当前分支的分支
> > `--no-merged`: 列出未合并到当前分支的分支
> > `--column[=<options>]`: 使用列格式列出分支，可以通过设置选项`<options>`来自定义列格式
> > > - `--no-column`: 禁用列格式
> > > - `--sort=<key>`: 按指定的关键字排序输出分支
> > > - `--points-at <object>`: 显示指向指定对象的所有分支
> > 
> > `<pattern>...`: 用于模式匹配查找分支
> 
> `<branch>`: 本地分支的名称
> > `git branch # 列出所有分支`
> > `git branch new-branch # 创建分支`
> 
## 切换分支
```
git checkout [<options>] <branch>
```
> `<options>`: 可选的命令行选项
> > `-b`: 创建并切换到新分支
> > `-B`: 创建并切换到新分支，如果同名分支已存在，则先删除原有分支
> > `-l`: 创建新分支时，将其标记为本地分支，即不推送到远程仓库
> > `-t`: 创建新分支并跟踪指定的远程分支
> > `-p`: 提示进行交互式的文件差异修补
> > `--detach`: 暂时切换到某个提交的状态，而不是分支，可以用于查看某个历史版本
> > `--orphan`: 创建一个与当前没有关联的新分支
> `<branch>`: 本地分支的名称
## 合并分支
```
git merge [<options>] <branch>
```
> `<options>`: 可选的命令行选项
> > `-m <message>`或`--message=<message>`: 使用指定的合并消息进行提交
> > `-q`或`--quiet`: 不显示合并进程的进度信息
> > `--no-commit`: 在合并成功后不自动创建提交，留待稍后手动提交
> > `--no-ff`: 始终通过创建新的合并提交来合并分支，而不是通过快进合并
> > `--ff-only`: 只能进行快进合并，如果分支无法快进合并，那么该命令将失败
> > `--abort`: 中止当前正在进行的合并操作
> > `--squash`: 将合并的提交压缩成单个提交，而不是创建新的合并提交
> > `--strategy=<option>`或`--strategy-option=<option>`: 用于指定合并策略和特定的选项`option`
> > > - `recursive`: 自动合并代码，并在无法自动合并时提示用户手动解决冲突(默认)
> > > - `octopus`: 另一种自动合并策略，支持更多的情况
> > > - `subtree`: 一种同时合并多个分支的策略，可以合并两个以上的分支
> > 
> > `--rerere-autoupdate`: 启用`"rerere"`机制，以便在未来的冲突解决中重用先前解决的冲突
> > `-s`或`--signoff`: 将当前用户的签名添加到合并提交的提交信息末尾
> 
> `<branch>`: 需要合并到当前分支的分支名称
>
#
# 标签
```
git tag [<options>] <tag_name>
```
> `<options>`: 可选的命令行选项
> > `-l <pattern>`: 列出匹配给定模式的标签
> > > `git tag -l "v1.*" # 列出所有以 "v1." 开头的标签`
> >
> > `-a <tagname> [-m <message>]`: 创建一个带注释的标签
> > `-d <tagname>`: 删除指定的标签
> > `-f <tagname> [<commit>]`: 将已有标签强制覆盖为新的提交，如果没有指定新的提交，则默认为`HEAD`
> > `-n`: 显示带有标签说明的最新提交的信息
> > `-v`: 显示标签和标签说明，以及最新提交的信息
> `<tag_name>`: 设置的标签名