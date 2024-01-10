# git-learning
Self study on git
https://learngitbranching.js.org/

#  git commit   
commit your git

#  git branch bugFix       
create new branch
#  git checkout bugFix; git commit  
commit with branch 

#  git checkout c3     
seperate HEAD from current branch to c3
#  git branch -f main c5  
move main to c5 version. can be any version.   -f for FORCING
#  git checkout HEAD^     
move HEAD one step up
#  git checkout HEAD~5        
move HEAD 5 step up, number can be changed
#  git branch -f bugFix HEAD~5   
move bugFix and HEAD 5 step up

#  git reset HEAD~1         
move the current branch one step backwards as the older commit. like from c2 to c1. Works on local machine(your own PC). 
#  git revert HEAD         
reverse the current branch to backwards but it not like c2 to c1, it actually commit to a c2* that you can share with others. REMEMBER DON'T ADD ~ OR ^ IF JUST WANT ONE STEP BACK.

#  git rebase -i to reorder the commits
#  git cherry-pick c2 c4     
just copy branch c2 c4 to the current branch and created c2* c4*
#  git rebase -i HEAD~3     
same like cherry-pick but have more functions such like you can reorder commit, remove specific commit and check commit. example: HEAD~3 C2 C3 C4 to C4 C2(C3 had been removed) .
#  git commit --amend       
create another current branch. like c2 >>> c2`, c3`` >>> c3```.

#  git rebase caption main  
move main to caption(HEAD position)
#  git tag v2 c2 
tag c2 with a name v2
#  git describe <ref>

Where <ref> is anything git can resolve into a commit. If you don't specify a ref, git just uses where you're checked out right now (HEAD).
The output of the command looks like:

#  <tag>_<numCommits>_g<hash>

Where tag is the closest ancestor tag in history, numCommits is how many commits away that tag is, and <hash> is the hash of the commit being described.
