GIT # Git assignment-2

#### Create a new directory and initialize it as a Git repository.Add a README.md file to provide a brief description of the project.Make an initial commit with the README.md file.Push the repository to a remote repository hosting service (e.g., GitHub).

### Step 1: Create a New Directory and Initialize Git

#### 1. Open terminal and navigate to the location where you want to create the project.

#### 2. Create a new directory and navigate into it:

    mkdir git-assignment-2
    cd git-assignment-2

#### 3. Initialize it as a Git repository:

    git init

### Step 2: Add a README.md File

#### 1. Create a README.md file with a brief description of project:

    echo "# Git assignment-2" > README.md

#### 2. Stage the file for commit:

    git add README.md

### Step 3: Make an Initial Commit

#### 1. Commit the staged file:

    git commit -m "Initial commit"

### Step 4: Push to GitHub

#### 1. Go to GitHub and create a new repository:

 >- Repository name: git-assignment-2
 >- Do not initialize the repository with a README (to avoid conflicts).

#### 2. Add the remote repository URL to your local Git repository:

    git remote add origin https://github.com/<your-username>/my_project.git

Replace <your-username> with GitHub username.

#### 3. Push your local main branch to the remote repository:

    git branch -M main
    git push -u origin main


#### Create a new branch named feature-1.
#### Switch to the feature-1 branch.
#### Make changes to the project (e.g., add a new file or modify an existing one).
#### Commit these changes with meaningful commit messages.
#### Repeat the process by creating another branch named feature-2:
>- Switch back to the main branch.
>- Create and switch to the feature-2 branch.
>- Make changes and commit them with appropriate messages.

Push both feature-1 and feature-2 branches to the remote repository.Create pull requests (PRs) for merging feature-1 and feature-2 into the main branch.Review the changes in each PR before merging.Merge the PRs sequentially to avoid conflicts.Before merging each branch, ensure the feature branch is updated with the latest changes from the main branch.Use the method instead of merge to keep the commit history linear.Resolve any conflicts that arise during rebasing and re-test the branch.After merging both feature branches, check the commit history in the main branch.ubbEnsure that the commit history is linear and easy to understand.Delete the merged branches from both the local and remote repositories to keep the repository clean and organized.

### Step 1: Create and switch to feature-1 branch

#### 1. Create and switch to the branch:
    
    git checkout -b feature-1

### Step 2: Make changes, commit, and push the feature-1 branch

#### 1. Add or modify files (e.g., create a new file feature1.txt)

    echo "This is feature 1" > feature1.txt
    git add feature1.txt
    git commit -m "Add feature1.txt for feature1"

#### 2. Push the branch:

    git push -u origin feature-1


### Step 3: Create and switch to feature-2 branch


#### 1. Switch back to the main branch:

    git checkout main

#### 2. Create and switch to the feature-2 branch:

    git checkout -b feature-2

### Step 4: Make changes, commit, and push the feature-2 branch


#### 1. Add or modify files (e.g., create a new file feature2.txt):

    echo "This is feature 2" > feature2.txt
    git add feature2.txt
    git commit -m "Add feature2.txt for feature-2"

#### 2. Push the branch:

    git push -u origin feature-2

### Step 5: Create pull requests for feature-1 and feature-2

1. Go to your GitHub repository.
2. Open a pull request (PR) for merging feature-1 into main.
3. Open another PR for merging feature-2 into main.

### Step 6: Review and rebase feature-1 before merging

#### 1. Ensure feature-1 is updated with the latest changes from main:

    git checkout feature-1
    git fetch origin
    git rebase main

#### 2. Resolve any conflicts if they arise:

>- Fix conflicts in files.
-> Stage changes:

    git add <file>

>- Continue the rebase:

    git rebase --continue

#### 3. Force-push the rebased branch:

    git push --force

#### 4. Merge the PR for feature-1 in GitHub.

### Step 7: Rebase feature-2 and merge

#### 1. Update feature-2 with the latest changes from main:

    git checkout feature-2
    git fetch origin
    git rebase main

#### 2. Resolve conflicts, if any, and force-push the branch:

    git push --force

#### 3. Merge the PR for feature-2 in GitHub.


### Step 8: Check the commit history

#### 1. View the commit history to ensure it is linear:

    git log --oneline --graph

### Step 9: Clean up merged branches

#### 1. Delete the branches locally:

    git branch -d feature-1
    git branch -d feature-2

#### 2. Delete the branches remotely:

    git push origin --delete feature-1
    git push origin --delete feature-2


















