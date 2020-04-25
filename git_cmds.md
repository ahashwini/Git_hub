Gitbub is a code hosting platform that can enables version control collaboration.
### Installing git in your local machine [Ubuntu]
> `sudo apt-get install git -y`

### Set Up Git:
> git config --global user.name "Vamshi-dhar"                                                     
> git config --global user.email "vamshi.analyst2013@gmail.com"

### Turns local directory to git repository i.e. working copy in local machine.
> git init 
### Current state of repository.
> git status 
#### To clone repository from any public account.
> git clone <url>
  
#### to add the file to staging area for git.only files in staging area are considered for commit.
> git add <file names> 
  
#### to add all files in given repository
> git add . 
> git commit -m "(committed message)"
> git push -u origin master
> git remote add origin master (url)
