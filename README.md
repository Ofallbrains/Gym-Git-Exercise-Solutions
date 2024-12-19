# Git exercises

## Bundle 1

### Exercise1

```bash
gymimena@Imenas-iMac ~ % cd documents
gymimena@Imenas-iMac documents % mkdir Git-Exercises
gymimena@Imenas-iMac documents % cd Git-Exercises 
gymimena@Imenas-iMac Git-Exercises % git init
Initialized empty Git repository in /Users/gymimena/Documents/Git-Exercises/.git/
 git status
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Bundle 1/

nothing added to commit but untracked files present (use "git add" to track)
gymimena@Imenas-iMac Git-Exercises % git branch -m main master
gymimena@Imenas-iMac Git-Exercises % git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Bundle 1/

nothing added to commit but untracked files present (use "git add" to track)
gymimena@Imenas-iMac Git-Exercises % git add .
gymimena@Imenas-iMac Git-Exercises % git commit -m "Exercise 1"
[master (root-commit) ef12307] Exercise 1
 1 file changed, 12 insertions(+)
 create mode 100644 Bundle 1/Ex1.html
gymimena@Imenas-iMac Git-Exercises % git remote add origin https://github.com/Ofallbrains/GIT-EXERCISES.git
gymimena@Imenas-iMac Git-Exercises % git push -u origin master
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (4/4), 435 bytes | 435.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/Ofallbrains/GIT-EXERCISES.git
 * [new branch]      master -> master
branch 'master' set up to track 'origin/master'.
gymimena@Imenas-iMac Git-Exercises % git remote -v
origin  https://github.com/Ofallbrains/GIT-EXERCISES.git (fetch)
origin  https://github.com/Ofallbrains/GIT-EXERCISES.git (push)
gymimena@Imenas-iMac Git-Exercises % git branch dev
gymimena@Imenas-iMac Git-Exercises % git status
On branch master
Your branch is up to date with 'origin/master'.

nothing to commit, working tree clean
git checkout -b dev
Switched to a new branch 'dev'
gymimena@Imenas-iMac Git-Exercises % git push origin dev
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote: 
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/Ofallbrains/GIT-EXERCISES/pull/new/dev
remote: 
To https://github.com/Ofallbrains/GIT-EXERCISES.git
 * [new branch]      dev -> dev
gymimena@Imenas-iMac Git-Exercises % git status
On branch dev
nothing to commit, working tree clean
gymimena@Imenas-iMac Git-Exercises % git checkout -b test
Switched to a new branch 'test'
gymimena@Imenas-iMac Git-Exercises % git push origin test
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote: 
remote: Create a pull request for 'test' on GitHub by visiting:
remote:      https://github.com/Ofallbrains/GIT-EXERCISES/pull/new/test
remote: 
To https://github.com/Ofallbrains/GIT-EXERCISES.git
 * [new branch]      test -> test
gymimena@Imenas-iMac Git-Exercises % git checkout dev
Switched to branch 'dev'
git branch -d test  
Deleted branch test (was ef12307).
```

### Exercise 2

```bash

gymimena@Imenas-iMac Bundle 1 % git add .
gymimena@Imenas-iMac Bundle 1 % git stash
Saved working directory and index state WIP on master: 44009cd ex1
gymimena@Imenas-iMac Bundle 1 % git status
On branch master
Your branch is up to date with 'origin/master'.

nothing to commit, working tree clean
gymimena@Imenas-iMac Bundle 1 % git add .
gymimena@Imenas-iMac Bundle 1 % git stash
Saved working directory and index state WIP on master: 44009cd ex1
gymimena@Imenas-iMac Bundle 1 % git add .
gymimena@Imenas-iMac Bundle 1 % git stash
Saved working directory and index state WIP on master: 44009cd ex1
gymimena@Imenas-iMac Bundle 1 % git stash list
stash@{0}: WIP on master: 44009cd ex1
stash@{1}: WIP on master: 44009cd ex1
stash@{2}: WIP on master: 44009cd ex1
gymimena@Imenas-iMac Bundle 1 % git stash pop stash@{2}
On branch master
Your branch is up to date with 'origin/master'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   home.html

Dropped stash@{2} (c6a472b9c8c14b4cd7b67eaabb2f5c4eae024179)
gymimena@Imenas-iMac Bundle 1 % git stash pop stash@{1}
On branch master
Your branch is up to date with 'origin/master'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped stash@{1} (1117fb3f5ac795fb0234e3dfbc32f12e733d1d4e)
gymimena@Imenas-iMac Bundle 1 % git commit -m "Stashing"
[master 355ded6] Stashing
 2 files changed, 22 insertions(+)
 create mode 100644 Bundle 1/about.html
 create mode 100644 Bundle 1/home.html
gymimena@Imenas-iMac Bundle 1 % git push
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 8 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (5/5), 556 bytes | 556.00 KiB/s, done.
Total 5 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/Ofallbrains/GIT-EXERCISES.git
   44009cd..355ded6  master -> master
gymimena@Imenas-iMac Bundle 1 % git stash pop stash@{0} 
On branch master
Your branch is up to date with 'origin/master'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped stash@{0} (f4a3b5edd4dda6d4df44fd229569cf8f64f9ef45)
gymimena@Imenas-iMac Bundle 1 % git reset --hard
HEAD is now at 355ded6 Stashing
```

