# git-learning
Self study on git
https://learngitbranching.js.org/

#  git commit   
commit your git

#  git branch bugFix       
create new branch
# git checkout -b bugFix c2(optional)
create new branch(c2) and move head on bugFix
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
The output of the command looks like: "tag_numCommits_g hash"
# git merge 


Where tag is the closest ancestor tag in history, numCommits is how many commits away that tag is, and <hash> is the hash of the commit being described.
# git clone
git clone in the real world is the command you'll use to create local copies of remote repositories
copy all the branch 
# git fetch
download the remote respository to origin/main. but it won't update the main only the o/main. 
git fetch performs two main steps, and two main steps only. It:

downloads the commits that the remote has but are missing from our local repository, and...
updates where our remote branches point
# git pull
 git pull is essentially shorthand for a git fetch followed by a merge of whatever branch was just fetched.

# git fakeTeamwork

 commit remote repository. can always do "git faketeamwork main 3", this means commit remote main 3 times. 

 # git push

 git push is responsible for uploading your changes to a specified remote and updating that remote to incorporate your new commits. 
 # git pull --rebase
 # git checkout -b foo o/main
create a new branch foo and use it to track orgin/main instead of using main to track.
 # git branch -u o/main foo
 set foo to track o/main(if there is a branch called foo). if foo already checkout can do with git branch checkout -u o/main
