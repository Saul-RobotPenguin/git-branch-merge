# Making Git Branches and Pushing into YOUR OWN GIT BRANCH!! (NOT MAIN OR MASTER!!) Also Some Git Cloning!
 
This is a sheet that gives you a step-by-step guide on how to make your branch and push changes onto your branch that's separate from the main or master.

(WARNING: I will go on with the assumption that you know how to navigate Git Bash, meaning that I will not be explaining Linux commands that navigate into directories or make directories like the one below)
```bash
cd projects
``` 

or
```bash
mkdir project-name
```


## Git Cloning 

Make sure that one of your members has already made a repository and has added you as a collaborator first before doing the following.

IN YOUR TEAMS REPOSITORY

1. Click on the Big Green Code button

2. Make sure that you have SSH clicked on and NOT HTTPS

3. Copy the entirety of the link that starts with 'git@github.com:'

![alt text](https://phoenixnap.com/kb/wp-content/uploads/2023/11/clone-git-repository-using-ssh.png)

## Git Cloning  (Part 2)
In your Git Bash or VS Code terminal, do the following

## 
```bash
git clone paste-your-link-from-github-here-instead-of-this.git
```

Now change into your team's project folder 
```bash
cd your-teams-folder
```

## Making Your Own Git Branch 

To make your git branch, use the code below but replace your-name with your first name of course.
Typically you should get into the practice of calling your branch by your first name so that everyone in your team knows who's branch is who's.

```bash
git branch your-name
```
![making a branch](https://github.com/Saul-RobotPenguin/git-branch-merge/assets/81450209/c89c20d4-6eda-44a5-ae2a-3b1a41eb99a2)

To move into your newly created branch, you would run the following

```bash
git checkout your-name
```
Notice that "(master)" disappears and is replaced with "(saul)", this lets me know that I'm in my branch instead of the master.
![from master branch to saul branch](https://github.com/Saul-RobotPenguin/git-branch-merge/assets/81450209/bfa39715-6472-4ad9-9390-8fa97e0d6902)


From here, you're able to add and make changes without interfering with your other members!

At least not yet.....



## Pushing Your Changes Into Your Branch!

You added a new color to your background or maybe you changed the font size of some text, whatever the case, your project isn't in the same state from when we first started and we need to save these changes before your hard work disappears like the number of hours of sleep I have gotten this week!


This should be familiar.


WARNING: MAKE SURE THAT YOU'RE IN YOUR BRANCH AND NOT IN THE MAIN OR MASTER!!

### Adding our Files
First we have to add the files that we have changed by either doing

```bash
git add .
```
Which adds all the files that have added or edited.

or

```bash
git add name-of-file.html
```
This means we only want one of our files that we edited to be added.


### Commiting Our Changes

After adding the files you'll need to commit your changes so make sure to do the following!

```bash
git commit -m "Whatever you want here but ideally state the changes that you did!"
```
### Pushing Our Changes Into Our OWN BRANCH

ONCE AGAIN, MAKE SURE THAT YOU'RE IN YOUR OWN BRANCH,

```bash
git push origin your-name
```

You should see the following!

![git-push-origin-saul](https://github.com/Saul-RobotPenguin/git-branch-merge/assets/81450209/dd45f643-7b99-441e-aece-6fd8eeaac0dd)



CLICK THE LINK INSIDE to make a Pull Request!!

![git-push-origin-saul-with-red-circle](https://github.com/Saul-RobotPenguin/git-branch-merge/assets/81450209/83398dd1-14a4-4aab-b0ac-a69bbee043fa)

### Making A Pull Request for our changes!

A Pull Request is a request to add changes to the production branch which is typically your main or master from your own branch which is read by a reviewer or a fellow teammate.


You should see something like this
image here
![git-pull-request](https://github.com/Saul-RobotPenguin/git-branch-merge/assets/81450209/4f36aaa6-4b5a-4ad8-ab29-630851cf9255)

Insert a description about your pull request, similar to your git commit message except you can ask questions or get into more detail about your changes to the person who's reviewing your code and determining whether it's suitable to push to the master or main branch.



## Approving Merge changes (For Code Reviewers Only!!!)
After making sure that your teammate's code is acceptable to be pushed into the master/main branch by checking the files changed, if it looks alright and you see the green button that says "Merge pull request" then go ahead and press it!.


![approve merge-red-circle](https://github.com/Saul-RobotPenguin/git-branch-merge/assets/81450209/a0f96cd3-2f65-40d6-9495-3ad8668231f7)



## Seeing those changes in your VSCode

Once a pull request is approved, you'll want the main or master branch to get the latest changes by just doing the following in your terminal

```bash
git checkout main
```
or 

```bash
git checkout master
```

depending on which branch your team agreed to put the final code changes to

and then doing the following in either main or master branch

```bash
git pull
```

### Merging your local main/master branch to your own branch



```bash
git checkout your-branch
```

And then merging your main


```bash
git merge main
```


And voila you're done!



## License

[MIT](https://choosealicense.com/licenses/mit/)
