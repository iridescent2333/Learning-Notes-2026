### 基本操作
- **git**基础指令，
- **github**基础功能，拷贝clone，提交commit，拉取pull，推送push，代码仓库repository，commitID(仓库操作唯一)，方便ai识别操作，
- **.git**文件夹，初始仓库管理，
- **.gitignore**，node_modules/(存储nodejs依赖包，末尾/代表是目录),.env(存储密钥)，
- 分支**branch**，**main/master**(主干分支)，**feature**(特性分支)，创建分支，合并merge，
- **worktree**，merge conflict，人工决定保留哪个文件，
- git分区，working directory工作区，local repository本地仓库，remote repository远程仓库，fetch，merge，暂存区，
- 仓库管理，
- 交互，**fork复刻**，issue讨论(open未结束，close已解决)，pull request拉取合并请求，
### 团队协作
- **discard**，放弃还未commit的文件更改，未提交，**reset**，把仓库强制回退到某个历史状态，单人使用的分支，还未提交远程仓库，**revert***，生成反向commit抵消某次commit，多人协作的分支，不能强制推送，否则他人代码肯被
- 第一步，fork复刻到自己名下，子项目，然后clone到本地，创建分支，防止冲突，在分支上拓展代码并commit，然后贡献者创建**pull requests**(即**PR**)，管理员审核代码，同意后就合并代码，更新成功，后续需要修改就把母项目同步到feature分支上，在本地解决问题后再PR，
- PR，贡献者pull requests，再点击new PR，注意合并方向箭头，创建和并请求，管理员检查审核后就能同意合并了，
- 对于协作者，设置中发送用户请求，分配权限，就不用fork了，直接创建分支commit，交由管理员审核，
- cherry pick拣选提交，复制需要提交的commitID给ai操作即可，
- stash临时存储，没写完的代码存储，再pop继续写，
- rebase变基，分支操作，