## Bundle 2

### Exercise1

``` bash
gymimena@Imenas-iMac Git-Exercises % git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'
gymimena@Imenas-iMac Git-Exercises % git add .
gymimena@Imenas-iMac Git-Exercises % git commit -m "Changes made"
[ft/bundle-2 a99418d] Changes made
 1 file changed, 11 insertions(+)
 create mode 100644 services.html
gymimena@Imenas-iMac Git-Exercises % git push origin ft/bundle-2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 442 bytes | 442.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
remote: 
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/Ofallbrains/GIT-EXERCISES/pull/new/ft/bundle-2
remote: 
To https://github.com/Ofallbrains/GIT-EXERCISES.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2

 ```

 ### Exercise 2

 ``` bash
 git pull origin main
remote: Enumerating objects: 1, done.
remote: Counting objects: 100% (1/1), done.
remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (1/1), 897 bytes | 448.00 KiB/s, done.
From https://github.com/Ofallbrains/GIT-EXERCISES
 * branch            main       -> FETCH_HEAD
   f6a498a..be6d3b8  main       -> origin/main
Updating f6a498a..be6d3b8
Fast-forward
 services.html | 11 +++++++++++
 1 file changed, 11 insertions(+)
 create mode 100644 services.html
gymimena@Imenas-iMac Git-Exercises % git checkout -b  ft/service-redesign
Switched to a new branch 'ft/service-redesign'
gymimena@Imenas-iMac Git-Exercises % git add .
gymimena@Imenas-iMac Git-Exercises % git commit -m "Modified changes"
[ft/service-redesign 45a3393] Modified changes
 1 file changed, 1 insertion(+)
gymimena@Imenas-iMac Git-Exercises % git push origin ft/service-redesign 
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 350 bytes | 350.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/Ofallbrains/GIT-EXERCISES/pull/new/ft/service-redesign
remote: 
To https://github.com/Ofallbrains/GIT-EXERCISES.git
 * [new branch]      ft/service-redesign -> ft/service-redesign
gymimena@Imenas-iMac Git-Exercises % git checkout main
Switched to branch 'main'
gymimena@Imenas-iMac Git-Exercises % git add .
gymimena@Imenas-iMac Git-Exercises % git commit -m "changes"
[main c240672] changes
 1 file changed, 1 insertion(+)
gymimena@Imenas-iMac Git-Exercises % git push origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 330 bytes | 330.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/Ofallbrains/GIT-EXERCISES.git
   be6d3b8..c240672  main -> main
gymimena@Imenas-iMac Git-Exercises % git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'
git diff main..ft/service-redesign
gymimena@Imenas-iMac Git-Exercises % git diff main..ft/service-redesign
diff --git a/services.html b/services.html
index 4835ab8..67918b8 100644
--- a/services.html
+++ b/services.html
@@ -7,6 +7,6 @@
 </head>
 <body>
     <h1>Welcome to our services page</h1>
-    <p>services</p>
+    <p>These are our services:</p>
 </body>
 </html>
\ No newline at end of file
gymimena@Imenas-iMac Git-Exercises % git checkout main
Switched to branch 'main'
gymimena@Imenas-iMac Git-Exercises % git merge ft/service-redesign
Auto-merging services.html
CONFLICT (content): Merge conflict in services.html
Automatic merge failed; fix conflicts and then commit the result.
gymimena@Imenas-iMac Git-Exercises % git push origin main
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 360 bytes | 360.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/Ofallbrains/GIT-EXERCISES.git
   c240672..97b113c  main -> main

```

## Bundle 3

### Exercise1

