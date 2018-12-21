
# .gitconfig

Add this to the global .gitconfig to use vscode during git difftool and git mergetool. Make sure the vscode is in your path.

``` bash

[core]
    editor = code --wait
[merge]
    tool = vscode
[mergetool "vscode"]
    cmd = code --wait $MERGED
[diff]
    tool = vscode
[difftool "vscode"]
    cmd = code --wait --diff $LOCAL $REMOTE

```
