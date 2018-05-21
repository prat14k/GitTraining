**$ mkdir project1 project2**           


**$ git init**          
Initialized empty Git repository in /Users/prat14k/Desktop/gitExercise3/project1/.git/          


**(master)$ git checkout -b staging**          
Switched to a new branch 'staging'          
 

**(staging)$ cat > Test1.txt**          
This is the first commit ^C          


**(staging)$ git add \***          


**(staging)$ git commit -m "First Commit"**          
[staging (root-commit) b280cf8] First Commit          
 1 file changed, 1 insertion(+)          
 create mode 100644 Test1.txt          



**(staging)$ git remote add origin git@github.com:prat14k/Test_Project.git**          


**(staging)$ git push origin staging**          
Counting objects: 3, done.          
Writing objects: 100% (3/3), 243 bytes | 243.00 KiB/s, done.          
Total 3 (delta 0), reused 0 (delta 0)          
To github.com:prat14k/Test_Project.git          
 \* [new branch]      staging -> staging          


**(staging)$ cd ../project2**          


**$ git clone git@github.com:prat14k/Test_Project.git .**          
Cloning into '.'...          
remote: Counting objects: 3, done.          
remote: Total 3 (delta 0), reused 3 (delta 0), pack-reused 0          
Receiving objects: 100% (3/3), done.          


**(staging)$ cat > Test1.txt**                    
This is second commit ^C          


**(staging)$ cat Test1.txt**          
This is second commit          


**(staging)$ git add\***          


**(staging)$ git commit -m "Second Commit"**          
[staging 38a48df] Second Commit          
 1 file changed, 1 insertion(+), 1 deletion(-)          


**(staging)$ git push origin staging**          
Counting objects: 3, done.          
Writing objects: 100% (3/3), 269 bytes | 269.00 KiB/s, done.          
Total 3 (delta 0), reused 0 (delta 0)          
To github.com:prat14k/Test_Project.git          
   b280cf8..38a48df  staging -> staging          


**(staging)$ cd ../project1**          


**(staging)$ cat > Test1.txt**          
This is third commit ^C          


**(staging)$ git commit -am "Third commit overrall"**          
[staging 6adb522] Third commit overrall          
 1 file changed, 1 insertion(+), 1 deletion(-)          


**(staging)$ git push origin staging**          
To github.com:prat14k/Test_Project.git          
 ! [rejected]        staging -> staging (fetch first)          
error: failed to push some refs to 'git@github.com:prat14k/Test_Project.git'          
hint: Updates were rejected because the remote contains work that you do          
hint: not have locally. This is usually caused by another repository pushing          
hint: to the same ref. You may want to first integrate the remote changes          
hint: (e.g., 'git pull ...') before pushing again.          
hint: See the 'Note about fast-forwards' in 'git push --help' for details.          


**(staging)$ git pull origin staging**          
remote: Counting objects: 3, done.          
remote: Total 3 (delta 0), reused 3 (delta 0), pack-reused 0          
Unpacking objects: 100% (3/3), done.          
From github.com:prat14k/Test_Project          
 \* branch            staging    -> FETCH_HEAD          
   b280cf8..38a48df  staging    -> origin/staging          
Auto-merging Test1.txt          
CONFLICT (content): Merge conflict in Test1.txt          
Automatic merge failed; fix conflicts and then commit the result.          
 

**(staging)$ cat Test1.txt**          
<<<<<<< HEAD          
This is third commit          
\=\=\=\=\=\=\=          
This is second commit          
\>\>\>\>\>\>\> 38a48df9a0166e13241ee64f525d1d0aeb1240dd          
 

**(staging)$ subl Test1.txt**          


**(staging)$ git add Test1.txt**          


**(staging)$ git commit -am "Pull Merge Conflict Removed"**          
[staging e8b5e48] Pull Merge Conflict Removed          


**(staging)$ git push origin staging**          
Counting objects: 6, done.          
Delta compression using up to 8 threads.          
Compressing objects: 100% (3/3), done.          
Writing objects: 100% (6/6), 581 bytes | 581.00 KiB/s, done.          
Total 6 (delta 0), reused 0 (delta 0)          
To github.com:prat14k/Test_Project.git          
   38a48df..e8b5e48  staging -> staging          



**(staging)$ git checkout master**          
error: pathspec 'master' did not match any file(s) known to git.          


**(staging)$ git checkout -b master**          
Switched to a new branch 'master'          


**(master)$ git merge staging**          
Already up to date.          


**(master)$ git push origin master**          
Total 0 (delta 0), reused 0 (delta 0)       
To github.com:prat14k/Test_Project.git       
 \* [new branch]      master -> master       



**$ git push origin master**           
Total 0 (delta 0), reused 0 (delta 0)         
To github.com:prat14k/Test_Project.git         
 \* [new branch]      master -> master         


**$ git checkout -b testing**                    
Switched to a new branch 'testing'         


**$ cat Test1.txt**                    

This is third commit.          
Second commit was from project2/         


**$ subl Test1.txt**                             


