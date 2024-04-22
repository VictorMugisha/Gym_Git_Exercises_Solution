# GIT EXERCISES
## Exercise 1 - Bundle 1

```bash
C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git init
Initialized empty Git repository in C:/Users/victo/OneDrive/Documents/TheGym_Git_Exercises/.git/

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git status
On branch master

No commits yet

nothing to commit (create/copy files and use "git add" to track)

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git branch -m master main

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git status
On branch main

No commits yet

nothing to commit (create/copy files and use "git add" to track)

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>
```
#### After commiting the creation of README.md file and adding remote repository

```bash
C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git status
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md

nothing added to commit but untracked files present (use "git add" to track)

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git add README.md

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git commit -m "Initial commit after creating README.md file"
[main (root-commit) 66412a2] Initial commit after creating README.md file
 1 file changed, 25 insertions(+)
 create mode 100644 README.md

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git remote add origin https://github.com/VictorMugisha/Gym_Git_Exercises_Solution.git

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git branch -M main

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git push -u origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 500 bytes | 250.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/VictorMugisha/Gym_Git_Exercises_Solution.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>
```

##### After creating `dev` branch and creating and removing `test` branch
```bash
C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git checkout -b dev
Switched to a new branch 'dev'

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git status
On branch dev
nothing to commit, working tree clean

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git push origin dev
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote:
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/VictorMugisha/Gym_Git_Exercises_Solution/pull/new/dev
remote:
To https://github.com/VictorMugisha/Gym_Git_Exercises_Solution.git
 * [new branch]      dev -> dev

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git checkout -b test
Switched to a new branch 'test'

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git switch dev
Switched to branch 'dev'

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git branch -d test
Deleted branch test (was f4858cc).

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git push origin dev
Everything up-to-date

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>
```