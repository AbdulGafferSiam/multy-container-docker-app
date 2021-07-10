# Issues:
## GitHub folder has a white arrow on it and can't open
```
git rm --cached client      # no trailing slash
git commit -m "remove client gitlink"
```
Than you can try and add client/ again, which, since it has no .git subfolder, should include its files content.

## “git add” returning “fatal: outside repository” error
First in the clone folder you can create a Branch (so the master stay untouched)
```
git branch [branch_name]
```
After, just copy the files you want from your old folder to the clone folder.

When you are done, just add / commit your change and Merge your branch into the "master" branch. It will look like to something like this:
```
git add .
git commit -m "Comments"
git checkout master
git merge [new_branch]
```