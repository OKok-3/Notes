## GPG Signing Previous Commits

**Note that the following 2 commands will change the original commit dates**

`git rebase --exec 'git commit --amend --no-edit -n -S' -i [hash of first signed commit]`

### GPG Sign All Past Commits In A Repo

`git rebase --exec 'git commit --amend --no-edit -n -S' -i --root`

### Keep Original Commit Dates Back Signing Previous Commits

**MUST BE RUN AFTER ONE OF THE ABOVE 2 COMMANDS ARE EXECUTED**

`git rebase --committer-date-is-author-date -i --root`

*Author: Peter Babic 
[source](https://peterbabic.dev/blog/git-sign-previous-commits-keeping-dates)*
