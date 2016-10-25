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
3. Make your username the same as your HSTAT email excluding the @hstat.org part
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



---
## Workflow & Commands