``` bash
gymimena@Imenas-iMac Git-Exercises % git checkout -b ft/team-page
Switched to a new branch 'ft/team-page'
gymimena@Imenas-iMac Git-Exercises % git add .
gymimena@Imenas-iMac Git-Exercises % git commit -m "Created a new page"
[ft/team-page 681e9b7] Created a new page
 1 file changed, 11 insertions(+)
 create mode 100644 team.html
gymimena@Imenas-iMac Git-Exercises % git push origin ft/team-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 467 bytes | 467.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
remote: 
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/Ofallbrains/GIT-EXERCISES/pull/new/ft/team-page
remote: 
To https://github.com/Ofallbrains/GIT-EXERCISES.git
 * [new branch]      ft/team-page -> ft/team-page
 gymimena@Imenas-iMac Git-Exercises % git checkout main
Switched to branch 'main'
gymimena@Imenas-iMac git-exe % git pull origin main
remote: Enumerating objects: 1, done.
remote: Counting objects: 100% (1/1), done.
remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (1/1), 896 bytes | 448.00 KiB/s, done.
From https://github.com/Ofallbrains/Git--Exe
 * branch            main       -> FETCH_HEAD
   78fc4a4..97bf7fd  main       -> origin/main
Updating 78fc4a4..97bf7fd
Fast-forward
 team.html | 11 +++++++++++
 1 file changed, 11 insertions(+)
 create mode 100644 team.html
 create mode 100644 team.html
gymimena@Imenas-iMac git-exe % git branch  ft/contact-page
gymimena@Imenas-iMac Git-Exercises % git checkout ft/team-page
Switched to branch 'ft/team-page'
gymimena@Imenas-iMac Git-Exercises % git log
commit 681e9b788358d4fc1d069591ca7e6ebdb11ef211 (HEAD -> ft/team-page, origin/ft/team-page)
Author: Ofallbrains <ofallbrains@gmail.com>
Date:   Wed Dec 18 13:25:32 2024 +0200

    Created a new page

commit 97b113c1154f0906dbc31182a7fc0aa71d5a3436 (origin/main, main, ft/contact-page)
Merge: c240672 45a3393
Author: Ofallbrains <ofallbrains@gmail.com>
Date:   Wed Dec 18 12:35:14 2024 +0200

    Merge branch 'ft/service-redesign'

commit c2406727677fc073a5e86d8ae4b2281abca69209
Author: Ofallbrains <ofallbrains@gmail.com>
Date:   Wed Dec 18 12:22:38 2024 +0200

    changes
:
gymimena@Imenas-iMac Git-Exercises % git checkout ft/contact-page
Switched to branch 'ft/contact-page'
gymimena@Imenas-iMac Git-Exercises % git cherry-pick  681e9b788358d4fc1d069591ca7e6ebdb11ef211
[ft/contact-page 3c60ed6] Created a new page
 Date: Wed Dec 18 13:25:32 2024 +0200
 1 file changed, 11 insertions(+)
 create mode 100644 team.html
gymimena@Imenas-iMac Git-Exercises % git add .
gymimena@Imenas-iMac Git-Exercises % git commit -m "Cherry pick"
[ft/contact-page 99dde39] Cherry pick
 1 file changed, 1 insertion(+)
gymimena@Imenas-iMac Git-Exercises % git push origin ft/contact-page
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 8 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 707 bytes | 707.00 KiB/s, done.
Total 6 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), done.
remote: 
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/Ofallbrains/GIT-EXERCISES/pull/new/ft/contact-page
remote: 
To https://github.com/Ofallbrains/GIT-EXERCISES.git
 * [new branch]      ft/contact-page -> ft/contact-page
 gymimena@Imenas-iMac Git-Exercises % git checkout -b ft/faq-page
Switched to a new branch 'ft/faq-page'
gymimena@Imenas-iMac Git-Exercises % git add .
gymimena@Imenas-iMac Git-Exercises % git commit -m "Questions"
[ft/faq-page c982043] Questions
 1 file changed, 11 insertions(+)
 create mode 100644 faq.html
gymimena@Imenas-iMac Git-Exercises % git push origin ft/faq-page
Enumerating objects: 25, done.
Counting objects: 100% (25/25), done.
Delta compression using up to 8 threads
Compressing objects: 100% (24/24), done.
Writing objects: 100% (25/25), 3.00 KiB | 3.00 MiB/s, done.
Total 25 (delta 11), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (11/11), done.
remote: 
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/Ofallbrains/GIT-EXERCISES/pull/new/ft/faq-page
remote: 
To https://github.com/Ofallbrains/GIT-EXERCISES.git
 * [new branch]      ft/faq-page -> ft/faq-page
 gymimena@Imenas-iMac Git % git log
commit af5f541f8871b68e43965b46cac41db0f6f74de1 (HEAD -> ft/faq-page, origin/ft/faq-page)
Author: Ofallbrains <ofallbrains@gmail.com>
Date:   Wed Dec 18 16:23:50 2024 +0200

    faq page

commit 1781dd2583ddd1665707d8f215bbf0764c084adf (origin/ft/contact-page, ft/contact-page)
Author: Ofallbrains <ofallbrains@gmail.com>
Date:   Wed Dec 18 16:21:24 2024 +0200

    CONTACT PAGE

commit 7ea35a99e03e6642587e9af722b5bc61cebc33ec
Author: Ofallbrains <ofallbrains@gmail.com>
Date:   Wed Dec 18 16:14:29 2024 +0200

    Created team page

commit 9f6e864707088679f270ad3ea47e467c922c7c43 (origin/main, main)
Merge: 14ec2e8 b165b51
Author: Ofallbrains <ofallbrains@gmail.com>
Date:   Wed Dec 18 16:12:46 2024 +0200
gymimena@Imenas-iMac Git % git revert 7ea35a99e03e6642587e9af722b5bc61cebc33ec
hint: Waiting for your editor to close the file... code --wait: code: command not found
error: There was a problem with the editor 'code --wait'.
Please supply the message using either -m or -F option.
gymimena@Imenas-iMac Git % git revert 7ea35a99e03e6642587e9af722b5bc61cebc33ec
error: your local changes would be overwritten by revert.
hint: commit your changes or stash them to proceed.
fatal: revert failed
gymimena@Imenas-iMac Git % git status   
On branch ft/faq-page
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        deleted:    team.html

gymimena@Imenas-iMac Git % git commit -m "reverted"
[ft/faq-page 39f69d2] reverted
 1 file changed, 11 deletions(-)
 delete mode 100644 team.html
gymimena@Imenas-iMac Git % git log
commit 39f69d24ca9f0576a002d9b2db310213f7fadb17 (HEAD -> ft/faq-page)
Author: Ofallbrains <ofallbrains@gmail.com>
Date:   Wed Dec 18 16:25:57 2024 +0200

    reverted

commit af5f541f8871b68e43965b46cac41db0f6f74de1 (origin/ft/faq-page)
Author: Ofallbrains <ofallbrains@gmail.com>
Date:   Wed Dec 18 16:23:50 2024 +0200

    faq page

commit 1781dd2583ddd1665707d8f215bbf0764c084adf (origin/ft/contact-page, ft/contact-page)
Author: Ofallbrains <ofallbrains@gmail.com>
Date:   Wed Dec 18 16:21:24 2024 +0200

    CONTACT PAGE

commit 7ea35a99e03e6642587e9af722b5bc61cebc33ec
Author: Ofallbrains <ofallbrains@gmail.com>
Date:   Wed Dec 18 16:14:29 2024 +0200

gymimena@Imenas-iMac Git % git push
fatal: The current branch ft/faq-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/faq-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

gymimena@Imenas-iMac Git % git push origin ft/faq-page
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 216 bytes | 216.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/Ofallbrains/Git-Exercises.git
   af5f541..39f69d2  ft/faq-page -> ft/faq-page
   ```

   ### Exercise 2

   ``` bash
   gymimena@Imenas-iMac Git % git checkout ft/faq-page
Switched to branch 'ft/faq-page'
gymimena@Imenas-iMac Git % git branch ft/home-page-redesign
gymimena@Imenas-iMac Git % git checkout main
Switched to branch 'main'
gymimena@Imenas-iMac Git % git add --all
gymimena@Imenas-iMac Git % git commit -m "changes to contact"
[main 6b3d3d9] changes to contact
 1 file changed, 1 insertion(+)
gymimena@Imenas-iMac Git % git push origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 319 bytes | 319.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/Ofallbrains/Git-Exercises.git
   cdb42ab..6b3d3d9  main -> main
gymimena@Imenas-iMac Git % git checkout ft/home-page-redesign
Switched to branch 'ft/home-page-redesign'
gymimena@Imenas-iMac Git % git status
On branch ft/home-page-redesign
nothing to commit, working tree clean
gymimena@Imenas-iMac Git % git log
commit 39f69d24ca9f0576a002d9b2db310213f7fadb17 (HEAD -> ft/home-page-redesign, origin/ft/faq-page, ft/faq-page)
Author: Ofallbrains <ofallbrains@gmail.com>
Date:   Wed Dec 18 16:25:57 2024 +0200

    reverted

commit af5f541f8871b68e43965b46cac41db0f6f74de1
Author: Ofallbrains <ofallbrains@gmail.com>
Date:   Wed Dec 18 16:23:50 2024 +0200

    faq page

commit 1781dd2583ddd1665707d8f215bbf0764c084adf (origin/ft/contact-page, ft/contact-page)
Author: Ofallbrains <ofallbrains@gmail.com>
Date:   Wed Dec 18 16:21:24 2024 +0200

    CONTACT PAGE

commit 7ea35a99e03e6642587e9af722b5bc61cebc33ec
Author: Ofallbrains <ofallbrains@gmail.com>
Date:   Wed Dec 18 16:14:29 2024 +0200
gymimena@Imenas-iMac Git % git rebase main
Successfully rebased and updated refs/heads/ft/home-page-redesign.
gymimena@Imenas-iMac Git % git status
On branch ft/home-page-redesign
nothing to commit, working tree clean
gymimena@Imenas-iMac Git % git log
commit 6b3d3d968f8c4b887932eb3b359073aa55922d68 (HEAD -> ft/home-page-redesign, origin/main, main)
Author: Ofallbrains <ofallbrains@gmail.com>
Date:   Wed Dec 18 16:38:39 2024 +0200

    changes to contact

commit cdb42ab9464169c85d349904ceed1f9cb3716209
Merge: 1ab61fb 39f69d2
Author: Uwamwezi Denyse <ofallbrains@gmail.com>
Date:   Wed Dec 18 16:27:31 2024 +0200

    Merge pull request #4 from Ofallbrains/ft/faq-page
    
    Ft/faq page

commit 1ab61fbabae6fea9380efe458d960e86d13aa02d
Merge: 9f6e864 1781dd2
Author: Uwamwezi Denyse <ofallbrains@gmail.com>
Date:   Wed Dec 18 16:27:13 2024 +0200

    Merge pull request #3 from Ofallbrains/ft/contact-page
gymimena@Imenas-iMac Git % git add .
gymimena@Imenas-iMac Git % git commit -m "all"
[ft/home-page-redesign 4a43218] all
 1 file changed, 5 insertions(+), 1 deletion(-)
gymimena@Imenas-iMac Git % git push origin ft/home-page-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 326 bytes | 326.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote: 
remote: Create a pull request for 'ft/home-page-redesign' on GitHub by visiting:
remote:      https://github.com/Ofallbrains/Git-Exercises/pull/new/ft/home-page-redesign
remote: 
To https://github.com/Ofallbrains/Git-Exercises.git
 * [new branch]      ft/home-page-redesign -> ft/home-page-redesign

```

