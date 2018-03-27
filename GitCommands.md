# Git & GitHub

## Git

```bash
#Git client configuration
git config  --global user.name "<Your Full Name>"
            --global user.email "<your-email-address>"
            --list   #list all settings

git clone <Project-URL> <optinal-new-name>
```

```bash
git status
git diff    #Show difference between the working tree and the index

git log
    --oneline
    --stat  #show the how many files were changed and the number of lines that were added/removed
    -p || --patch
    -w           # ignore white-space
    <sha>      # show log starting from this commit
    --autor=<name-part>
    --grep=<regex>
    --oneline --decorate --graph --all

git shortlog    #git log output grouped by author and title
            -s || --summary
            -n || --numbered

git show        # show last commit, show same info as git log -p
        <sha>
        --stat
        -w
```

```bash
git add <file1> <file2> … <fileN>
git add .   #add all files to staging area

git rm --cached <file-name> #unstage a file

git commit
git commit -m 'commit message'  || commit --message="message"

#Tell the command to automatically stage files that have been modified and deleted, but new files you have not told Git about are not affected.
git commit (-a -m || -am) 'commit message' #or: --all --message="message"
git commit --amend  #Replace the tip of the current branch by creating a new commit.

git tag
         (-a || --annotate) <tag>
         -a <tag> <sha>
         (-d || --delete) <tag>


git branch
           <new-branch-name>
           <new-branch-name> <sha>
           (-d || --delete) <branch-name>
           (-D || -df ||--delete --force) <branch-name>

git checkout <banch-name>
             -b <branch-name> <from> #create new branch

git merge <name-of-branch-to-merge-in>

git revert <sha>    #Revert some existing commits

git reset (--soft || --hard)<reference-to-commit>
```

## GitHub

```bash
git remote
             -v || --verbose  #show remote url after name
             add <remote-name> <remote-address>
             rename <old-name> <new-name>

git push --all  #Push all branches
         -u <remote-name> <local-branch-name> #use: -u or --set-upstream
         -f <remote-name> <local-branch-name>   #f: force

git pull <remote-name> <branch-to-pull>     #pull = fetch + merge

git fetch <remote-name> <branch-to-pull>

git rebase -i HEAD~3    #i: interactive
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbMjAyMzkxNzY1MV19
-->