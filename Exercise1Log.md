# GitExercise1


**$ cat > File1.txt**   
This is some dummy text. This is for the Git track.  This is some dummy text.    
This is for the Git track.  ^C   


**$ git init**  
Initialized empty Git repository in /Users/prat14k/Desktop/gitExercise1/.git/    


##### \# Creating A Repository on Github 


**(master)$ git add \***   
 

**(master)$ git commit -am "File1 Added"**   
[master (root-commit) 9fac48b] File1 Added   
 1 file changed, 1 insertion(+)   
 create mode 100644 File1.txt   


**(master)$ cat > File2.txt**   
This is some dummy text. This is for the Git track.This is some dummy text. This is for the Git track.     
This is some dummy text. This is for the Git track.     
This is some dummy text. This is for the Git track.This is some dummy text. This is for the Git track.     
This is some dummy text. This is for the Git track.  ^C   


**(master)$ git status**   
On branch master   
Changes to be committed:   
  (use "git reset HEAD <file>..." to unstage)   
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;new file:   File2.txt   


**(master)$ git diff**   
(END)   


**(master)$ git diff --cached**   
diff --git a/File2.txt b/File2.txt   
new file mode 100644   
index 0000000..7975797   
--- /dev/null   
+++ b/File2.txt   
@@ -0,0 +1,3 @@   
+This is some dummy text. This is for the Git track.This is some dummy text. This is for the Git track. \    
+This is some dummy text. This is for the Git track. \    
+This is some dummy text. This is for the Git track.This is some dummy text. This is for the Git track. \    
(END)   


**(master)$ git commit -am "File2 Added"**   
[master 58e8669] File2 Added   
 1 file changed, 3 insertions(+)   
 create mode 100644 File2.txt   


**(master)$ cat >> File1.txt**   
vinsoll track git   
vinsoll track git   
vinsoll track gitvinsoll track gitvinsoll track git vinsoll track gitvinsoll track git ^C   


**(master)$ cat > File3.txt**   
This is some dummy text. This is for the Git track.  This is some dummy text. This is for the Git track.    
This is some dummy text. This is for the Git track.  This is some dummy text. This is for the Git track.    
This is some dummy text. This is for the Git track.  This is some dummy text. ^C   


**(master)$ git status**   
On branch master   
Changes not staged for commit:   
  (use "git add <file>..." to update what will be committed)   
  (use "git checkout -- <file>..." to discard changes in working directory)   

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;modified:   File1.txt   

Untracked files:   
  (use "git add <file>..." to include in what will be committed)   

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;File3.txt   

no changes added to commit (use "git add" and/or "git commit -a")   


**(master)$ git add File3.txt**   


**(master)$ git diff HEAD**   
diff --git a/File1.txt b/File1.txt   
index 6602fd5..8b9cb29 100644   
--- a/File1.txt   
+++ b/File1.txt   
@@ -1 +1,4 @@   
 This is some dummy text. This is for the Git track.  This is some dummy text. This is for the Git track.     
+vinsoll track git   
+vinsoll track git   
+vinsoll track gitvinsoll track gitvinsoll track git vinsoll track gitvinsoll track git   
diff --git a/File3.txt b/File3.txt   
new file mode 100644   
index 0000000..51f052d   
--- /dev/null   
+++ b/File3.txt   
@@ -0,0 +1,3 @@   
+This is some dummy text. This is for the Git track.  This is some dummy text. This is for the Git track.    
+This is some dummy text. This is for the Git track.  This is some dummy text. This is for the Git track.    
+This is some dummy text. This is for the Git track.  This is some dummy text.   
(END)   


**(master)$ git status**   
On branch master   
Changes to be committed:   
  (use "git reset HEAD <file>..." to unstage)   
   
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;new file:   File3.txt   

Changes not staged for commit:   
  (use "git add <file>..." to update what will be committed)   
  (use "git checkout -- <file>..." to discard changes in working directory)   

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;modified:   File1.txt   


**(master)$ git add \***   


**(master)$ git commit -am "File3 added, File2 modified"**   
[master 9e1663b] File3 added, File2 modified   
 2 files changed, 6 insertions(+)   
 create mode 100644 File3.txt   


**(master)$ cat >> File2.txt**   
nqw,emnwq,enmnwe   
wqenlwkqenlkwe qw elqw elqwe kqw elqew l ^C   


**(master)$ git status**   
On branch master   
Changes not staged for commit:   
  (use "git add <file>..." to update what will be committed)   
  (use "git checkout -- <file>..." to discard changes in working directory)   
   
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;modified:   File2.txt   

