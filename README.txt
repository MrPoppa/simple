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