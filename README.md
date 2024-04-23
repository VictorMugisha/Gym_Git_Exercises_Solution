# GIT EXERCISES

## Bundle 1
### Bundle 1 - Exercise 1: Creating and deleting branches 

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

### Bundle 1 - Exercise 2: Adding, Stashing and Unstashing files
```bash

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git status
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        home.html

nothing added to commit but untracked files present (use "git add" to track)

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git add home.html

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git stash
Saved working directory and index state WIP on main: 3dc9eb4 Deleted files to re-do Exercise2

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git status
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        about.html

nothing added to commit but untracked files present (use "git add" to track)

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git add about.html

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git stash
Saved working directory and index state WIP on main: 3dc9eb4 Deleted files to re-do Exercise2

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git add team.html

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git stash
Saved working directory and index state WIP on main: 3dc9eb4 Deleted files to re-do Exercise2

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git stash list
stash@{0}: WIP on main: 3dc9eb4 Deleted files to re-do Exercise2
stash@{1}: WIP on main: 3dc9eb4 Deleted files to re-do Exercise2
stash@{2}: WIP on main: 3dc9eb4 Deleted files to re-do Exercise2

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git stash pop stash@{1}
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (7f2b482d7dc26421d05d52355c67b8440724822c)

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git stash pop stash@{2}
Auto-merging about.html
CONFLICT (content): Merge conflict in about.html
CONFLICT (modify/delete): home.html deleted in Updated upstream and modified in Stashed changes.  Version Stashed changes of home.html left in tree.
On branch main
Your branch is up to date with 'origin/main'.

Unmerged paths:
  (use "git restore --staged <file>..." to unstage)
  (use "git add/rm <file>..." as appropriate to mark resolution)
        both modified:   about.html
        deleted by us:   home.html

no changes added to commit (use "git add" and/or "git commit -a")
The stash entry is kept in case you need it again.

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git stash pop stash@{0}
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

Dropped stash@{0} (1cc923897cfb5a407a54c9339c1fb1a1ce16e729)

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git reset --hard
HEAD is now at 6d33625 Currect stashing state with only team.html stashed

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>
```

## Bundle 2

### Bundle 2 - Exercise 1

```bash
PS C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises> git commit -m 
[main 7c464df] Finished with bundle 1
PS C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises> git checkout -
Switched to a new branch 'ft/bundle2'
PS C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises> git branch -m ft/bundle-2
PS C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises> git status
On branch ft/bundle-2
nothing to commit, working tree clean
PS C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises> git status
On branch ft/bundle-2
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        services.html

nothing added to commit but untracked files present (use "git add" to track)     
PS C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises> git add services.html
PS C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises> git commit -m "Adding 
services.html page"
[ft/bundle-2 e328a70] Adding services.html page
 1 file changed, 14 insertions(+)
 create mode 100644 services.html
PS C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises> git push origin ft/bundle-2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 482 bytes | 482.00 KiB/s, done. 
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/VictorMugisha/Gym_Git_Exercises_Solution/pull/new/ft/bundle-2
remote: 
To https://github.com/VictorMugisha/Gym_Git_Exercises_Solution.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
PS C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>
```