no changes added to commit (use "git add" and/or "git commit -a")   


**(master)$ git checkout \-\- File2.txt**   


**(master)$ cat >> File2.txt**   
This is for the Git track   

This is for the Git track   
This is for the Git track   

This is for the Git trackThis is for the Git trackThis is for the Git track   

This is for the Git track   
This is for the Git trackThis is for the Git track   
This is for the Git track ^C   


**(master)$ git add File2.txt**   


**(master)$ git reset HEAD File2.txt**   
Unstaged changes after reset:   
M	File2.txt   


**(master)$ git checkout \-\- File2.txt**   

**(master)$ git status**   
On branch master   
nothing to commit, working tree clean   


**(master)$ cat >> File2.txt**   
This is for the Git track   
This is for the Git trackThis is for the Git trackThis is for the Git track   
This is for the Git track   
This is for the Git track ^C   


**(master)$ cat >> File3.txt**   
This is for the Git track   
This is for the Git trackThis is for the Git track   
This is for the Git trackThis is for the Git trackThis is for the Git trackThis is for the Git track   
This is for the Git track   
This is for the Git trackThis is for the Git trackThis is for the Git track ^C   


**(master)$ cat > File4.txt**   
This is for the Git track   
This is for the Git trackThis is for the Git trackThis is for the Git track   
This is for the Git trackThis is for the Git trackThis is for the Git trackThis is for the Git trackThis is for the Git track   
This is for the Git trackThis is for the Git trackThis is for the Git track   
This is for the Git trackThis is for the Git trackThis is for the Git trackThis is for the Git track ^C   


**(master)$ git status**   
On branch master   
Changes not staged for commit:   
  (use "git add <file>..." to update what will be committed)   
  (use "git checkout -- <file>..." to discard changes in working directory)   
  
  modified:   File2.txt   
	modified:   File3.txt   

Untracked files:   
  (use "git add <file>..." to include in what will be committed)   
  
  File4.txt   

no changes added to commit (use "git add" and/or "git commit -a")   


**(master)$ git add \***   


**(master)$ git commit -am "File 4 added, File2,3 modified"**   
[master 8efbbab] File 4 added, File2,3 modified   
 3 files changed, 14 insertions(+)   
 create mode 100644 File4.txt   


**(master)$ git log**   
commit 8efbbabb6fc2e4421e47b158d1616dfcb2e016ab (HEAD -> master)   
Author: Prateek Sharma <prateek13103718@gmail.com>   
Date:   Thu May 17 19:10:59 2018 +0530   
  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;File 4 added, File2,3 modified   

commit 9e1663b709a826dba167e413e9308d5a367327e6   
Author: Prateek Sharma <prateek13103718@gmail.com>   
Date:   Thu May 17 18:44:01 2018 +0530   

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;File3 added, File2 modified   

commit 58e86699fa8a20730d19dd1358b8f36d903fd350   
Author: Prateek Sharma <prateek13103718@gmail.com>   
Date:   Thu May 17 18:21:25 2018 +0530   

  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;File2 Added   

commit 9fac48b14c463bd9f4c5773911d1dd6cf6e88942   
Author: Prateek Sharma <prateek13103718@gmail.com>   
Date:   Thu May 17 17:59:28 2018 +0530   

  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;File1 Added   
(END)   


**(master)$ git revert HEAD**   
[master 8446daf] Revert "File 4 added, File2,3 modified"   
 3 files changed, 14 deletions(-)   
 delete mode 100644 File4.txt   


**(master)$ git log**   
commit 8446daf7f3c9459ee94a29e8ad91e4938e2b7737 (HEAD -> master)   
Author: Prateek Sharma <prateek13103718@gmail.com>   
Date:   Thu May 17 19:28:27 2018 +0530   

  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Revert "File 4 added, File2,3 modified"   
    
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;This reverts commit 8efbbabb6fc2e4421e47b158d1616dfcb2e016ab.   
    
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Revert   

commit 8efbbabb6fc2e4421e47b158d1616dfcb2e016ab   
Author: Prateek Sharma <prateek13103718@gmail.com>   
Date:   Thu May 17 19:10:59 2018 +0530   

  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;File 4 added, File2,3 modified   

commit 9e1663b709a826dba167e413e9308d5a367327e6   
Author: Prateek Sharma <prateek13103718@gmail.com>   
Date:   Thu May 17 18:44:01 2018 +0530   

  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;File3 added, File2 modified   

