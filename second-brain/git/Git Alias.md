Collection of git alias - Jihyo personal!

## [alias] in '~/.gitconfig'
```cmd
graph = log --graph --branches --tags --remotes --oneline --decorate --pretty=format:'%C(auto)%h%C(auto)%d %Creset%s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit --date=relative

gone = "!f() { git fetch --all --prune; git branch -vv | awk '/: gone]/{print $1}' | xargs git branch -D; }; f"

undo = reset HEAD~1 --mixed
```

### graph
: Alias for showing the graph of branches on console

### gone
: Alias for removing local branches that are gone on remote
- `git fetch --all --prune` just fetches remotes info
- `git branch -vv` list branches and pipes output lines to awk
- `awk '/: gone]/{print $1}'` find lines with `gone`, select first column (which is branch name) and pipe to xargs
- `xargs git branch -D` takes received branches names and deletes them

### undo
: Alias for reseting the previous commit on this branch, and check out all the previous committed changes as uncommitted