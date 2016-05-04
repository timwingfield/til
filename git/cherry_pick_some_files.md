### git cherry-pick some files from a commit

When you want to cherry-pick only some files from a commit, do the following. These steps will unstage the entire
commit and allow you to review each modified file via `git add -p`.

1. `git cherry-pick -n <commit>` This will cherry pick using the no commit flag (`-n | --no-commit`) which will let
   you inspect the result before committing.
2. `git reset HEAD` this will unstage all the files in the commit you just cherry picked.
3. [optional] `git rm <path>` Do this if there are files in the commit you don't want added
4. `git add -p <path>` to add the new files, or reject the changes you don't want
5. `git commit`
6. `git checkout .` to throw away any commits left over after you're done

Alternatively, if you want to only remove one or two files...

1. `git cherry-pick -n <commit>` This will cherry pick using the no commit flag (`-n | --no-commit`) which will let
   you inspect the result before committing.
2. `git checkout HEAD <path>` This will recursively remove any file(s) you don't want from the cherry picked commit.
3. `git commit` and it'll use the commit message from the cherry picked commit
