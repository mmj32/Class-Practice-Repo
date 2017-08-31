# Class Practice Repo

Publicly shared class repo. For practicing, class activities, etc.

## Initial steps
Fork this repository into your GitHub account. Then, clone your fork to your local machine. 

    git clone git@github.com:YOUR-USERNAME/YOUR-FORKED-REPO.git

Add remote from original repository ('upstream') into your forked local repository. 

    cd into/cloned/fork-repo
    git remote add upstream git://github.com/ORIGINAL-DEV-USERNAME/REPO-YOU-FORKED-FROM.git

## Submitting to-do tasks

The routine goes like:

1. Move into your local repo. 

2. Start by syncing with the original upstream: 

```git
git fetch upstream	
git pull upstream master```

3. Move into the current assignment directory (todo1, todo2, etc.)

4. Work on your submission file. Name it `todo1_yourname.txt` or something like it. 

5. Don't forget to commit and save your progress while working on your file. Also, check status via `git status`. 

6. Occasionally push it to your GitHub remote fork. 

7. When you think you have a final version, push it one last time to your GitHub remote fork. Check the file on GitHub to make sure everything looks fine. 

8. Create a pull request for me. 