commit 58e86699fa8a20730d19dd1358b8f36d903fd350   
Author: Prateek Sharma <prateek13103718@gmail.com>   
Date:   Thu May 17 18:21:25 2018 +0530   

  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;File2 Added   

commit 9fac48b14c463bd9f4c5773911d1dd6cf6e88942   
Author: Prateek Sharma <prateek13103718@gmail.com>   
Date:   Thu May 17 17:59:28 2018 +0530   

  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;File1 Added   
(END)   


**(master)$ git log \-\-oneline**   
8446daf (HEAD -> master) Revert "File 4 added, File2,3 modified"   
8efbbab File 4 added, File2,3 modified   
9e1663b File3 added, File2 modified   
58e8669 File2 Added   
9fac48b File1 Added   
(END)   


**(master)$ git show 9e1663b**   
commit 9e1663b709a826dba167e413e9308d5a367327e6   
Author: Prateek Sharma <prateek13103718@gmail.com>   
Date:   Thu May 17 18:44:01 2018 +0530   

  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;File3 added, File2 modified   

diff --git a/File1.txt b/File1.txt   
index 6602fd5..8b9cb29 100644   
\-\-\- a/File1.txt   
+++ b/File1.txt   
@@ -1 +1,4 @@   
 This is some dummy text. This is for the Git track.  This is some dummy text. This is for the Git track.     
+vinsoll track git   
+vinsoll track git   
+vinsoll track gitvinsoll track gitvinsoll track git vinsoll track gitvinsoll track git   
diff --git a/File3.txt b/File3.txt   
new file mode 100644   
index 0000000..51f052d   
--- /dev/null   
+++ b/File3.txt   
@@ -0,0 +1,3 @@   
+This is some dummy text. This is for the Git track.  This is some dummy text. This is for the Git track.    
+This is some dummy text. This is for the Git track.  This is some dummy text. This is for the Git track.    
+This is some dummy text. This is for the Git track.  This is some dummy text.      


**(master)$ git branch feature1**   


**(master)$ git branch feature2**   


**(master)$ git branch**       
  feature1   
  feature2   
\* master   


**(master)$ git branch -d feature2**   
Deleted branch feature2 (was 8446daf).   


**(master)$ git branch**          
  feature1   
\* master   



**(master)$  git checkout feature1**     
M	File1.txt     
Switched to branch 'feature1'     


**(feature1)$ cat >> File1.txt**      
Vinsol Track Git . Vinsol Track Git     
Vinsol Track Git     
Vinsol Track GitVinsol Track GitVinsol Track Git     
Vinsol Track Git ^C     
 

**(feature1)$ cat File1.txt**     
This is some dummy text. This is for the Git track.  This is some dummy text. This is for the Git track.       
vinsoll track git     
vinsoll track git     
vinsoll track gitvinsoll track gitvinsoll track git vinsoll track gitvinsoll track git     
Dummy Text To add.Dummy Text To add.      
Dummy Text To add.     
Dummy Text To add.Dummy Text To add.     
Vinsol Track Git . Vinsol Track Git     
Vinsol Track Git     
Vinsol Track GitVinsol Track GitVinsol Track Git     
Vinsol Track Git     


**(feature1)$ git add \***                     


**(feature1)$ git commit -m "File1 modified"**                 
[feature1 5bd5276] File1 modified     
 1 file changed, 7 insertions(+)     


**(feature1)$ git checkout master**     
Switched to branch 'master'     



**(master)$ cat >> File1.txt**     
Dummy Text To add.Dummy Text To add.      
Dummy Text To add.     
Dummy Text To add.Dummy Text To add. ^C     
 

**(master)$ cat File1.txt**   
This is some dummy text. This is for the Git track.  This is some dummy text. This is for the Git track.     
vinsoll track git   
vinsoll track git   
vinsoll track gitvinsoll track gitvinsoll track git vinsoll track gitvinsoll track git   
Dummy Text To add.Dummy Text To add.    
Dummy Text To add.   
Dummy Text To add.Dummy Text To add.   



**(master)$ git merge feature1**    
Auto-merging File1.txt    
CONFLICT (content): Merge conflict in File1.txt    
Automatic merge failed; fix conflicts and then commit the result.    


