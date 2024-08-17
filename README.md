## Create empty git repository with git init command. 

![Снимок экрана 2024-08-17 143214.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/850409a6-1c4d-4d08-b306-c1cf9786b99f/95c5eb3b-855e-4bab-a4fa-4f48b0918c45/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA_%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0_2024-08-17_143214.png)

## Let us create new file with touch README.md command.

![Снимок экрана 2024-08-17 144503.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/850409a6-1c4d-4d08-b306-c1cf9786b99f/366c61e6-4433-46d1-a6bc-e2014b6577e2/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA_%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0_2024-08-17_144503.png)

## To modify the existing file, we will use VIM text editor. 
This editor is widely used for rebasing and other git activities so every developer should get used to it. 
Type vim README.md command to open vim text editor. Press letter i to enter the insert mode. 
Type in “Hello World” or something you like. Press Escape on the keyboard to exit from insert mode and
go to the command mode. In the command mode press Shift + ZZ to save current file and exit.

![Снимок экрана 2024-08-17 144729.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/850409a6-1c4d-4d08-b306-c1cf9786b99f/67f29824-fa38-45f3-a263-62bd82b544c9/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA_%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0_2024-08-17_144729.png)

![Снимок экрана 2024-08-17 144911.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/850409a6-1c4d-4d08-b306-c1cf9786b99f/0785d043-d184-4dda-a89c-0b79eb7d969d/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA_%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0_2024-08-17_144911.png)

## To check the progress type git status command. 
You should see that readme file is untracked now. 
You should check for a status as often as it is possible. 
If you always read status carefully enough, you will never end up in strange unpredictable situations.

![Снимок экрана 2024-08-17 145157.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/850409a6-1c4d-4d08-b306-c1cf9786b99f/0572d47d-5fa7-46b6-b215-9fe09cc214cc/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA_%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0_2024-08-17_145157.png)

## To track readme you can use git add command. 
This will track and stage all the files in the current directory. 
Now you should see that your readme file is green which means it is also staged. 
Take a moment to read about tracking and staging and how they are different with each other.

![Снимок экрана 2024-08-17 145357.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/850409a6-1c4d-4d08-b306-c1cf9786b99f/0061bc5d-295d-4683-bc1c-d73e47dd3d92/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA_%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0_2024-08-17_145357.png)

It is time to commit changes. To create commit use git commit -m “created readme”
command which will create commit with corresponding message. Your working tree should be
clean now.

![Снимок экрана 2024-08-17 145533.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/850409a6-1c4d-4d08-b306-c1cf9786b99f/46d19471-1521-45ad-8cae-3ae4f8a647f8/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA_%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0_2024-08-17_145533.png)

We are going to create new branch called develop, which will contain all the functionality you
are currently working on. To create a new branch, execute git checkout -b develop command.
This will create new branch from the current (master). Create git_task branch from develop and
git_0 branch from git_task

![Снимок экрана 2024-08-17 145825.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/850409a6-1c4d-4d08-b306-c1cf9786b99f/1bd727ac-c793-43c3-835e-b8e8a51cdf88/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA_%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0_2024-08-17_145825.png)

You can use git show-branch command to view all branches at once. The branch you are
currently working with is marked with * symbol.

![Снимок экрана 2024-08-17 145932.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/850409a6-1c4d-4d08-b306-c1cf9786b99f/0b816c14-75d8-4933-9948-44415f726e12/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA_%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0_2024-08-17_145932.png)

Now we will add some changes to README.md, with vim, check status, stage changes with
git add README.md command, commit changes, check the result (status) then checkout to
git_task branch (with git checkout git_task command) and merge changes from git_0 branch
with git merge git_0 --no-ff command. Take some time to read about merging and no-ff option.
This is usually the default pull request merging behavior so you will work with it on you daily
basis.

![Снимок экрана 2024-08-17 151617.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/850409a6-1c4d-4d08-b306-c1cf9786b99f/eab9d58e-98e3-41ba-b0ee-3d4e7c6d89f9/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA_%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0_2024-08-17_151617.png)

![Снимок экрана 2024-08-17 151548.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/850409a6-1c4d-4d08-b306-c1cf9786b99f/ab861534-d023-45c6-814b-101bf6f934ce/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA_%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0_2024-08-17_151548.png)

![Снимок экрана 2024-08-17 151739.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/850409a6-1c4d-4d08-b306-c1cf9786b99f/e8a329e5-9cd9-4a26-acc8-58fecb3da382/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA_%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0_2024-08-17_151739.png)

Also note that you can view staged changes with git diff --cached command. For example, here
we can see that new line “changes from git_0” was added to the file

Also note that you can view your latest changes with gitk command (which should invoke gitk
tool). If this command does nothing or returns error, this usually means that you do not have gitk
installed by default (e.g. working from mac). This tool is not necessary and is the matter of
choice.

![Снимок экрана 2024-08-17 152510.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/850409a6-1c4d-4d08-b306-c1cf9786b99f/9129b8c7-b4f6-4b5c-a005-6aaa3632a6dc/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA_%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0_2024-08-17_152510.png)

![Снимок экрана 2024-08-17 152643.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/850409a6-1c4d-4d08-b306-c1cf9786b99f/2ef0d529-6f41-4243-910e-04223b3d677f/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA_%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0_2024-08-17_152643.png)

Now repeat merging process to get your commit to master (through develop of course)
branch. When you finish, you can use something this git log --all --graph --decorate --
oneline --simplify-by-decoration or this git log --graph --oneline –all command. These
commands were found on the stackoverflow as an answer to a question of viewing git history
as a tree. This is not the best solution, but it is more than enough for our needs. You output
should look similar to this:

![Снимок экрана 2024-08-17 154231.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/850409a6-1c4d-4d08-b306-c1cf9786b99f/ca3137e7-20fe-47bf-89d7-62417fbc80f8/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA_%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0_2024-08-17_154231.png)

![Снимок экрана 2024-08-17 154642.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/850409a6-1c4d-4d08-b306-c1cf9786b99f/3c426a49-2ddb-46d9-8fad-6c8fd286bea5/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA_%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0_2024-08-17_154642.png)

![Снимок экрана 2024-08-17 154839.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/850409a6-1c4d-4d08-b306-c1cf9786b99f/f35b40c8-6ab7-40c5-b3a7-400a700d27d0/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA_%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0_2024-08-17_154839.png)
