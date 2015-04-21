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