**(master)$ cat File1.txt**    
This is some dummy text. This is for the Git track.  This is some dummy text. This is for the Git track.      
vinsoll track git    
vinsoll track git    
vinsoll track gitvinsoll track gitvinsoll track git vinsoll track gitvinsoll track git    
Dummy Text To add.Dummy Text To add.     
Dummy Text To add.    
Dummy Text To add.Dummy Text To add.    
<<<<<<< HEAD    
\=\=\=\=\=\=\=    
Vinsol Track Git . Vinsol Track Git    
Vinsol Track Git    
Vinsol Track GitVinsol Track GitVinsol Track Git    
Vinsol Track Git    
\>\>\>\>\>\>\> feature1    


**(master)$  subl File1.txt**		


###### \#  After Resolving the conflict     
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;

**(master)$  git add \***                         


**(master)$ git commit -m "Feature1 merged"**     
[master 7c0e2dd] Feature1 merged	



**(master)$ git checkout -b feature2**     
Switched to a new branch 'feature2'     



**(feature2)$ cat >> File3.txt**         
Rebase trial       
Rebase trial Rebase trial Rebase trial       
Rebase trial       
Rebase trial Rebase trial Rebase trial Rebase trial ^C      


**(feature2)$ cat File3.txt**       
This is some dummy text. This is for the Git track.  This is some dummy text. This is for the Git track.       
This is some dummy text. This is for the Git track.  This is some dummy text. This is for the Git track.       
This is some dummy text. This is for the Git track.  This is some dummy text.      
Rebase trial       
Rebase trial Rebase trial Rebase trial       
Rebase trial       
Rebase trial Rebase trial Rebase trial Rebase trial       


**(feature2)$ git add \***      


**(feature2)$ git commit -am "File 3 changes"**      
[feature2 c840091] File 3 changes      
 1 file changed, 4 insertions(+)      


**(feature2)$ git checkout master**      
Switched to branch 'master'      


**(master)$ cat >> File3.txt**      
Conflict Arise ^C      


**(master)$ cat File3.txt**         
This is some dummy text. This is for the Git track.  This is some dummy text. This is for the Git track.       
This is some dummy text. This is for the Git track.  This is some dummy text. This is for the Git track.       
This is some dummy text. This is for the Git track.  This is some dummy text.      
Conflict Arise      


**(master)$ git add File3.txt**       


**(master)$ git commit -m "File 3 changes"**       
[master 07da956] File 3 changes      
 1 file changed, 1 insertion(+)      



**(master)$ git checkout feature2**      
Switched to branch 'feature2'      


**(feature2)$ git rebase master**      
First, rewinding head to replay your work on top of it...      
Applying: File 3 changes      
Using index info to reconstruct a base tree...      
M	File3.txt      
.git/rebase-apply/patch:9: trailing whitespace.      
Rebase trial       
.git/rebase-apply/patch:10: trailing whitespace.      
Rebase trial Rebase trial Rebase trial       
.git/rebase-apply/patch:11: trailing whitespace.      
Rebase trial       
.git/rebase-apply/patch:12: trailing whitespace.      
Rebase trial Rebase trial Rebase trial Rebase trial       
warning: 4 lines add whitespace errors.      
Falling back to patching base and 3-way merge...      
Auto-merging File3.txt      
CONFLICT (content): Merge conflict in File3.txt      
error: Failed to merge in the changes.      
Patch failed at 0001 File 3 changes      
The copy of the patch that failed is found in: .git/rebase-apply/patch      

Resolve all conflicts manually, mark them as resolved with      
"git add/rm <conflicted_files>", then run "git rebase --continue".      
You can instead skip this commit: run "git rebase --skip".      
To abort and get back to the state before "git rebase", run "git rebase --abort".      


**(feature2)$ cat File3.txt**      
This is some dummy text. This is for the Git track.  This is some dummy text. This is for the Git track.       
This is some dummy text. This is for the Git track.  This is some dummy text. This is for the Git track.       
This is some dummy text. This is for the Git track.  This is some dummy text.      
<<<<<<< HEAD      
Conflict Arise      
\=\=\=\=\=\=\=      
Rebase trial       
Rebase trial Rebase trial Rebase trial       
Rebase trial       
Rebase trial Rebase trial Rebase trial Rebase trial       
\>\>\>\>\>\>\> File 3 changes      


**(feature2)$ subl File3.txt**      


###### \#  After Resolving the conflict        
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;

**(feature2)$ cat File3.txt**      
This is some dummy text. This is for the Git track.  This is some dummy text. This is for the Git track.       
This is some dummy text. This is for the Git track.  This is some dummy text. This is for the Git track.       
This is some dummy text. This is for the Git track.  This is some dummy text.      
      