### Bundle 2 - Exercise 2
```bash
PS C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises> git status
On branch ft/bundle-2
nothing to commit, working tree clean
PS C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises> git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises> git pull
remote: Enumerating objects: 1, done.
remote: Counting objects: 100% (1/1), done.
remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (1/1), 923 bytes | 230.00 KiB/s, done.
From https://github.com/VictorMugisha/Gym_Git_Exercises_Solution
   7c464df..4563deb  main       -> origin/main
Updating 7c464df..4563deb
Fast-forward
 README.md     | 43 +++++++++++++++++++++++++++++++++++++++++++
 services.html | 14 ++++++++++++++
 2 files changed, 57 insertions(+)
 create mode 100644 services.html
PS C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises> git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
PS C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises> git checkout -b ft/service-redesign
Switched to a new branch 'ft/service-redesign'
PS C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises> git status
On branch ft/service-redesign
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   services.html

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises> git add --all
PS C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises> git commit -m "Modifying services.html from ft/service-redesign branch"
[ft/service-redesign e70b7fa] Modifying services.html from ft/service-redesign branch
 1 file changed, 2 insertions(+)
PS C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises> git push origin ft/service-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 394 bytes | 197.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/VictorMugisha/Gym_Git_Exercises_Solution/pull/new/ft/service-redesign
remote:
To https://github.com/VictorMugisha/Gym_Git_Exercises_Solution.git
 * [new branch]      ft/service-redesign -> ft/service-redesign
PS C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises> git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises> git add services.html
PS C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises> git commit -m "Modifying services page from main branch"
[main 3400197] Modifying services page from main branch
 1 file changed, 2 insertions(+)
PS C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises> git push origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 393 bytes | 393.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/VictorMugisha/Gym_Git_Exercises_Solution.git
   4563deb..3400197  main -> main
PS C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises> git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'
PS C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises> git diff main
diff --git a/services.html b/services.html
index 28a9b03..cf81dbc 100644
--- a/services.html
+++ b/services.html
@@ -10,7 +10,7 @@
     <h1>Services Page</h1>
     <p>This is the content of services page!</p>

-    <h2>This is from main branch and we have old services!</h2>
+    <h2>We are introducing new services to clients</h2>

 </body>
 </html>
\ No newline at end of file
PS C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises> git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises> git merge ft/service-redesign
Auto-merging services.html
CONFLICT (content): Merge conflict in services.html
Automatic merge failed; fix conflicts and then commit the result.
PS C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises> git status
On branch main
Your branch is up to date with 'origin/main'.

You have unmerged paths.
  (fix conflicts and run "git commit")
  (use "git merge --abort" to abort the merge)

Unmerged paths:
  (use "git add <file>..." to mark resolution)
        both modified:   services.html

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises> git add --all
PS C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises> git commit -m "Merge ft/service-redesign into main"
[main faf70de] Merge ft/service-redesign into main
PS C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises> git push origin main
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 443 bytes | 221.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/VictorMugisha/Gym_Git_Exercises_Solution.git
   3400197..faf70de  main -> main
PS C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>
```

## Bundle 3

### Bundle 3 - Exercise 1 
```bash
git checkout ft/team-page
Already on 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git status
On branch ft/team-page
Your branch is up to date with 'origin/ft/team-page'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        team.html

nothing added to commit but untracked files present (use "git add" to track)

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git add --all

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git commit -m "Creating team page"
[ft/team-page 21b9140] Creating team page
 1 file changed, 14 insertions(+)
 create mode 100644 team.html

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git push origin ft/team-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 459 bytes | 459.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/VictorMugisha/Gym_Git_Exercises_Solution.git
   765742a..21b9140  ft/team-page -> ft/team-page

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git checkout -b  ft/contact-page
fatal: a branch named 'ft/contact-page' already exists

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git branch -d ft/contact-page
Deleted branch ft/contact-page (was 4e9fa2e).

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git commit -m ""
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git push origin main
Everything up-to-date

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git branch -d ft/contact-page
error: branch 'ft/contact-page' not found

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git checkout -b  ft/contact-page
Switched to a new branch 'ft/contact-page'

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git checkout ft/team-page
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git log
commit 21b9140c4ca6a81ca885c2fbc9660b4ea6c5829c (HEAD -> ft/team-page, origin/ft/team-page)
Author: Victor Mugisha Shyaka <victormugishavm6@gmail.com>
Date:   Mon Apr 22 19:32:10 2024 +0200

    Creating team page

commit 765742a634bca5d1b1c9c0e39b2aa29677c00882
Author: Victor Mugisha Shyaka <victormugishavm6@gmail.com>
Date:   Mon Apr 22 18:15:59 2024 +0200

    Done.

commit b8a5f3c7d40c500de58ed810b53b81f50a2d2803
Author: Victor Mugisha Shyaka <victormugishavm6@gmail.com>
Date:   Mon Apr 22 17:57:15 2024 +0200

    Adding content to contact page while cherry-picking commit

commit 35c8748c4e55da90274ac34f1ca31b079e663784
Author: Victor Mugisha Shyaka <victormugishavm6@gmail.com>
Date:   Mon Apr 22 17:57:15 2024 +0200

    Created team page in ft/team branch

commit 4e9fa2e3006ef606acf80e2051e2e8da238c1af0 (origin/main, main, ft/contact-page)
Author: Victor Mugisha Shyaka <victormugishavm6@gmail.com>
Date:   Mon Apr 22 17:51:15 2024 +0200

    Completed with Bundle 2 - Exercise 2

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git checkout ft/contact-page
Switched to branch 'ft/contact-page'

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git cherry-pick 21b9140c4ca6a81ca885c2fbc9660b4ea6c5829c
[ft/contact-page 4e96a16] Creating team page
 Date: Mon Apr 22 19:32:10 2024 +0200
 1 file changed, 14 insertions(+)
 create mode 100644 team.html

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git status
On branch ft/contact-page
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        contact.html

nothing added to commit but untracked files present (use "git add" to track)

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git add contact.html

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git commit -m "Updating contact with cherry-pick"
[ft/contact-page d1e0230] Updating contact with cherry-pick
 1 file changed, 14 insertions(+)
 create mode 100644 contact.html

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git push origin ft/contact-page
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 784 bytes | 392.00 KiB/s, done.
Total 6 (delta 3), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/VictorMugisha/Gym_Git_Exercises_Solution/pull/new/ft/contact-page
remote:
To https://github.com/VictorMugisha/Gym_Git_Exercises_Solution.git
 * [new branch]      ft/contact-page -> ft/contact-page

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git checkout -b ft/faq-page
Switched to a new branch 'ft/faq-page'

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git add faq.html

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git commit -m "Added faq.html"
[ft/faq-page 3ebd540] Added faq.html
 1 file changed, 13 insertions(+)
 create mode 100644 faq.html

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git status
On branch ft/faq-page
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        deleted:    team.html


C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git commit -m "Reverted to commit"
[ft/faq-page 0992296] Reverted to commit
 1 file changed, 14 deletions(-)
 delete mode 100644 team.html

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git push origin ft/faq-page
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 236 bytes | 236.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/VictorMugisha/Gym_Git_Exercises_Solution.git
   852d73a..0992296  ft/faq-page -> ft/faq-page

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>
```


