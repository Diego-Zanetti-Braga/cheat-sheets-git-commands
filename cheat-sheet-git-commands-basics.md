## Basic Unix commands to use git bash
- Enter a folder
>> cd <folder_name>

- Go to one folder up
>> cd ..

- Go to the root folder
>> cd ~

- Make a new folder
>> mkdir <folder_vame>

- Create a new file
>> touch <file_name.extension>

## Important informations
- "indes state" is the same as the staging area


## Iniciate a git repository

- Open git bash
- Go to the folder where you want to initiate the git repository and use the following command
>> git init

- Check if this is alredy a git repository
>> git status

## Commit

- First, stage the files that you want to stage
>> git add <file_name.txt>

- or stage all changes
>> git add .

- Commiting
>> git commit -m "you commit message here"
- Commiting and adding all files that have already been staged at least once before
>> git commit -am "you commit message here" 

## Branching

- See all branches available
>> git branch

- Swicth branches
>> git switch <branch_that_you_want_to_go>
or
>> git checkout <branch_that_you_want_to_go>

- Create a new branch based on another one
>> git switch <branch_you_want_to_copy>
>> git switch -c <branch_you_want_to_create>
or
>> git checkout -b <branch_you_want_to_create>

- Delete a branch
>> git branch -d <branch_name>
or
>> git branch -D <branch_name> (if it is a branch that has never been merged to any other branch)


## Merging

- Go to the branch that you want to receive the changes of the other branch
>> git merge <branch_with_the_changes>


## Diff

- See the differences between the Working Area (or WIP: Work In Progress) and steged files
>> git diff

- See the differences between the staging and working area and the last commit
>> git diff head <optional: file_name if you want to diff a specific file>

- See the differences between staging area and the last commit
>> git diff --staged <optional: file_name if you want to diff a specific file>
>> git diff --cached <optional: file_name if you want to diff a specific file>

- Compare files between two different branches
>> git diff branch-a..branch-b
or
>> git diff branch-a branch-b
- To compare a specific file between branches
>> git diff branch-a..branch-b -- file_name.txt


- Compare files between two different commits
>> git diff ce4175d..811a471
or
>> git diff ce4175d  811a471

- Compare the current HEAD with the previous HEAD
>> git diff head..head~1
or just
>> git diff head~1 (this code is the same as "git diff head~1..head", it just switches the order)

## Stashing
- Stash (hide/save) WIP (staged and unstaged) so you can move branches without the need to commit
>> $ git stash ("git stash save" is the same)

- Unstash (apply stashed changes) and drop the changes of the stash (if there is more then one stash it will consider the last one)
>> $ git stash pop

- Unstash (apply stashed changes) and keep the changes of the stash in memory (if there is more then one stash it will consider the last one)
>> $ git stash apply

-- List os the stashes that you have in memory
>> git stash list

-- Apply a specific stash version
>> git stash apply stash@{1} (the versions of stash will have an alias that look like this: "stash@{1}", "stash@{2}", etc..)

-- Drop a specific stash
>> git stash drop stash@{1}

-- Drop all stashes
>> git stash clear



