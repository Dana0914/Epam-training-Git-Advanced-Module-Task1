## Create empty git repository with git init command. 

![Снимок экрана 2024-08-17 143214](https://github.com/user-attachments/assets/905994ca-efcc-4191-b789-1c5351c3de55)



## Let us create new file with touch README.md command.

![Снимок экрана 2024-08-17 144503](https://github.com/user-attachments/assets/07f35d29-9fb0-4707-a666-22bd76f23924)


## To modify the existing file, we will use VIM text editor. 
This editor is widely used for rebasing and other git activities so every developer should get used to it. 
Type vim README.md command to open vim text editor. Press letter i to enter the insert mode. 
Type in “Hello World” or something you like. Press Escape on the keyboard to exit from insert mode and
go to the command mode. In the command mode press Shift + ZZ to save current file and exit.

![Снимок экрана 2024-08-17 144729](https://github.com/user-attachments/assets/7aba3181-0be4-4df0-929c-08defa2971d6)

![Снимок экрана 2024-08-17 144911](https://github.com/user-attachments/assets/579a0082-92e9-4ec5-a31e-8d2042313e1a)

![Снимок экрана 2024-08-17 145010](https://github.com/user-attachments/assets/c63ed4a6-521b-4956-839c-27cc5536fc0e)


## To check the progress type git status command. 
You should see that readme file is untracked now. 
You should check for a status as often as it is possible. 
If you always read status carefully enough, you will never end up in strange unpredictable situations.

![Снимок экрана 2024-08-17 145157](https://github.com/user-attachments/assets/32f05410-3da0-49c4-8d00-f34299bfe23d)


## To track readme you can use git add command. 
This will track and stage all the files in the current directory. 
Now you should see that your readme file is green which means it is also staged. 

![Снимок экрана 2024-08-17 145357](https://github.com/user-attachments/assets/1b995e2f-a507-41f8-a7c3-e7b6dd1dcf54)


It is time to commit changes. To create commit use git commit -m “created readme”
command which will create commit with corresponding message. Your working tree should be
clean now.

![Снимок экрана 2024-08-17 145533](https://github.com/user-attachments/assets/c80b5ece-91ec-4b4d-8393-70d609928127)


We are going to create new branch called develop, which will contain all the functionality you
are currently working on. To create a new branch, execute git checkout -b develop command.
This will create new branch from the current (master). Create git_task branch from develop and
git_0 branch from git_task

![Снимок экрана 2024-08-17 145825](https://github.com/user-attachments/assets/76b8c355-4ed4-4cdb-912c-aae4887508b3)

You can use git show-branch command to view all branches at once. The branch you are
currently working with is marked with * symbol.

![Снимок экрана 2024-08-17 145932](https://github.com/user-attachments/assets/3601306c-2ef9-4cc7-b6f4-7b4cb5c41ab3)


Now we will add some changes to README.md, with vim, check status, stage changes with
git add README.md command, commit changes, check the result (status) then checkout to
git_task branch (with git checkout git_task command) and merge changes from git_0 branch
with git merge git_0 --no-ff command. Take some time to read about merging and no-ff option.
This is usually the default pull request merging behavior so you will work with it on you daily
basis.

![Снимок экрана 2024-08-17 151617](https://github.com/user-attachments/assets/78fd4e83-129d-438e-9d12-14bd6ceac46a)

![Снимок экрана 2024-08-17 151548](https://github.com/user-attachments/assets/54c27bc9-e79c-4cc6-a8fe-3b643dd4eabc)

![Снимок экрана 2024-08-17 151739](https://github.com/user-attachments/assets/5efe5836-3469-424e-9b63-88ab9d1d3af8)



Also note that you can view staged changes with git diff --cached command. For example, here
we can see that new line “changes from git_0” was added to the file

Also note that you can view your latest changes with gitk command (which should invoke gitk
tool). If this command does nothing or returns error, this usually means that you do not have gitk
installed by default (e.g. working from mac). This tool is not necessary and is the matter of
choice.

![Снимок экрана 2024-08-17 152510](https://github.com/user-attachments/assets/1fc454d7-80d6-488c-9854-fcd13c30e55b)

![Снимок экрана 2024-08-17 152643](https://github.com/user-attachments/assets/c3d09d26-6e14-4a89-9584-55aa469cd0b7)



Now repeat merging process to get your commit to master (through develop of course)
branch. When you finish, you can use something this git log --all --graph --decorate --
oneline --simplify-by-decoration or this git log --graph --oneline –all command. These
commands were found on the stackoverflow as an answer to a question of viewing git history
as a tree. This is not the best solution, but it is more than enough for our needs. You output
should look similar to this:

![Снимок экрана 2024-08-17 154231](https://github.com/user-attachments/assets/b84113db-178e-4d86-8d1d-d08a6b8da9cb)

![Снимок экрана 2024-08-17 154642](https://github.com/user-attachments/assets/3469d6ce-f72b-4100-8f12-367351d9846e)

![Снимок экрана 2024-08-17 154839](https://github.com/user-attachments/assets/f0d74122-e856-40d2-88f6-02705bf9547c)



