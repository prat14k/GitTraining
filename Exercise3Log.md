**$ mkdir project1 project2**           

**$ cd project1**

**$ git init**          
Initialized empty Git repository in /Users/prat14k/Desktop/gitExercise3/project1/.git/      

&nbsp;    
##### \# Created Repo named "Test_Project" on Github
&nbsp; 

**(master)$ git remote add origin git@github.com:prat14k/Test_Project.git**         

**(master)$ git checkout -b staging**          
Switched to a new branch 'staging'          
 

**(staging)$ cat > Test1.txt**          
This is the first commit ^C          

**(staging)$ git status**    
On branch staging
Untracked files:
  (use "git add <file>..." to include in what will be committed)

&nbsp;&nbsp;&nbsp;&nbsp;Test1.txt

nothing added to commit but untracked files present (use "git add" to track)

**(staging)$ git add Test1.txt**          


**(staging)$ git commit -m "First Commit"**          
git commit -m "First Commit"
[staging 5d3c15b] First Commit
 1 file changed, 1 insertion(+)
 create mode 100644 Test1.txt   


**(staging)$ git push origin staging**          
Counting objects: 3, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 306 bytes | 306.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To github.com:prat14k/Test_Project.git          
 &nbsp;&nbsp;&nbsp;&nbsp;\* [new branch]      staging -> staging          


**(staging)$ cd ../project2**          


**$ git clone git@github.com:prat14k/Test_Project.git .**          
Cloning into '.'...
remote: Counting objects: 6, done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 6 (delta 0), reused 6 (delta 0), pack-reused 0
Receiving objects: 100% (6/6), done.            

**(master)$ git checkout staging**    
Branch 'staging' set up to track remote branch 'staging' from 'origin'.
Switched to a new branch 'staging'

**(staging)$ cat > Test1.txt**                    
This is second commit ^C          


**(staging)$ cat Test1.txt**          
This is second commit          

**(staging)$ git status**      
On branch staging
Your branch is up to date with 'origin/staging'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

&nbsp;&nbsp;&nbsp;&nbsp;modified:   Test1.txt

no changes added to commit (use "git add" and/or "git commit -a")

**(staging)$ git add Test1.txt**          


**(staging)$ git commit -m "Second Commit"**          
[staging 3601245] Second Commit
 1 file changed, 1 insertion(+), 1 deletion(-)        


**(staging)$ git push origin staging**          
Counting objects: 3, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 303 bytes | 303.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To github.com:prat14k/Test_Project.git
&nbsp;&nbsp;&nbsp;&nbsp;5d3c15b..3601245  staging -> staging         


**(staging)$ cd \.\.\/project1**          


**(staging)$ cat > Test1.txt**          
This is third commit ^C          


**(staging)$ git commit -am "Third commit overrall"**          
[staging 0c79817] Third commit overrall
 1 file changed, 1 insertion(+), 1 deletion(-)          


**(staging)$ git push origin staging**          
To github.com:prat14k/Test_Project.git
&nbsp;&nbsp;! [rejected]  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;      staging -> staging (fetch first)
error: failed to push some refs to 'git@github.com:prat14k/Test_Project.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.          

&nbsp;&nbsp;&nbsp;&nbsp;
##### \# Push Operation Not successful because we had already pushed changes from another local repo and we didn't take a pull from the repo to get the latest pushed changes to the branch.
 &nbsp;&nbsp;&nbsp;&nbsp;
 
**(staging)$ git checkout master**          
Switched to branch 'master'          


**(master)$ git merge staging**          
Updating 070bb4d..0c79817
Fast-forward
 &nbsp;&nbsp;Test1.txt | 1 +
 &nbsp;&nbsp;1 file changed, 1 insertion(+)
 &nbsp;&nbsp;create mode 100644 Test1.txt        


**(testing)$ git checkout -b testing**                    
Switched to a new branch 'testing'         


**(testing)$ cat Test1.txt**                    

This is third commit.          


**(testing)$ subl Test1.txt**                             

**(testing)$ git status**                                   
On branch testing
Changes not staged for commit:
  &nbsp;&nbsp;(use "git add <file>..." to update what will be committed)
  &nbsp;&nbsp;(use "git checkout -- <file>..." to discard changes in working directory)
    
&nbsp;&nbsp;&nbsp;&nbsp;modified:   Test1.txt

no changes added to commit (use "git add" and/or "git commit -a")

**(testing)$ git commit -am "char A"**                    
[testing b2aa562] char A
 1 file changed, 1 insertion(+), 1 deletion(-)         


**(testing)$ git commit -am "char B"**           
[testing 0517657] char B       
 1 file changed, 1 insertion(+), 1 deletion(-)         


**(testing)$ git commit -am "char C"**           
[testing 65f2827] char C         
 1 file changed, 1 insertion(+), 1 deletion(-)         


