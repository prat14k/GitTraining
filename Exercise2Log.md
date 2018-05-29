**$ cat > File1.txt**      
Exercise 2       
Git tag Exercise 2      
Git track ^C      

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
##### \# Created a Repository on Github
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;

**$ git init**      
Initialized empty Git repository in /Users/prat14k/Desktop/gitExercise2/.git/      


**(master)$ cat > File2.txt**      
Git track      
Git trackGit track Git trackGit track      
Git track ^C      


**(master)$ git status**            
On branch master      

No commits yet      

Untracked files:      
  (use "git add <file>..." to include in what will be committed)      

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;File1.txt      
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;File2.txt      

nothing added to commit but untracked files present (use "git add" to track)      


**(master)$ git add \***                  


**(master)$ git commit -m "Initial Commit"**            
[master (root-commit) 39a4d4c] Initial Commit      
 2 files changed, 6 insertions(+)      
 create mode 100644 File1.txt      
 create mode 100644 File2.txt      


**(master)$ git tag -a 1.0.0 -m "Version 1.0.0"**            


**(master)$ nano File1.txt**            


**(master)$ cat File1.txt**            
Vinsol track Exercise 2            
Git Exercise 2            
Git             
jkabsd            
sd            
askd            
sadk sd a            


sakdnas            
kdns            
dkasnd            
aksda            
sdsandasdknasd lsa dj dka dslkands            


**(master)$ nano File2.txt**            


**(master)$ cat File2.txt**            
dkjs ds            
fsdf            
 dslf sdf m             

;k             

k  d;f ;ld fs;df            
k             
kd f            
 fksd f            
dsf             
d             


Git track            
Git track            
ad,'asd            
ckGit trat track            



**(master)$ git status**          
On branch master		
Changes not staged for commit:		
  (use "git add <file>..." to update what will be committed)		
  (use "git checkout -- <file>..." to discard changes in working directory)		

   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;modified:   File1.txt		
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;modified:   File2.txt		

no changes added to commit (use "git add" and/or "git commit -a")		


**(master)$ git add \*** 	 


**(master)$ git commit -m "Changes and improvements"**     
[master 731bba8] Changes and improvements      	
 2 files changed, 30 insertions(+), 4 deletions(-)		


**(master)$ git tag -a 1.0.1 -m "Version 1.0.1"**		


**(master)$ cat > File3.txt**       
File 3        
new tag 	       	       
git tags tack ^C	       	       


**(master)$ git add \***		       		


**(master)$ git commit -m "New Feature"**             
[master d9ee0d7] New Feature             
 1 file changed, 3 insertions(+)	              	       
 create mode 100644 File3.txt                     
       

**(master)$ git tag -a 1.1.0 -m "Version 1.1.0"**          


**(master)$ git tag**		                   
1.0.0		              
1.0.1		              
1.1.0		              
(END)		                     


**(master)$ git checkout 1.0.1**       	       	          
Note: checking out '1.0.1'.	                 

You are in 'detached HEAD' state. You can look around, make experimental		              
changes and commit them, and you can discard any commits you make in this		              
state without impacting any branches by performing another checkout.		              

If you want to create a new branch to retain commits you create, you may		              
do so (now or later) by using -b with the checkout command again. Example:		              

  git checkout -b <new-branch-name>		              

HEAD is now at 731bba8... Changes and improvements	                    


**(master)$ git checkout -b v1.0.1_FIX**	                                 
Switched to a new branch 'v1.0.1_FIX'	              	       


**(master)$ cat >> File2.txt**		                            
Tag detached head play ^C		                     


**(master)$ git commit -am "Bug fix"**	       	                                 
[v1.0.1_FIX 1cdd232] Bug fix		                          
 1 file changed, 1 insertion(+)		                                  


**(master)$ git tag -a 1.0.2 -m "Version 1.0.2"**	                                          


**(master)$ git tag**		                     


**(master)$ git checkout master**	                                
Switched to branch 'master'		                     


**(master)$ cat >> File3.txt**                                               
New changes 		              
new Build Improvement ^C		              


**(master)$ git commit -am "New improvements to 1.1.0"**       	                                         
[master d3c1802] New improvements to 1.1.0		              
 1 file changed, 2 insertions(+)		              


**(master)$ git tag -a 1.1.1 -m "Version 1.1.1"**		       		       



**(master)$ git remote add origin git@github.com:prat14k/GitExercise2.git**		       		


**(master)$ git push --follow-tags origin master**				       
Counting objects: 18, done.		       
Delta compression using up to 8 threads.		       
Compressing objects: 100% (16/16), done.		       
Writing objects: 100% (18/18), 1.75 KiB | 897.00 KiB/s, done.		
Total 18 (delta 2), reused 0 (delta 0)		
remote: Resolving deltas: 100% (2/2), done.		
To github.com:prat14k/GitExercise2.git		
 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;\* [new branch]      master -> master		
 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;\* [new tag]         1.0.0 -> 1.0.0		
 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;\* [new tag]         1.0.1 -> 1.0.1		       
 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;\* [new tag]         1.1.0 -> 1.1.0		       
 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;\* [new tag]         1.1.1 -> 1.1.1		       


**(master)$ git push --follow-tags origin v1.0.1_FIX**		                 		       
Counting objects: 4, done.		       
Delta compression using up to 8 threads.		       
Compressing objects: 100% (4/4), done.		       
Writing objects: 100% (4/4), 461 bytes | 461.00 KiB/s, done.		       
Total 4 (delta 1), reused 0 (delta 0)		       
remote: Resolving deltas: 100% (1/1), completed with 1 local object.		       
To github.com:prat14k/GitExercise2.git		       
 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;\* [new branch]      v1.0.1_FIX -> v1.0.1_FIX             		
 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;\* [new tag]         1.0.2 -> 1.0.2	       
