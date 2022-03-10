# Beginners Workshop
Git and GitHub workshop for beginners

## Fork the remote respository
[IMAGE]

## Create your local respository
Clone the fork into your new folder:
```
$ git clone https://github.com/<username>/beginners-workshop  
```
[IMAGE]  

Go into the git directory:  
```
$ cd beginners-workshop
```  

Add 'upstream' repo to list of remotes:  
*This isn't required, but we do it to keep our copy up to date with the remote*
```
$ git remote add upstream https://github.com/github-user-group/beginners-workshop
```
Verify the new remote named 'upstream':  
```
$ git remote -v [-v | --verbose]
```
Open the **list_of_contributors.md** in your text editor

## Create and modify a local branch
Create a new feature branch:
```
$ git branch <feature_yourname>
$ git checkout <feature_yourname>
$ git branch -a
```
OR shorthand version:
```
$ git checkout -b <feature_yourname>
```
https://github.com/wwcgitworkshop/GithubWorkshop
https://github.com/chrisbridges/thinkful-git-workshop
