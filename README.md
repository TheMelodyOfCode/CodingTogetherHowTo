**Hi there fellar!**

Since I'm farly new to github, 

I created this repo for my own sake, too be able to remember what steps to take to code together.
If there is anything wrong with this manual - let me know.
Cheers


**Pull request - Feaure Branch Workflow**

The idea is that ereyone works on their own feature and the main repo
won't get touched unless all changes have been discussed before the merge.

**1 - Fork it!**
    Navigate to the repo you want to contribute to and fork it

**2 - Clone it!**
    Creates a copy of the repo on your local machine
    git clone https://user@bitbucket.org/user/repo.git

**3 - Create a new Branch**
    Before you can start to work on the repo you need to create a new branch
    git checkout -b nameOfNewBranch
    To see what branch you're one
    git branch

**4 - Now you can work on the new branch as you are used to**

    -edit code
    git status   -View the state of the repo
    git add <some-file>   -Stage a file
    git commit -m "some message"

**5 - Push your changes to your online branch to get to reviewed by your co-workers**
    No changes will be made to the original repo

    git push origin nameOfBranchh

**6 - Pull request**
    Navigate on the website to the main repo
    click on:
    Compare & pull request

  The code will get reviewed by the owner and either accepted or dismissed

------------------------------------------------------------------------------------------                                                                        ------------------------------------------------------------------------------------------                                                                         
#  Working together on CENTRAL Repository   

**1 - Create a central repository**
    If it's a completely new repository, create a bare repository
    It's convention to put .git on the end   
    user@host git init --bare /path/to/repo.git

**2 - Clone the project to your local machine**

    git clone ssh://user@host/path/to/repo.git

**3 - Now you can work on your local version as you are used to**

    -edit code
    git status   -View the state of the repo
    git add <some-file>   -Stage a file
    git commit -m "some message">

**4 - To share your work push your changes to the central repository**
    git push origin main

**5 - ERROR**
    The central repo is the official project.
    If your working with several people on a central project commits can differ when updating.
    Git will throws an error if that happens.

**6 - Pull --rebase to get the changes that have been made and put your owwn on top**
    rebase transmitts every local commit one by one instead of a big massiv merge commit

    git pull --rebase origin main

**7 - Merge conflict**
    If there is a conflict check out the problem
    git status
    After the problem has been solved
    git add <some-file>
    git rebase --continue
    In case you got no f.. clue
    git rebase --abort
