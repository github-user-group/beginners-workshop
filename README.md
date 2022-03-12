# Beginners Workshop
Git and GitHub workshop for beginners

## Open an issue
Open a new `New contributor` with your name at the title (replace `<your_name>`)</br>  
<img src="https://user-images.githubusercontent.com/19731161/158020341-a711cc28-4e81-445b-b21e-97ae271669fb.png" width="60%" height="50%">
</br>
<img src="https://user-images.githubusercontent.com/19731161/158020410-ff20216e-4375-48f8-85cd-420cd6617cb5.png" width="60%" height="50%">

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
Create a new file under the `contributors` dir: `<your_name.md>`

Copy this into **contributors/your_name.md** file:

```
Your name:
Why you came to the workshop?
Is this your first event?
Favorite animal?
What is GitHub user URL?
```

Check the status of your changes: 
```bash
   $ git status
``` 
*Your file is not being track by git, we need to add it*

Add **contributors/your_name.md** to the repo:
```bash
  $ git add contributors/<your_name.md>
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
   $ git push 
```

You will get the following error:
```
fatal: The current branch <feature_yourname> has no upstream branch.
To push the current branch and set the remote as upstream, use
```
*This error is happening becasue your branch only exsits locally and not on the server*

So let's fix that:

```bash
   $ git push --set-upstream origin <feature_yourname>
   $ git status
```

## Create your PR

Go to your fork on GitHub and click `Compare & pull request`

<img src="https://user-images.githubusercontent.com/19731161/158021191-b2b63a14-45a0-4962-9735-cccf42365e3d.png" width="60%" height="50%">

Add your issue number to the PR title (e.g. <message> #2)  
</br>
Comapre changes and submit your message  
<img src="https://user-images.githubusercontent.com/19731161/158018528-0eac7b3d-c554-4715-8a79-aeb15804ffae.png" width="60%" height="50%">

## [Optional] Delete your branch
*Once your PR has been merged, you should delete your feature branch*

```bash
   $ git push --delete origin <feature_yourname>
   $ git branch -d <feature_yourname>
```
