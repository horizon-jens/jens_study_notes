>git - 分布式版本控制系统
>>git init ===  命令把当前目录变成Git可以管理的仓库  
>>git add file-name  ===  把文件添加到仓库,注意，可反复多次使用，添加多个文件  
>>git commit -m "填写描述信息"  ===  把文件提交到仓库  
>>git status  ===  命令可以让我们时刻掌握仓库当前的状态  
>>git diff ===  可以查看修改内容  
>>git log  ===  显示从最近到最远的提交日志  
>>git log --pretty=oneline  
>>git reset --hard HEAD^  ===  回退到上一版本，回退到前20版本 HEAD~20  
>>git reset --hard 3628164  ===  进入指定版本号的版本  
>>git reflog ===  用来记录你的每一次命令   
>>git checkout -- file-name  ===  丢弃工作区的修改 : 把文件在工作区的修改全部撤销,让这个文件回到最近一次git commit或git add时的状态。
用版本库里的版本替换工作区的版本，无论工作区是修改还是删除，都可以“一键还原”  
>>git reset HEAD file-name  ===  把暂存区的修改撤销掉（unstage），重新放回工作区  
>>git rm file-name  ===  用于删除一个文件  
>>git push -u origin master ===  把本地库的内容推送到远程,加上了-u参数，Git不但会把本地的master分支内容推送的远程新的master分支，还会把本地的master分支和远程的master分支关联起来，在以后的推送或者拉取时就可以简化命令。  
>>git push origin master  === 把本地master分支的最新修改推送至GitHub  
>>git clone 地址 === 命令克隆  
>>git checkout -b branch-name ===  创建+切换分支   
>>git branch  ===  查看分支  
>>git branch branch-name  ===  创建name分支  
>>git checkoutbranch-name  ===  切换分支  
>>git merge branch-name ===  合并某分支到当前分支  
>>git branch -d branch-name  ===  删除分支  
>>git stash  ===  把当前工作现场“储藏”起来，等以后恢复现场后继续工作  
>>git stash pop  ===  恢复工作区的同时把stash内容也删了  
>>git remote -v  ===  查看远程库信息  
>>git push origin branch-name  ===  从本地推送分支  
>>git pull  ===  抓取远程的新提交  
>>git checkout -b branch-name origin/branch-name  ===  在本地创建和远程分支对应的分支,本地和远程分支的名称最好一致  
>>git branch --set-upstream branch-name origin/branch-name  ===  建立本地分支和远程分支的关联  
>>git tag tag-name  ===  用于新建一个标签  
>>git tag -a tag-name -m "blablabla..."  ===  可以指定标签信息  
>>git tag  ===  查看所有标签  
>>git tag -d tag-name  ===  删除一个本地标签  
>>git push origin tag-name  ===  可以推送一个本地标签  
>>git push origin --tags  ===  可以推送全部未推送过的本地标签  






 
>>> 例子:  
$ git add file1.txt  
$ git add file2.txt file3.txt  
$ git commit -m "add 3 files."  

>>>注意：  
HEAD指向的版本就是当前版本，因此，Git允许我们在版本的历史之间穿梭，使用命令git reset --hard commit_id。  
穿梭前，用git log可以查看提交历史，以便确定要回退到哪个版本。  
要重返未来，用git reflog查看命令历史，以便确定要回到未来的哪个版本。 

>>>注意：  
要关联一个远程库，使用命令git remote add origin git@server-name:path/repo-name.git；  
关联后，使用命令git push -u origin master第一次推送master分支的所有内容；  
此后，每次本地提交后，只要有必要，就可以使用命令git push origin master推送最新修改；  

>>>多人协作的工作模式：  
1.首先，可以试图用git push origin branch-name推送自己的修改；  
2.如果推送失败，则因为远程分支比你的本地更新，需要先用git pull试图合并；  
3.如果合并有冲突，则解决冲突，并在本地提交；  
4.没有冲突或者解决掉冲突后，再用git push origin branch-name推送就能成功！  
5.如果git pull提示“no tracking information”，则说明本地分支和远程分支的链接关系没有创建，用命令git branch --set-upstream branch-name origin/branch-name。  

>>>翻译:  
Untracked files  ===  没有被添加过 的文件  
modified  ===  adj. 改进的，修改的；改良的 v. 修改；缓和  