**$ git commit -am "char A"**                    
[testing 1624cc7] char A         
 1 file changed, 1 insertion(+), 4 deletions(-)         


**$ git commit -am "char B"**           
[testing d63e6b5] char B         
 1 file changed, 1 insertion(+), 1 deletion(-)         


**$ git commit -am "char C"**           
[testing bf42bfd] char C         
 1 file changed, 1 insertion(+), 1 deletion(-)         


**$ git commit -am "char D"**           
[testing f1640ff] char D         
 1 file changed, 1 insertion(+), 1 deletion(-)         


**$ git commit -am "char E"**           
[testing c33347b] char E         
 1 file changed, 1 insertion(+), 1 deletion(-)         


**$ git commit -am "char F"**           
[testing 8c4c297] char F         
 1 file changed, 1 insertion(+), 1 deletion(-)         


**$ git commit -am "char G"**           
[testing 71bf3a8] char G         
 1 file changed, 1 insertion(+), 1 deletion(-)         


**$ git checkout master**               
Switched to branch 'master'         


**$ git push origin testing**           
Counting objects: 21, done.         
Delta compression using up to 8 threads.         
Compressing objects: 100% (7/7), done.         
Writing objects: 100% (21/21), 1.60 KiB | 546.00 KiB/s, done.         
Total 21 (delta 0), reused 0 (delta 0)         
To github.com:prat14k/Test_Project.git         
 \* [new branch]      testing -> testing         


**$ git checkout master**           
Switched to branch 'master'         


**$ cat Test1.txt**            

This is third commit.          
Second commit was from project2/         



**$ subl Test1.txt**            


**$ git commit -am "number 1"**           
[master 03c296f] number 1         
 1 file changed, 1 insertion(+), 4 deletions(-)         


**$ git commit -am "number 2"**           
[master 0b74328] number 2         
 1 file changed, 1 insertion(+), 1 deletion(-)         


**$ git commit -am "number 3"**           
[master 9e85d83] number 3         
 1 file changed, 1 insertion(+), 1 deletion(-)         


**$ git commit -am "number 4"**           
[master 377acc1] number 4         
 1 file changed, 1 insertion(+), 1 deletion(-)         


**$ git commit -am "number 5"**           
[master 80c7a1d] number 5         
 1 file changed, 1 insertion(+), 1 deletion(-)         


**$ git commit -am "number 6"**           
[master 23201ab] number 6         
 1 file changed, 1 insertion(+), 1 deletion(-)         


**$ git commit -am "number 7"**           
[master 8c9b791] number 7         
 1 file changed, 1 insertion(+), 1 deletion(-)         


**$ git checkout testing**           
Switched to branch 'testing'         


**$ git rebase master**           
First, rewinding head to replay your work on top of it...         
Applying: char A         
Using index info to reconstruct a base tree...         
M	Test1.txt         
Falling back to patching base and 3-way merge...         
Auto-merging Test1.txt         
CONFLICT (content): Merge conflict in Test1.txt         
error: Failed to merge in the changes.         
Patch failed at 0001 char A         
The copy of the patch that failed is found in: .git/rebase-apply/patch         

Resolve all conflicts manually, mark them as resolved with         
"git add/rm <conflicted_files>", then run "git rebase --continue".         
You can instead skip this commit: run "git rebase --skip".         
To abort and get back to the state before "git rebase", run "git rebase --abort".         


**$ git rebase --continue**            
Test1.txt: needs merge         
You must edit all merge conflicts and then         
mark them as resolved using git add         


**$ cat Test1.txt**            
<<<<<<< HEAD         
7 is a number         
\=\=\=\=\=\=\=         
A is a character         
\>\>\>\>\>\>\> char A         


**$ git add \***           


**$ git rebase --continue**           
Applying: char A         
Applying: char B         
Using index info to reconstruct a base tree...         
M	Test1.txt         
Falling back to patching base and 3-way merge...         
Auto-merging Test1.txt         
CONFLICT (content): Merge conflict in Test1.txt         
error: Failed to merge in the changes.         
Patch failed at 0002 char B         
The copy of the patch that failed is found in: .git/rebase-apply/patch         

Resolve all conflicts manually, mark them as resolved with         
"git add/rm <conflicted_files>", then run "git rebase --continue".         
You can instead skip this commit: run "git rebase --skip".         
To abort and get back to the state before "git rebase", run "git rebase --abort".         


**$ git add \***           


**$ git rebase --continue**           
Applying: char B         
Applying: char C         
Using index info to reconstruct a base tree...         
M	Test1.txt         
Falling back to patching base and 3-way merge...         
Auto-merging Test1.txt         
CONFLICT (content): Merge conflict in Test1.txt         
error: Failed to merge in the changes.         
Patch failed at 0003 char C         
The copy of the patch that failed is found in: .git/rebase-apply/patch         

Resolve all conflicts manually, mark them as resolved with         
"git add/rm <conflicted_files>", then run "git rebase --continue".         
You can instead skip this commit: run "git rebase --skip".         
To abort and get back to the state before "git rebase", run "git rebase --abort".         


