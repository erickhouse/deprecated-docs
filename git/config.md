
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

## git credentials

https://git-scm.com/docs/gitcredentials.html

Credentials are stored in a key registry within the os. Each os has a different key manager. You have the ability to set credentials on the .gitconfig level but it is best to just let git do its own thing. 

When you first try to push / pull a repository git will ask for your credentials in the cli. It will then register those credentials with the git repository and keep them safe in the key registry. 

You can check credentials locally by

`git config user.name`
`git config user.email`

or check which credentials are being used globally.

`git config --global user.name`
`git config --global user.email`