### Bundle 3 - Exercise 2

```bash
C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git checkout ft/faq-page
Switched to branch 'ft/faq-page'

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git checkout -b ft/home-page-redesign
Switched to a new branch 'ft/home-page-redesign'

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git add --all

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git commit -m "Made changes to main branch"
[main 0c1a7d5] Made changes to main branch
 2 files changed, 1 insertion(+), 7 deletions(-)

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git push origin main
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 425 bytes | 425.00 KiB/s, done.
Total 4 (delta 3), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (3/3), completed with 3 local objects.
To https://github.com/VictorMugisha/Gym_Git_Exercises_Solution.git
   01915e0..0c1a7d5  main -> main

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git checkout ft/home-page-redesign
Switched to branch 'ft/home-page-redesign'

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git rebase main
Successfully rebased and updated refs/heads/ft/home-page-redesign.

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git status
On branch ft/home-page-redesign
nothing to commit, working tree clean

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git status
On branch ft/home-page-redesign
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   home.html

no changes added to commit (use "git add" and/or "git commit -a")

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git add home.html

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git commit -m "Add changes to home page"
[ft/home-page-redesign 8c5e034] Add changes to home page
 1 file changed, 2 insertions(+)

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git push origin ft/home-page-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 372 bytes | 372.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'ft/home-page-redesign' on GitHub by visiting:
remote:      https://github.com/VictorMugisha/Gym_Git_Exercises_Solution/pull/new/ft/home-page-redesign
remote:
To https://github.com/VictorMugisha/Gym_Git_Exercises_Solution.git
 * [new branch]      ft/home-page-redesign -> ft/home-page-redesign

```

## Bundle 4

### Bundle 4 - Exercise 1 : Terminal History After creating second repo and pushing new changes
```bash
C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git checkout main
Already on 'main'
Your branch is up to date with 'origin/main'.

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git remote add git-copy https://github.com/VictorMugisha/git-copy.git

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git remote -v
git-copy        https://github.com/VictorMugisha/git-copy.git (fetch)
git-copy        https://github.com/VictorMugisha/git-copy.git (push)
origin  https://github.com/VictorMugisha/Gym_Git_Exercises_Solution.git (fetch)
origin  https://github.com/VictorMugisha/Gym_Git_Exercises_Solution.git (push)

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git add home.html

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git commit -m "After changing home content and creating git-copy repo"
[main 1023454] After changing home content and creating git-copy repo
 1 file changed, 2 insertions(+)

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git push origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 410 bytes | 410.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/VictorMugisha/Gym_Git_Exercises_Solution.git
   e8cc05b..1023454  main -> main

C:\Users\victo\OneDrive\Documents\TheGym_Git_Exercises>git push git-copy main
Enumerating objects: 81, done.
Counting objects: 100% (81/81), done.
Delta compression using up to 4 threads
Compressing objects: 100% (78/78), done.
Writing objects: 100% (81/81), 12.50 KiB | 673.00 KiB/s, done.
Total 81 (delta 41), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (41/41), done.
To https://github.com/VictorMugisha/git-copy.git
 * [new branch]      main -> main
```