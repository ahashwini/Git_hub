Gitbub is a code hosting platform that can enables version control collaboration.
### Installing git in your local machine [Ubuntu]
> `sudo apt-get install git -y`

### Set Up Git:
> `git config --global user.name "Vamshi-dhar"`                                                    
> `git config --global user.email "vamshi.analyst2013@gmail.com"`

#### To clone repository from any public account. (URL you get from a given repo)
> `git clone <url>`

### Turns local directory to git repository i.e. working copy in local machine.
> `git init` 

### Current state of files that you need to commit / pust to git repo. This will show if there are any untracked files.
> `git status`  

#### to add the file to staging area for git. (only files in staging area are considered for commit)
> `git add <file names>`
  
#### to add all files from current folder to staging area. 
> `git add .`    


#### a kind of checkpoint to staging area. Snapshot of data that is available at the top will only be pushed to git repo.  
> `git commit -m "<committed message>"`   

#### 
Incase if any file is stagged by mistake, then to unstage it, you can be use. 
> `git -rm --catched <filename>`   
--hard ???
or to unstage all files use.
> `git -rm --catched .`   

Hostory of project:
> `git log .`   

Unstage commints:
Each commit will have a hash id, and is built on top of each other so you can not remove the commits form the middle of the order in log. 
What ever copy of hash Id is mentioned, all above commits will be removed. 
> `git reset <hash_id>`   
hash_id you can get from git log. (above author and after commit)

### Stashing:
Git provides an easy way of stashing these uncommitted changes so that we can return to them later, without having to make unnecessary commits. 

To stash use:
> `git stash`   

To revese stash, use:
> `git stash pop`   

To close/clear stashing:
> `git stash clear`   


### allocating name to URL
To add a URL of Repo to a local machine.
> `git remote add origin <url link>`
Here origin is like contact name and 
URL link is the mobile number. 

To check URLs that are linked to the current local env.
> `git remote -v`

### push based on name allocated (origin)
> `git push origin <branch-name>`
Note: origin is used for personal, upstream is used while forking the repo from others. (URL of that person named upstream)
-f cmd can be used for force push. It is required when Eg: you have removed a file that was there in earlier commit in github, in such senario to make it possible we need to push it with force. 


### To update my forked repo with its actual owers repo.
>`git fetch --all -prune`or
>`git pull upstream main` 

eg: When I forked a repo it is having 3 commits, 
and after some days. A 2 new commits are made in actual repo and you need to get it. This is made with help of fetch.
- -prune: If you deleted any files. those also be fixed.
Also after fetching from upstram, if we need to have same commit as upstream.

>`git reset --hard upstream/main` 
note: it gets updated in local machine only, so to reflet in your github repo you need to pust it. 
and then you need to push to main branch to reflet commit in your own repo. 


### Branching
Note: Before creating a new branch, you need to make sure that your master is upto date. 1:01:01

To create a new branch
> `git branch <branch-name>`

To move to other branch
> `git checkout <branch-name>`

To merge into other branch
> `git merge <branch-name>`


- Comapre and Pull request, pop up when you push to your local Repo with given new branch (other than main/master).
Only one pull request can be done for 1 branch.
- So it is adviced to create a new branch for every new feature that we work with. 
- i.e. each time prepare the new breach and add new features and push to your local Repo into that same new branch created and it automatically pops up compare and pull request. 

#######################################

### Squashing
> `git rebase -i <hash-id of commit you need it to be remained>` 
Note: -i indicates interactive.
- In interatcive UI,  replacing "pick" with "s" will squash that perticular commit.
pick eadskbs 1
s asdcaug 2
s aciuagd 3
pick ascgada 4
this will mix 2 and 3 into 1, as a result only commits 1 and 4 are visible. 
- to exit from interactive UI, press Esc and then :x and Enter. 



##################################
> `git push -u origin master`  
> `git remote add origin master (url)`  
