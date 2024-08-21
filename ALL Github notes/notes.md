git config --global user.name "name"  # Correct
git config --global user.email "email@gmail.com"  # Remove the backtick and fix the typo in "gmail.com"
git config --global core.editor "code --wait"  # Correct, setting VS Code as the default editor
git config --global core.autocrlf true  # Add 'true' to enable line ending conversion from Windows to Unix/Linux

//

1. Stages in Git:
U - Untracked: New files not yet tracked by Git.
A - Added or Staged: Files added to the staging area.
C - Committed: Changes committed to the repository.
2. Typical Workflow:
Stage Changes Using VS Code:

Use the Git icon in VS Code or click the + symbol next to the file to stage it.
View Commit History:

bash
Copy code
git log --oneline
This shows a concise list of commits with their commit hashes.
Reset to a Previous Commit:

To move back one commit:
bash
Copy code
git reset --hard HEAD~1
To move back two commits:
bash
Copy code
git reset --hard HEAD~2
View Reflog to Identify the Commit to Move Forward To:

bash
Copy code
git reflog
This displays a list of recent commits and their hashes, including actions like resets.
Move Forward to a Specific Commit:

Suppose e1a1b5f is the hash of the commit you want to move forward to:
bash
Copy code
git reset --hard e1a1b5f
 

// stauts and logs 

git status -s  it will give only main point

git log // give full information

git log -oneline // give only main point or --graph it was a flag //for brach

git status -s tell the status before and after commit

git log tell the no of commits we did 



// Branches 


git branch   // show the branch 

git branch name of the branch// create a new branch

git switch branch name // switch the branch


// to merge first go to the main then 
git merge branch name // then git add . commit etc.. done


//to delete the branch

git branch -d branch name // delete the branch




For Main Repository:
bash
Copy code
cd path/to/main-repo # Navigate to the main repo
git pull origin main # Pull latest changes from remote
git push origin main # Push your changes to remote
For Submodule:
bash
Copy code
cd path/to/submodule # Navigate to the submodule directory
git pull origin main # Pull latest changes from remote
git push origin main # Push your changes to remote
cd ../.. # Return to main repo directory
git add path/to/submodule # Update submodule reference
git commit -m "Update submodule reference" # Commit submodule update
git push origin main # Push changes to remote






Remove the file from tracking (without deleting it from the remote):
git rm --cached <file_name>


git init
git remote add origin https://github.com/yourusername/your-repo.git
git fetch origin
git checkout main  # or `master`
git pull origin main  # or `master`
git add .
git commit -m "Your commit message"
git push origin main  # or `master`
