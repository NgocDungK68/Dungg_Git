---
title : "Project Management"
date :  "`r Sys.Date()`" 
weight : 4 
chapter : false
pre : " <b> 3.4 </b> "
---

## Project management using Git

#### Step 1: Install Git
Download and install **Git** here: [Git_Install](https://git-scm.com/).


#### Step 2: Config Git
1. Open **Git Bash**
2. Config **user name** and **email**
    ```
    git config --global user.name "User Name"
    ```
    ```
    git config --global user.email "username@gmail.com"
    ```
![Git_Config](/Dungg_Git/images/1.4/0001.png)

3. Check config
    ```
    git config --global user.name
    ```
    ```
    git config --global user.email
    ```
![Git_Config](/Dungg_Git/images/1.4/0002.png)


#### Step 3: Initialize repository
1. Make a new direction for the project and move into that direction
    ```
    mkdir <direction_name>
    ```
- **mkdir** stands for "make directory".
- **direction_name** is the name of the folder.
- This command will make a new direction named **direction_name** in the current direction.
    ```
    cd <direction_name>
    ```
- **cd** stands for "change directory".
- **direction_name** is the name of the folder you want to move into.
- This command will change your current direction to **direction_name**.

![Git_Initialize](/Dungg_Git/images/1.4/0003.png)

2. Initialize **Repository**
    ```
    git init
    ```
- After running this command, Git will initialize a new repository in your current direction.
- This involves creating a hidden .git directory containing all the files needed to track changes in the project.
![Git_Initialize](/Dungg_Git/images/1.4/0004.png)

3. Check status
    ```
    git status
    ``` 
- This command will show the current status of the repository, including which files have been changed but not committed yet.


#### Step 4: Add and Commit Change
This step involves creating a **README.md** file, adding content to it, and then adding the file to the Git staging area and committing the changes to your repository.

1. Create a **README.md** file and write a few lines describing the project:
- Make sure you are in the project directory.
- Use the **echo** command to create a README.md file and add a description line to it:
    ```
    echo "# AdvancedGitProject" >> README.md
    ```
This command will create a README.md file and add the line "#AdvancedGitProject" to it.

![Git](/Dungg_Git/images/1.4/0005.png)

1. Check the contents of the **README.md** file:
    ```
    cat README.md
    ```
2. Add the **README.md** file to the staging area
- Use the **git add** command to add the README.md file to the staging area, preparing for commit:
    ```
    git add README.md
    ```
1. Commit change
- Use the **git commit** command to commit changes with a descriptive message:
    ```
    git commit -m "Add README.md with project description"
    ```

![Git](/Dungg_Git/images/1.4/0006.png)

#### Step 5: Create New Branch and Use Rebase
In this step, you will create a new branch, make some changes on that branch, then rebase the new branch onto the main branch.

1. Create and switch to a new branch named **feature-branch**:
    ```
    git checkout -b feature-branch
    ```
- This command creates a new branch named **feature-branch** and switches you to that branch.

![Git](/Dungg_Git/images/1.4/0007.png)

2. Create a new file **feature.txt** and add the content, then commit the changes:
    ```
    echo "This is a new feature" >> feature.txt
    ```
    ```
    git add feature.txt
    ```
    ```
    git commit -m "Add feature.txt with new feature description"
    ```

- **echo "This is a new feature" >> feature.txt**: Create a feature.txt file and add the line "This is a new feature".
- **git add feature.txt**: Add feature.txt file to staging area.
- **git commit -m "Add feature.txt with new feature description"**: Commit changes with message.

![Git](/Dungg_Git/images/1.4/0008.png)

3. Switch to **main** branch (or **master**):
    ```
    git checkout master
    ```

4. Create a new file **hotfix.txt**, add the content and commit the changes:
    ```
    echo "This is a hotfix" >> hotfix.txt
    ```
    ```
    git add hotfix.txt
    ```
    ```
    git commit -m "Add hotfix.txt with hotfix description"
    ```

![Git](/Dungg_Git/images/1.4/0009.png)

5. Rebase the **feature-branch** to the **master branch**:
    ```
    git checkout feature-branch
    ```
    ```
    git rebase master
    ```

- Move **feature-branch** commits above **main** branch's latest commit.

![Git](/Dungg_Git/images/1.4/0010.png)





 