**(testing)$ git commit -am "char D"**           
[testing 6cc8a5a] char D         
 1 file changed, 1 insertion(+), 1 deletion(-)         


**(testing)$ git commit -am "char E"**           
[testing a3bcc34] char E         
 1 file changed, 1 insertion(+), 1 deletion(-)         


**(testing)$ git commit -am "char F"**           
[testing c428f58] char F         
 1 file changed, 1 insertion(+), 1 deletion(-)         


**(testing)$ git commit -am "char G"**           
[testing 3fb2112] char G        
 1 file changed, 1 insertion(+), 1 deletion(-)         

**(testing)$ git push origin testing**           
Counting objects: 21, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (14/14), done.
Writing objects: 100% (21/21), 1.82 KiB | 933.00 KiB/s, done.
Total 21 (delta 0), reused 0 (delta 0)
To github.com:prat14k/Test_Project.git
 &nbsp;&nbsp;\* [new branch]      testing -> testing  
 
 
**(testing)$ git checkout master**           
Switched to branch 'master'         


**(master)$ cat Test1.txt**            
This is third commit.             


**(master)$ subl Test1.txt**            

**(master)$ git status**
On branch master
Changes not staged for commit:
  &nbsp;&nbsp;&nbsp;&nbsp;(use "git add <file>..." to update what will be committed)
  &nbsp;&nbsp;&nbsp;&nbsp;(use "git checkout -- <file>..." to discard changes in working directory)

&nbsp;&nbsp;&nbsp;&nbsp;modified:   Test1.txt

no changes added to commit (use "git add" and/or "git commit -a")

**(master)$ git commit -am "number 1"**           
[master 0f558b5] number 1        
 1 file changed, 1 insertion(+), 1 deletions(-)         


**(master)$ git commit -am "number 2"**           
[master 4410075] number 2        
 1 file changed, 1 insertion(+), 1 deletion(-)         


**(master)$ git commit -am "number 3"**           
[master ce70dfc] number 3         
 1 file changed, 1 insertion(+), 1 deletion(-)         


**(master)$ git commit -am "number 4"**           
[master 67d8415] number 4         
 1 file changed, 1 insertion(+), 1 deletion(-)         


**(master)$ git commit -am "number 5"**           
[master 509f57a] number 5         
 1 file changed, 1 insertion(+), 1 deletion(-)         


**(master)$ git commit -am "number 6"**           
[master 1cf0301] number 6         
 1 file changed, 1 insertion(+), 1 deletion(-)         


**(master)$ git commit -am "number 7"**           
[master b702c7d] number 7         
 1 file changed, 1 insertion(+), 1 deletion(-)         

**(master)$ git push origin master**     
Counting objects: 21, done.         
Delta compression using up to 8 threads.         
Compressing objects: 100% (14/14), done.         
Writing objects: 100% (21/21), 1.80 KiB | 923.00 KiB/s, done.         
Total 21 (delta 0), reused 0 (delta 0)         
To github.com:prat14k/Test_Project.git         
&nbsp;&nbsp;&nbsp;&nbsp;0c79817..b702c7d  master -> master         


**(f774842)$ subl Test1.txt**     



**(master)$ git rebase testing**           
First, rewinding head to replay your work on top of it...
Applying: number 1
Using index info to reconstruct a base tree...
M	Test1.txt
Falling back to patching base and 3-way merge...
Auto-merging Test1.txt
CONFLICT (content): Merge conflict in Test1.txt
error: Failed to merge in the changes.
Patch failed at 0001 number 1
The copy of the patch that failed is found in: .git/rebase-apply/patch

Resolve all conflicts manually, mark them as resolved with
"git add/rm <conflicted_files>", then run "git rebase --continue".
You can instead skip this commit: run "git rebase --skip".
To abort and get back to the state before "git rebase", run "git rebase --abort".

**$ git add Test1.txt**           

**$ git rebase --continue**           
Applying: number 1
Applying: number 2
Using index info to reconstruct a base tree...
M	Test1.txt
Falling back to patching base and 3-way merge...
Auto-merging Test1.txt
CONFLICT (content): Merge conflict in Test1.txt
error: Failed to merge in the changes.
Patch failed at 0002 number 2
The copy of the patch that failed is found in: .git/rebase-apply/patch

Resolve all conflicts manually, mark them as resolved with
"git add/rm <conflicted_files>", then run "git rebase --continue".
You can instead skip this commit: run "git rebase --skip".
To abort and get back to the state before "git rebase", run "git rebase --abort".

**$ git add Test1.txt**             

**$ git rebase --continue**           
Applying: number 2
Applying: number 3
Using index info to reconstruct a base tree...
M	Test1.txt
Falling back to patching base and 3-way merge...
Auto-merging Test1.txt
CONFLICT (content): Merge conflict in Test1.txt
error: Failed to merge in the changes.
Patch failed at 0003 number 3
The copy of the patch that failed is found in: .git/rebase-apply/patch

