different line

If you add info in a file and that needs to be added and commited 
but before you do that you regret it you can checkout the previous file by typing
git checkout -- filename.

To commit a file directly without going via add you can use 
commit -am (or -a -m) "message"

If I want to reset after committing I can use
git reset --soft HEAD^
This will bring it back into stage area. I can reset it again by using
git reset HEAD (file-name optional)

To add github 
git remote add origin https://github.com/Andersrapp/simple.git

Check by using git remote -v.

To add credentials so you only have to specify your password and username ONCE:
git config --global credential.helper wincred

After next push and user-password thingy you're good to go.

To remove remotes 
git remote rm name (i.e. origin)

To clone a repo and give it a new name use 
git clone git-url "newName"

Okay, sooo...you create branch
git branch cat
git checkout cat
ls
git checkout master
ls
git checkout cat
echo "text" newfile.txt  (-- creates new file with text and file name)
git add, commit

move to master
git checkout master
git merge cat
git branch -d cat  (removes the branch)


To create and checkout a branch instantly
git checkout -b admin

added info to readme to create conflict....

When we update the same file at the same time on github via push.
The second one will get rejected. 
Using pull is the same as 
git fetch
 - and then  - 
git merge origin/master
And creates a commit!
After that we must make a push to make sure the repo online and our local git is the same.

-----
We edited the same line in the same file in two places. So the first one adds, commits and pushes. Everything's fine!
The second one adds, commits, pushes and is rejected. 
He uses pull to merge the files but it fails!
so he opens the files and solves the conflict between HEAD (local file) and the other.
Then type:
git commit -a    (without adding a message. it goes into editing mode. write :wq and hit enter)
After that the parts are merged and we can push to update repo online. The other then has to make a pull!!

-----

To create a new branch directly and switch to it(checkout) use git branch -b 'branch-name'
To push a branch to github use 
-- git push origin 'branch-name' -- !!!
Sorry! That's wrong. First time you use 
git push --set-upstream origin 'branch-name'

So in order to pull the branch from somewhere else
If I send git pull I get info on new branch. 
Type git branch will NOT show me the new branch yet - 
but git branch -r - will!
git checkout branch-name - will create local copy to work on!

git remote show origin -- will show us all the branches, tracked, remote and local

git branch remote -D branchname -- will delete the branch despite changes not being merged. 
Capital D takes care of that! :)

To create new tags
git tag -a name -m description
to see them write	 git tags
to push them write git push --tags