Conflict Removed      

Rebase trial       


**(feature2)$ git add File3.txt**      


**(feature2)$ git rebase --continue**      
Applying: File 3 changes      


**(feature2)$ git checkout master**      
Switched to branch 'master'      


**(master)$ git merge feature2**      
Updating 07da956..25404a8      
Fast-forward      
 File3.txt | 5 ++++-      
 1 file changed, 4 insertions(+), 1 deletion(-)      



**(master)$ cat >> File1.txt**      
Stash Trial        
Stash Trial Stash Trial Stash Trial Stash Trial       
Stash Trial ^C      


**(master)$ git log --oneline**      
25404a8 (HEAD -> master, feature2) File 3 changes      
07da956 File 3 changes      
7c0e2dd Feature1 merged      
e800a04 File1 modified      
5bd5276 (feature1) File1 modified      
8446daf Revert "File 4 added, File2,3 modified"      
8efbbab File 4 added, File2,3 modified      
9e1663b File3 added, File2 modified      
58e8669 File2 Added      
9fac48b File1 Added      
(END)      



**(master)$ git checkout e800a04**      
error: Your local changes to the following files would be overwritten by checkout:      
	File1.txt      
Please commit your changes or stash them before you switch branches.      
Aborting      


**(master)$ git stash**      
Saved working directory and index state WIP on master: 25404a8 File 3 changes      


**(master)$ git checkout e800a04**      
Note: checking out 'e800a04'.      

You are in 'detached HEAD' state. You can look around, make experimental      
changes and commit them, and you can discard any commits you make in this      
state without impacting any branches by performing another checkout.      

If you want to create a new branch to retain commits you create, you may      
do so (now or later) by using -b with the checkout command again. Example:      
      
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;git checkout -b <new-branch-name>      

HEAD is now at e800a04... File1 modified      

###### \#  After Doing your work      
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;

**(e800a04)$ git checkout master**       
Switched to branch 'master'      


**(master)$ git status**      
On branch master      
nothing to commit, working tree clean      


**(master)$ git stash pop**      
On branch master      
Changes not staged for commit:      
  (use "git add <file>..." to update what will be committed)      
  (use "git checkout -- <file>..." to discard changes in working directory)      

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;modified:   File1.txt      

no changes added to commit (use "git add" and/or "git commit -a")      



**(master)$ git add \***      

**(master)$ git commit -m "Stashed n final commit"**      
[master ef06343] Stashed n final commit      
 1 file changed, 3 insertions(+), 1 deletion(-)      


**(master)$ git remote add origin git@github.com:prat14k/GitExercise1.git**      


**(master)$ git pull origin master**      
warning: no common commits      
remote: Counting objects: 20, done.      
remote: Compressing objects: 100% (12/12), done.      
remote: Total 20 (delta 3), reused 0 (delta 0), pack-reused 0      
Unpacking objects: 100% (20/20), done.      
From github.com:prat14k/GitExercise1      
 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;\* branch            master     -> FETCH_HEAD      
 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;\* [new branch]      master     -> origin/master      
fatal: refusing to merge unrelated histories      


**(master)$ git pull --allow-unrelated-histories origin master**      
From github.com:prat14k/GitExercise1      
 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;\* branch            master     -> FETCH_HEAD      
Merge made by the 'recursive' strategy.      
 README.md | 458 ++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++      
 1 file changed, 458 insertions(+)      
 create mode 100644 README.md      


**(master)$ git push origin master**      
Counting objects: 36, done.      
Delta compression using up to 8 threads.      
Compressing objects: 100% (35/35), done.      
Writing objects: 100% (36/36), 3.31 KiB | 1.10 MiB/s, done.      
Total 36 (delta 16), reused 0 (delta 0)      
remote: Resolving deltas: 100% (16/16), done.      
To github.com:prat14k/GitExercise1.git      
   6c5ddcf..178290c  master -> master      


**(master)$ git checkout feature1**      
Switched to branch 'feature1'      


**(feature1)$ git push origin feature1**      
Total 0 (delta 0), reused 0 (delta 0)      
To github.com:prat14k/GitExercise1.git      
 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;\* [new branch]      feature1 -> feature1      


**(feature1)$ git push origin feature2**      
Total 0 (delta 0), reused 0 (delta 0)      
To github.com:prat14k/GitExercise1.git      
 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;\* [new branch]      feature2 -> feature2      


