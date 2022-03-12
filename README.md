# Beginners Workshop
Git and GitHub workshop for beginners

## Fork the remote respository
<img src="https://user-images.githubusercontent.com/19731161/158017341-0551f689-4151-44d0-9fa8-6bff2b0d762f.png" width="60%" height="50%">

## Create your local respository
Clone the fork into your new folder:
```bash
$ git clone https://github.com/<USER_NAME>/beginners-workshop  
```
<img src="https://user-images.githubusercontent.com/19731161/158017477-670f83b3-89f3-441e-ae77-9e8cc60a917d.png" width="60%" height="50%">

Go into the git directory:  
```bash
$ cd beginners-workshop
```  

Add 'upstream' repo to list of remotes:  
*This isn't required, but we do it to keep our copy up to date with the remote*
```bash
$ git remote add upstream https://github.com/github-user-group/beginners-workshop
```
Verify the new remote named 'upstream':  
```bash
$ git remote -v [-v | --verbose]
```
Open the dir `beginners-workshop` in your text editor

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
Create a new file: `<your_name.md>`

Copy this into **your_name.md** file:

     Your name:
     Why you came to the workshop?
     Is this your first event?
     Favorite animal?
     What is GitHub user URL?

Check the status of your changes: 
```bash
   $ git status
``` 
*Your file is not being track by git, we need to add it*

Add **your_name.md** to the repo:
```bash
  $ git add <your_name.md>
```
>TIP: *git add* stages your changes. You cannot commit your changes until you have first staged them.

Check the status again to see the staged file:
```bash
  $ git status
```

Commit your changes: 
*"Commit early and commit often"*
```bash
   $ git commit -m "Add your commit message here"
``` 

Push your branch to the remote: 
```bash
   $ git push [ push | push -u origin <feature_yourname>]
   $ git status
```
>**TIP:** You only need the *-u* command if your branch is not already upstream 

## [OPTIONAL] Merge your branch into master

First review all the branches:
```bash
   $ git branch -a
```

Checkout Master:
```bash
   $ git checkout master 
```

Pull updates from the remote:
```bash
   $ git pull 
```
>**TIP:** *git pull* merges changes from the remote into your local copy. Use *git fetch* if you simply want to download the latest to keep track of what is going on. You will then need to merge to incorporate the updates from *fetch*.

Fetch upstream master and merge with your repo's master branch
```bash
$ git fetch upstream
$ git checkout master
$ git merge upstream/master
```
>**TIP:** If there were any new commits, you might want to *rebase* your development branch. More on that in the next session.

Now merge your changes into master:
```bash
  $ git merge <feature_yourname>

```

Push master to your origin:
```bash
   $ git push origin
```

## Create your PR

Go to your github and click `pull request`

<img src="https://user-images.githubusercontent.com/19731161/158018522-f5b6c4eb-0b80-478c-83c1-de439c2be8ef.png" width="60%" height="50%">

Comapre changes and submit your message

<img src="https://user-images.githubusercontent.com/19731161/158018528-0eac7b3d-c554-4715-8a79-aeb15804ffae.png" width="60%" height="50%">

## Delete your branch
*Once your PR has been merged, you should delete your feature branch*

```bash
   $ git push --delete origin <feature_yourname>
   $ git branch -d <feature_yourname>
```