Resolve all conflicts manually, mark them as resolved with
"git add/rm <conflicted_files>", then run "git rebase --continue".
You can instead skip this commit: run "git rebase --skip".
To abort and get back to the state before "git rebase", run "git rebase --abort".


**$ git add Test1.txt**           

**$ git rebase --continue**           
Applying: number 3
Applying: number 4
Using index info to reconstruct a base tree...
M	Test1.txt
Falling back to patching base and 3-way merge...
Auto-merging Test1.txt
CONFLICT (content): Merge conflict in Test1.txt
error: Failed to merge in the changes.
Patch failed at 0004 number 4
The copy of the patch that failed is found in: .git/rebase-apply/patch

Resolve all conflicts manually, mark them as resolved with
"git add/rm <conflicted_files>", then run "git rebase --continue".
You can instead skip this commit: run "git rebase --skip".
To abort and get back to the state before "git rebase", run "git rebase --abort".

**$ git add Test1.txt**           

**$ git rebase --continue**           
Applying: number 4
Applying: number 5
Using index info to reconstruct a base tree...
M	Test1.txt
Falling back to patching base and 3-way merge...
Auto-merging Test1.txt
CONFLICT (content): Merge conflict in Test1.txt
error: Failed to merge in the changes.
Patch failed at 0005 number 5
The copy of the patch that failed is found in: .git/rebase-apply/patch

Resolve all conflicts manually, mark them as resolved with
"git add/rm <conflicted_files>", then run "git rebase --continue".
You can instead skip this commit: run "git rebase --skip".
To abort and get back to the state before "git rebase", run "git rebase --abort".

**$ git add Test1.txt**           

**$ git rebase --continue**           
Applying: number 5
Applying: number 6
Using index info to reconstruct a base tree...
M	Test1.txt
Falling back to patching base and 3-way merge...
Auto-merging Test1.txt
CONFLICT (content): Merge conflict in Test1.txt
error: Failed to merge in the changes.
Patch failed at 0006 number 6
The copy of the patch that failed is found in: .git/rebase-apply/patch

Resolve all conflicts manually, mark them as resolved with
"git add/rm <conflicted_files>", then run "git rebase --continue".
You can instead skip this commit: run "git rebase --skip".
To abort and get back to the state before "git rebase", run "git rebase --abort".

**$ git add Test1.txt**        

**$ git rebase --continue**           
Applying: number 6
Applying: number 7
Using index info to reconstruct a base tree...
M	Test1.txt
Falling back to patching base and 3-way merge...
Auto-merging Test1.txt
CONFLICT (content): Merge conflict in Test1.txt
error: Failed to merge in the changes.
Patch failed at 0007 number 7
The copy of the patch that failed is found in: .git/rebase-apply/patch

Resolve all conflicts manually, mark them as resolved with
"git add/rm <conflicted_files>", then run "git rebase --continue".
You can instead skip this commit: run "git rebase --skip".
To abort and get back to the state before "git rebase", run "git rebase --abort".

**$ git add Test1.txt**           

**$ git rebase --continue**           
Applying: number 7
    

    
 
**(master)$ cd \.\.\/project2**           

**(staging)$ git branch --track testing origin/testing**                     
error: the requested upstream branch 'origin/testing' does not exist          
hint:           
hint: If you are planning on basing your work on an upstream          
hint: branch that already exists at the remote, you may need to          
hint: run "git fetch" to retrieve it.          
hint:           
hint: If you are planning to push out a new local branch that          
hint: will track its remote counterpart, you may want to use          
hint: "git push -u" to set the upstream config as you push.          

**(staging)$ git fetch origin**                     
remote: Counting objects: 45, done.
remote: Compressing objects: 100% (30/30), done.
remote: Total 45 (delta 1), reused 44 (delta 0), pack-reused 0
Unpacking objects: 100% (45/45), done.
From github.com:prat14k/Test_Project
   &nbsp;&nbsp;&nbsp;&nbsp;070bb4d..f774842  master     -> origin/master
 &nbsp;&nbsp;&nbsp;&nbsp;\* [new branch]      testing    -> origin/testing        


**(staging)$ git branch --track testing origin/testing**     
Branch 'testing' set up to track remote branch 'testing' from 'origin'.          


**(staging)$ git checkout master**           
Switched to branch 'master'
Your branch is behind 'origin/master' by 9 commits, and can be fast-forwarded.
  &nbsp;&nbsp;&nbsp;&nbsp;(use "git pull" to update your local branch)       


**(master)$ git merge testing**       
Updating 070bb4d..8f3c2fe
Fast-forward
 &nbsp;&nbsp;Test1.txt | 1 +
 &nbsp;&nbsp;1 file changed, 1 insertion(+)
 &nbsp;&nbsp;create mode 100644 Test1.txt
        
