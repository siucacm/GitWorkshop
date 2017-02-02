# WorkshopThree_February3rd2017
This repository is what participants of the 3rd SIU-ACM workshop will clone to learn the basics of git and github!


#Getting started with git and GitHub
###Cloning
+ Start by copying the SSH url on the github homepage of this repository
+ Then issue this command on your machine.
```bash
git clone [paste url here]
```
+ Next change into that directory. (Note typing "cd Work" then hittng TAB will save you a lot of effort)
```bash
cd WorkshopThree_February3rd2017
```

+ Try running the bash script provided
```bash
./ecryption.sh
```

+ There's no encryption yet, but we'll get there.

###Branching
+ Next we will make our own individual branches upon which we each can modify willy nilly.

+ Start by making a new branch
```bash
git branch name_of_my_new_branch
```

+ Then checkout that branch
```bash
git checkout name_of_my_new_branch
```

+ Next edit the encryption.sh file to say "Hello ACM"
```bash
gedit encryption.sh
```

###Add, commit, push
+ Next, we want to add our branch to SIUC-ACM's GitHub
+ Start by "staging" or adding the file.
```bash
git add encryption.sh
```

+ Next commit the file to your local repository
```bash
git commit -m "[YOUR COMMIT MESSAGE GOES HERE]"
```
+ Define the push behavior to avoid nasty messages.
```bash
git config --global push.default matching
```

+ Finally, push the file to GitHub
```bash
git push origin name_of_my_new_branch
```

###Merge
+ Suppose someone else made a really cool feature on their branch, and you want that feature for your branch.
+ This is why we use branch. We can add the changes from a different branch to our own branch without "checking out" their branch.

```bash
git merge answer_for_one
```

###Fork and Pull requests
+ Suppose we want someone else's repository on our github account to edit, branch, and push however we like. To do so, all we have to do is head over to that repository's GitHub homepage and hit "fork".

+ Suppose now we think our edits are good enough to be put on the original repository. In this case, we can submit a pull request to the owner of that repository, so they can decide whether or not to add our code to theirs.

###Addtional features
+ Change the encryption type from AES to DES (try ```bash man openssl``` for help)
+ Make the script read from the command line.
+ Change the encryption message
+ Use a specific key for encryption to avoid typing in the password each time.
+ [insert features here]
