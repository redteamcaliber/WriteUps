###1) Use gitignore
Make sure that you do not push file that are not part of your code. Examples of those files are log, swap, binary, unused code files. 
Best way to get rid of them is listing those files in ".gitignore" file.

###2) Follow proper branch workflow 
Don't push all of your code to master branch. Master branch should have most recent stable code. It should have your latest release code.
Your active development should be done on any branch other than master branch. There are lot of standards/methodology followed by people. One of them is "Feature Branch Workflow". 
Follow this link for another one: http://nvie.com/posts/a-successful-git-branching-model/
