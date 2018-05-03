>git - 分布式版本控制系统
>>git init ===  命令把当前目录变成Git可以管理的仓库   
>>git add \<file>  ===  把文件添加到仓库,注意，可反复多次使用，添加多个文件  
>>git commit -m "填写描述信息"  ===  把文件提交到仓库  
>>git status  ===  命令可以让我们时刻掌握仓库当前的状态  
>>git diff ===  可以查看修改内容  
>>git log  ===  显示从最近到最远的提交日志  
>>git log --pretty=oneline  
>>git reset --hard HEAD^  ===  回退到上一版本，回退到前20版本 HEAD~20  
>>git reset --hard 3628164  ===  进入指定版本号的版本  
>>git reflog ===  用来记录你的每一次命令   
>>git checkout -- \<file>  ===  丢弃工作区的修改 : 把\<file>文件在工作区的修改全部撤销,让这个文件回到最近一次git commit或git add时的状态。
用版本库里的版本替换工作区的版本，无论工作区是修改还是删除，都可以“一键还原”  
>>git reset HEAD \<file>  ===  把暂存区的修改撤销掉（unstage），重新放回工作区  
>>git rm \<file>  ===  用于删除一个文件  
>>git push -u origin master ===  把本地库的内容推送到远程,加上了-u参数，Git不但会把本地的master分支内容推送的远程新的master分支，还会把本地的master分支和远程的master分支关联起来，在以后的推送或者拉取时就可以简化命令。  
>>git push origin master  === 把本地master分支的最新修改推送至GitHub  
>>git clone 地址 === 命令克隆





 
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

>>>翻译:  
Untracked files  ===  没有被添加过 的文件


