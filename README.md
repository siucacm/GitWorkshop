# WorkshopThree_February3rd2017
This repository is what participants of the 3rd SIU-ACM workshop will clone to learn the basics of git and github!

#Cloning
+Start by copying the SSH url on the github homepage of this repository
+Then issue this command on your machine.
'''bash
git clone [paste url here]
'''
+Next change into that directory. (Note typing "cd Work" then hittng TAB will save you a lot of effort)
'''bash
cd WorkshopThree_February3rd2017
'''

+Try running the bash script provided
'''bash
./ecryption
'''

#Branching
+Next we will make our own indivdual branches

+Start by making a new branch
'''bash
git branch name_of_my_new_branch
'''

+Then checkout that branch
'''bash
git checkout name_of_my_new_branch
'''

#Add, commit, push
+Next, we want to add our branch to SIUC-ACM's GitHub
+Start by "staging" or adding the filec
'''bash
git add encryption
'''

+Next commit the file to your local repository
'''bash
git commit -m "{YOUR COMMIT MESSAGE GOES HERE]"
'''

+Finally, push the file to GitHub
'''bash
git push origin name_of_my_new_branch
'''

#Merge
+Suppose someone else made a really cool feature on their branch, and you want that feature for your branch.
+This is why we use branch. We can add the changes from a different branch to our own branch without "checking out" their branch

'''bash
git merge 
'''
