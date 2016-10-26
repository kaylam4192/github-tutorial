# GitHub Tutorial

_by Kayla Matos_

---
## Git vs. GitHub
There is a very big difference between **Git** and **Github**
* **Git:** Git is able to keep snapshots of your code, it runs in the command line, and it **does not require Github.**
* **Github:** Github requires Git, and stores code in the website.



---
## Initial Setup
### Making an Account
1. First off go to [Github](github.com)
2. Click the green _Sign up_ button in the upper right part of the screen.
3. Make your username the same as your HSTAT email without the @hstat.org part
4. Verfiy your account or else it won't work properly
5. Go to cloud9 and sign in 
6. Click on settings and go to connected services
7. Link Github and Cloud9, from on now you can sign in to cloud9 by clicking on the github icon(octocat)

### Cloud9 and Github SSH Key
Now that you have an account for Github and Cloud9 we have to add an SSH key. This allows you to push your work to Github at a later time without having to put in your password everytime.

1. First open Github and go to settings
2. Look for SSH and GPG keys and click on that
3. Enter the name to be Cloud9 and then open up [Cloud9](c9.io)
4. Click the gear icon in the top right corner and go to SSH Keys
5. Copy the code there beginning with `ssh-rsa` and paste it into github 
6. Go back to cloud9 and open up your workspace. In the terminal type `ssh -T git@github.com` and you should get a confirmation showing that you created the SSH Key


---
## Repository Setup
Now, it's time to create your first repository. Open up your workspace and make a new directory. Go into that directory and type `git init` to initialize git in your directory. Create a file using `touch` and add some text to it. Make sure cloud9 saved your work and then go to the terminal to `add` and `commit` the file. When committing make sure the **message is short and is written in future tense** to help other users trying to collaborate with you understand what a certain commit did. To make your current local repository to a remote repository you must make a repository on github. Open up github and click the plus sign to make a repository. When making the repository make sure you name it the same as the one you have on github. **Otherwise it will not work**. After you create the repository it will take you to a screen. Somewhere there it will have _HTTPS_ highlighted, change this to have SSH highlighted. Lower on the page it should have two lines of code and ontop of them it should say "...or push an existing repository from the command line". Copy those two lines and paste them into your terminal on cloud9. After that you should be able to push your changes from cloud9 to github.


---
## Workflow & Commands
`git status` is one of many commands necessary to properly use git. It is an optional command. The command highlights in red files that are untracked and need to be added to the, it highlights in green the files that are being tracked and are ready to commit. This can be useful because it can remind you to do things you have accidentally forgotten to do. `git add` is also a necessity because it adds files to the staging area in order to be committed and saved. `git commit -m "message` is the command used to save the current version of your files and revert back to them if there are errors. It also includes a helpful reminder telling you what you changed with that commit. Another useful command is `git push` which allows you to send your commits to the cloud, which is basically github. Your code is stored here and remembered incase something happens to your hardrive and you lose all your files.

---
## Error Handling 
### Did You Do git init In the Wrong Directory?
You can use `rm -rf .git` to remove git. The reason this works is because the .git is a hidden file that is created when you do `git init`. The `rm` part of the code means to remove however the `-rf` part means to remove recursively and forcefully.
### Do You Want to Remove a Repository? 
First go to the parent directory of the repository you want to delete. Use `rm -rf` along with the name of the repository you want to delete. Once that is gone you can go to [Github](github.com) and delete the repository on Github to. Now it is officially gone from your cloud and your local workspace.

---
## Collaboration
Github is a good way to work with others to come together and collaborate on one project. Or if you just want to take somebody elses work and take it in a different direction then you can do that and submit it to the user so that he can see the changes you made and decide if he also wants to use those changes. You can also clone other peoples work by going to your cloud9 terminal and type `git clone <url>`. This will allow you to have their work but if you try to push some of your changes, it will not allow you because you do not have permission. If you would like to be able to push the changes you made you can fork repositories and and make them your own. You can do this while you're looking at some other repository there will be a fork option at the top right corner. You click on that and you will have your own copy of the repo however it belongs to you. If you make a change that you think should be in the original project you can submit a pull. The owner can choose to include it in his work which would be him pulling your pull requests adding it to his work.