**$ git add \***           


**$ git rebase --continue**           
Applying: char C         
Applying: char D         
Using index info to reconstruct a base tree...         
M	Test1.txt         
Falling back to patching base and 3-way merge...         
Auto-merging Test1.txt         
CONFLICT (content): Merge conflict in Test1.txt         
error: Failed to merge in the changes.         
Patch failed at 0004 char D         
The copy of the patch that failed is found in: .git/rebase-apply/patch         

Resolve all conflicts manually, mark them as resolved with         
"git add/rm <conflicted_files>", then run "git rebase --continue".         
You can instead skip this commit: run "git rebase --skip".         
To abort and get back to the state before "git rebase", run "git rebase --abort".         


**$ git add \***           


**$ git rebase --continue**           
Applying: char D         
No changes - did you forget to use 'git add'?         
If there is nothing left to stage, chances are that something else         
already introduced the same changes; you might want to skip this patch.         

Resolve all conflicts manually, mark them as resolved with         
"git add/rm <conflicted_files>", then run "git rebase --continue".         
You can instead skip this commit: run "git rebase --skip".         
To abort and get back to the state before "git rebase", run "git rebase --abort".         


**$ git rebase --skip**           
Applying: char E         
Using index info to reconstruct a base tree...         
M	Test1.txt         
Falling back to patching base and 3-way merge...         
Auto-merging Test1.txt         
CONFLICT (content): Merge conflict in Test1.txt         
error: Failed to merge in the changes.         
Patch failed at 0005 char E         
The copy of the patch that failed is found in: .git/rebase-apply/patch         

Resolve all conflicts manually, mark them as resolved with         
"git add/rm <conflicted_files>", then run "git rebase --continue".         
You can instead skip this commit: run "git rebase --skip".         
To abort and get back to the state before "git rebase", run "git rebase --abort".         


**$ git add \***                       


**$ git rebase --continue**           
Applying: char E         
Applying: char F         
Using index info to reconstruct a base tree...         
M	Test1.txt         
Falling back to patching base and 3-way merge...         
Auto-merging Test1.txt         
CONFLICT (content): Merge conflict in Test1.txt         
error: Failed to merge in the changes.         
Patch failed at 0006 char F         
The copy of the patch that failed is found in: .git/rebase-apply/patch         

Resolve all conflicts manually, mark them as resolved with         
"git add/rm <conflicted_files>", then run "git rebase --continue".         
You can instead skip this commit: run "git rebase --skip".         
To abort and get back to the state before "git rebase", run "git rebase --abort".         


**$ git rebase --skip**            
Applying: char G         
Using index info to reconstruct a base tree...         
M	Test1.txt         
Falling back to patching base and 3-way merge...         
Auto-merging Test1.txt         
CONFLICT (content): Merge conflict in Test1.txt         
error: Failed to merge in the changes.         
Patch failed at 0007 char G         
The copy of the patch that failed is found in: .git/rebase-apply/patch         

Resolve all conflicts manually, mark them as resolved with         
"git add/rm <conflicted_files>", then run "git rebase --continue".         
You can instead skip this commit: run "git rebase --skip".         
To abort and get back to the state before "git rebase", run "git rebase --abort".         


**$ git add \***           


**$ git rebase --continue**           
Applying: char G         


**$ git checkout master**           
Switched to branch 'master'         


**$ git merge testing**           
Updating 8c9b791..77dbee4         
Fast-forward         
 Test1.txt | 7 ++++++-         
 1 file changed, 6 insertions(+), 1 deletion(-)         



**$ cd ../project2**           


**$ git checkout --track origin/testing**           
fatal: 'origin/testing' is not a commit and a branch 'testing' cannot be created from it          


**$ git --help branch**                             


**$ git branch --track testing origin/testing**                     
error: the requested upstream branch 'origin/testing' does not exist          
hint:           
hint: If you are planning on basing your work on an upstream          
hint: branch that already exists at the remote, you may need to          
hint: run "git fetch" to retrieve it.          
hint:           
hint: If you are planning to push out a new local branch that          
hint: will track its remote counterpart, you may want to use          
hint: "git push -u" to set the upstream config as you push.          


**$ git fetch origin**                     
remote: Counting objects: 27, done.          
remote: Compressing objects: 100% (10/10), done.          
Unpacking objects: 100% (27/27), done.          
remote: Total 27 (delta 0), reused 27 (delta 0), pack-reused 0          
From github.com:prat14k/Test_Project          
   38a48df..e8b5e48  staging    -> origin/staging          
 * [new branch]      master     -> origin/master          
 * [new branch]      testing    -> origin/testing          


**$ git branch --track testing origin/testing**                     
Branch 'testing' set up to track remote branch 'testing' from 'origin'.          


**$ git checkout master**           
Branch 'master' set up to track remote branch 'master' from 'origin'.          
Switched to a new branch 'master'          


**$ git merge testing**           
Updating e8b5e48..71bf3a8          
Fast-forward          
 Test1.txt | 5 +----          
 1 file changed, 1 insertion(+), 4 deletions(-)          




