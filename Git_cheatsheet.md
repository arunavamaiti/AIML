Create a devops directory in your home directory
Go to devops directory
Run git init to initialize a git repository
git config user.name "full_name"
git config user.email "email_id"


Create an empty file called helloworld.py using touch helloworld.py
Add line print("Hello World") in helloworld.py and save the file
Please use the below command to add a line to the file
echo 'print("Hello World")' > helloworld.py
Verify the file content using cat command
cat helloworld.py
You can use nano or vi editor to edit the file content if you are comfortable with them using commands like nano helloworld.py or vi helloworld.py

git add helloworld.py
git commit -m "First commit"

Check the branch you are in using git branch command
If you are not in master then checkout to master branch using git checkout master command
Now create a new branch feature_a and checkout to that branch

git branch testing
git checkout testing
git checkout -b dev


Check the status of files in your project using git status command
git status

Add the helloworld.py file to staging area using git add command
Commit the change to branch feature_a using git commit command with the message "Added I am learning git line"
-m flag can be used to provide message while committing


Merging branches:

If you are not on the master branch then checkout to master branch using git checkout master command
Check the content of helloworld.py file using cat helloworld.py command
Merge feature_a branch into master branch using git merge <branch_name> command


Add remote to your existing repository using : 

git remote add origin git@github.com:<your-github-username>/<repository-name>.git


GitHub Project - Getting Started with Git - Creating SSH keys and adding to GitHub:

NOTE:
      The .ssh folder and key files should have correct permissions. You can check permissions using ls -la command and
      hange them using chmod command
      The .ssh directory permissions should be 700 (drwx------)
      The public key (.pub file) permissions should be 644 (-rw-r--r--)
      The private key (id_rsa) permissions should be 600 (-rw-------)


Generate your ssh key pair using:

ssh-keygen -t rsa -b 4096
Save the key in ~/.ssh/id_rsa file
Set the password or it can be left empty
Copy the content of ~/.ssh/id_rsa.pub file and add it to SSH keys in GitHub account
Make sure you are copying only the public key stored in ~/.ssh/id_rsa.pub

git push -u origin master

note : 
if youwant to remove :
git remote rm origin
then to add use:
git remote add origin git@github.com:username/myapp.git
