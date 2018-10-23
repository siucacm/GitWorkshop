# Git Workshop
Welcome to the Git Workshop! Today we will learn how to use git with github.

### A friendly reminder
When using the command prompt you will want to use these useful commands:
#### Linux
+ **pwd** (Path Working Directory) displays what directory you are currently in
+ **ls** (List) displays the files in the directory you are currently in
+ **cd** *directory* (Change Directory) changes the directory you are given a file
+ **nano** *file* Edit a file

#### Windows
+ **dir** displays the files in the directory you are currently in
+ **cd** *directory* (Change Directory) changes the directory you are given a file

# Getting started with git and GitHub
### Installing
#### Linux
In the terminal install git by: `sudo apt install git-all`

#### Windows
[Download git here](https://git-scm.com/download/win)

### Github
In this workshop we will be using github to host the server repository.
Go ahead and create a new repository through the website and initialize the read me.

### Setting up git account on your terminal

Set your username in the terminal, this helps git tell them who you are when you make changes.
```bash
git config --global user.name "[[USERNAME]]"
```

You should also set your email.
```bash
git config --global user.email "[[EMAIL@EXAMPLE.com]]"
```

### Cloning
+ Start by copying the HTTPS url on the github repository you just created
+ Then issue this command on your machine.
```bash
git clone [paste url here]
```
+ Lets check if the repository was cloned
```bash
ls
```

+ Next change let's make it our currect directory. (Note typing "cd Work" then hittng TAB will save you a lot of effort)
```bash
cd [[REPOSITORY NAME]]
```

+ Here's a command to check how you are connected to github
```bash
git remote -v
```
It shows the status of what repository you are fetching and pushing. This also tells you the name that is associated with the server repositories. This is usually called `origin`.

+ Let's edit the README.md file
```bash
nano README.md
```
Go a head and type a joke. Then `ctrl + o` go through the prompt and save the file. The `ctrl + x` exits the file.

#### Status, Stage, Commit, Push

Now we are going to update our server repository.
+ Let us see what files have changed
```bash
git status
```

+ Now we are going to add the file, so it gets commited next. This is called the staging.
```bash
git add README.md
```

+ Check the status again
```bash
git status
```
It's GREEN! :D

+ Now we have to commit the changes
```bash
git commit -m "Updated README"
```

+ Then we push to the server repository
```bash
git push origin master
```
Since this is your first push to github, it will prompt you for your username and password.


### Branching
+ Next we will make our own individual branches which we each can each make changes.

+ Start by making a new branch
```bash
git branch name_of_my_new_branch
```

+ Then checkout that branch
```bash
git checkout name_of_my_new_branch
```

+ Check to see what branch you are on
```bash
git branch
```

+ Next create and edit a HelloWorld.sh file 
```bash
nano HelloWorld.sh
```
Add some code to it.
```bash
echo Hello world
```
Then `ctrl + o` go through the prompt and save the file. The `ctrl + x` exits the file

### Add, commit, push
+ Next, we want to add our branch with our changes to SIUC-ACM's GitHub

+ First push your new branch to the GitHub
```bash
git push origin name_of_my_new_branch
```

+ Then, "stage" or add your modified script file.
```bash
git add HelloWorld.sh
```
	
+ Next commit your file to your local repository
```bash
git commit -m "[YOUR COMMIT MESSAGE GOES HERE]"
```
+ Define the push behavior to avoid nasty messages.
```bash
git config --global push.default matching
```

+ Finally, push your edited file to GitHub
```bash
git push
```

### Merge
+ We can now merge the branch you just created with the master branch.

First switch to the master branch
```bash
git checkout master
```

Then let's merge them
```bash
git merge name_of_my_new_branch
```

Now the branches are merged!
This is extremely helpful for collaborating with other people, as they won't mess up your own personal branch.
It is the best way to avoid merge conflicts when working with a group. Merging helps add the changes from a different branch to our own branch without "checking out" their branch. 

### EXTRA

+ You can clone this repository down and create your own branch and then merge it with others!

Clone, enter the local repository, create a branch and merge the one below.

```bash
git merge answer_for_one
```

+ Try out the encryption script. (The password is just used for encryption/decryption)
```bash
./encryption.sh
```

+ Checkout your new encrypted message!
```bash
cat encrypted_message.txt
```

+ Look under the hood.
```bash
gedit encryption.sh
```

### Fork and Pull requests
+ Suppose we want someone else's repository on our github account to edit, branch, and push however we like. To do so, all we have to do is head over to that repository's GitHub homepage and hit "fork".

+ Suppose now we think our edits are good enough to be put on the original repository. In this case, we can submit a pull request to the owner of that repository, so they can decide whether or not to add our code to theirs.

### Addtional features
+ Change the encryption type from AES to DES (try ```bash man openssl``` for help)
+ Make the script read from the command line.
+ Change the encryption message
+ Use a specific key for encryption to avoid typing in the password each time.
+ [insert features here]