### Bundle 4

## Exercise 1

``` bash 
gymimena@Imenas-iMac Git % git checkout main
Switched to branch 'main'
gymimena@Imenas-iMac Git % git remote git-copy https://github.com/Ofallbrains/Another-git-repo.git
error: unknown subcommand: `git-copy'
usage: git remote [-v | --verbose]
   or: git remote add [-t <branch>] [-m <master>] [-f] [--tags | --no-tags] [--mirror=<fetch|push>] <name> <url>
   or: git remote rename [--[no-]progress] <old> <new>
   or: git remote remove <name>
   or: git remote set-head <name> (-a | --auto | -d | --delete | <branch>)
   or: git remote [-v | --verbose] show [-n] <name>
   or: git remote prune [-n | --dry-run] <name>
   or: git remote [-v | --verbose] update [-p | --prune] [(<group> | <remote>)...]
   or: git remote set-branches [--add] <name> <branch>...
   or: git remote get-url [--push] [--all] <name>
   or: git remote set-url [--push] <name> <newurl> [<oldurl>]
   or: git remote set-url --add <name> <newurl>
   or: git remote set-url --delete <name> <url>

    -v, --verbose         be verbose; must be placed before a subcommand

gymimena@Imenas-iMac Git % git remote add git-copy https://github.com/Ofallbrains/Another-git-repo.git
gymimena@Imenas-iMac Git % git add .
gymimena@Imenas-iMac Git % git commit -m "Changes to the contact"
[main 869895d] Changes to the contact
 1 file changed, 1 insertion(+)
gymimena@Imenas-iMac Git % git push origin
fatal: The current branch main has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin main

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

gymimena@Imenas-iMac Git % git push origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 334 bytes | 334.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/Ofallbrains/Git-Exercises.git
   a9b0c27..869895d  main -> main
gymimena@Imenas-iMac Git % git push git-copy
Enumerating objects: 42, done.
Counting objects: 100% (42/42), done.
Delta compression using up to 8 threads
Compressing objects: 100% (41/41), done.
Writing objects: 100% (42/42), 7.31 KiB | 7.31 MiB/s, done.
Total 42 (delta 21), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (21/21), done.
To https://github.com/Ofallbrains/Another-git-repo.git
 * [new branch]      main -> main

 ```

 ## Exercise 2

 ``` bash
 