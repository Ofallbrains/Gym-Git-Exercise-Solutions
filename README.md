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