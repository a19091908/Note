<h1>GIT Note</h1>

* git diff
    - git diff
    
    git diff will show you any changes that you’ve made but not yet added to the index

    -git diff --cached

   show you any changes that you have added to the index

* git add

    git add 命令接受「檔案」或「目錄」做為路徑名稱；如果是目錄，該命令會用遞迴的方式加入那個目錄下所有的檔案。


* git log --graph

    以ASCII 圖形用來顯示分支及合併的歷史

* git log --oneline

    以簡化的方式顯示log

* git commit --amend

    This command is to amend the commit message
    - 修改commit訊息。
    - 或如果忘了add files到stages，可以先將尚未add的files加入後，再使用 
    <code>git commit --amend</code>  

* git reset HEAD [file]

    This command is to move the file from stage to unstage

* git checkout -- [file]

    This command is to discard changes of the file

-------------

* git remote add [remote-name] [url]

   This command is to create a new remote repository 

* git fetch [remote-name]

   This command is to fetch data from remote repository( it would not merge)

* git pull

   This command is to fetch data first, and then to merge automatically

* git push [remote-name] [branch-name]

------------

* git tag -a v1.4 -m "my version 1.4"
    
    - create a tag
    - parameter: 
        1. -a means create
        2. -m means a tag message 

* git tag

    list all tags

* git show [tag_name]

    show the tag messages

* git push [remote-name] [tagname]

    the tag would not be push to the remote repository unless using git push [remote-name] [tagname]  

* git push [remote-name] --tags

    This command is to push all the tags that are not in the remote repository to the remote repository.

---------

* git branch
    
    list all branches

* git branch [branchName]

    create a new branch

* git checkout [branchName]

    checkout to the branch

---------

* git branch -d [branchName]
    
    delete a branch whose name is [branchName]

* git merge [branchName]
    
    merge a branch named [branchName] into the current branch

    #####Note that merge will cause confilcts if a piece of data is changed in both histories.

* git branch --no-merged

    list all the branches that have been merged into your current branch

------

* git rebase [baseBranch] [topicBranch]

    replay all the commits of [topicBranch] on [baseBranch]


    




 
    

