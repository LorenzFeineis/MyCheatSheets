# Git usage commands

* `HEAD` usually refers to the latest commit
* Commits are specified by the six digit hexadecimal `hash`
* `git help <command>` : prints help information about `command`
* `watch  "git status"` : shows real time status
* `watch "git log --oneline"`: show real time commit hashes and commit messages
  * `git log --oneline -n 3`: show hash and message of the last three commits

### Remote

* `git remote -v`: shows a list of existing remotes
* `git remote add <name> <url>`
  *  `git remote add origin git@github/UserName/project.git`
  *  `git push -u origin master`
* `git remote set-url <name> <newurl> <orldurl>` :Changes URLs for the remote
  *  `git remote set-url origin git@github/UserName/project.git` : Changes the URL for the remote with name `origin`

### Files and differences in commits

* `git show <commit:file>`: show the version of `file` in `commit`.
* `git diff [<file>]` show the difference between the working tree and `HEAD`; if `file` is given it only shows the difference regarding this file
* `git diff <commit> <commit> [<file>]` : show the difference between two commits

### Undo changes, unstage files, ...
* **Note**: Changed always have to be committed. There is no way to change `HEAD` otherwise.
* `git checkout .`: Sets all files back to `HEAD`
* `git checkout <commit> -- <file>` : Sets file to its version in `commit`
* `git restore <file>` : Discard changes in `file` in the current working tree and sets `file` back to the version of the latest commit
* `git restore --staged <file>` : unstage changes in file staged with `git add`
* `git revert -n 3 HEAD~3..HEAD` Set the repository back to the version three commits ago. The last three commits are not lost in this process.
