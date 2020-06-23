# How to Contribute to our website

Thank you for your offer to help. Before doing anything, make sure you have checked with one on the admins for the DCC++ EX project on either TrainBoard or our Discord.

# Submission Procedure

We will assume that you have an appropriate text editor and Git installed on your machine. We recommend the free Visual Studio Code IDE (VSC) and Git Bash. For version control, you could also use Git Desktop or with Git, VSC, and the GitLens plugin for VSC installed on your computer, you can manage everything from within VSC.

1. Clone both the "website" and "dcc-ex.github.io" repositories to your local machine. (Instructions: [Cloning a repository in GitHub](https://help.github.com/en/github/creating-cloning-and-archiving-repositories/cloning-a-repository))
2. Install Python (which also installs pip) then use pip to install mkdocs (instructions at [mkdocs.org](https://www.mkdocs.org/))
3. Using Git Bash, go to the "website" folder and make a branch: $ git checkout -b <your-name>-changes (you can use VSC and the GitLens add on to do all this too)
4. From Git Bash or a Command Prompt, run "mkdocs serve" to start up the software that turns .md markdown files in to .html files. Leave it running. (You may want to open both a Git command prompt and a Windows Command prompt or Mac Terminal window, so that the mkdocs server can be running in one while you use the Git Bash window to do your commits)
5. Open a Browser and go to "localhost:8000". The DCC++ EX website should load.
6. Open VSC and edit the files in the "website" folder. You will be only changing files in the "docs" subfolder and the mkdocs.yml file (if necessary). The browser should update the website in real time as you save changes.
7. Save in your editor and use "Git Add" and "Git commit" often to save changes. (VSC is one click to commit. It prompts to add unstaged files).
8. Push it to GitHub: $ git push origin <your-name>-changes
9. Double check that the website in your browser is working, then go back to the command prompt window, hit cntrl-c to stop the server.
10. Go to GitHub and issue a pull request for your <your-name>-changes branch to be pulled into the master branch
11. At this point one of the admins can then approve and merge the PR.
12. Anyone who gets privileges to administer the web page would make sure their "website" repo pulled in the latest version. If this was you, and you just issued and approved the PR, then your website repo is up to date. From the command prompt, change to the "dcc-ex.github.io" repository and run this command: 
$ mkdocs gh-deploy --config-file ..\website\mkdocs.yml --remote-branch master
This last step takes the .md files in the website repo, converts them into html and puts them in the dcc-ex.github.io repo and then pushes them up to GitHub which updates the live website.
