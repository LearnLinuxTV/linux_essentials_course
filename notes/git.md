# git

#### List current settings:

`git config --list`

#### Set user info:

1.  `git config --global user.name "Your Name"`

2.  `git config --global user.email somebody@somewhere.net`

3.  `git config --global core.editor vim`\
    Note: Run the above commands without the `--global` option to set the parameters for a single project.

#### Create a repository:

`git init`

#### Create a bare repository:

`git init --bare`

#### To remove a file from version control and working directory:

`git rm`

#### To remove a file from version control but not remove it from your working directory:

`git rm --cached myfile.txt`

#### To restore a deleted file:

`git rev-list -n 1 HEAD -- <file_path>`\
`git checkout <deleting_commit>^ -- <file_path>`

#### To move or rename a file:

`git mv myfile myrenamedfile`

#### Stage a file for commit:

`git add <filename>`

#### To commit all files that are set to be staged, run:

`git commit`

#### To commit all files that are set to be staged, and git an overview of what was changed:

`git commit -v`

#### To commit everything:

`git commit -a`

#### To commit and write the comment inline:

`git commit -m "This is a message."`

#### Show information regarding a commit:

`git show <checksum> (or tag id)`

#### To get more info than the git status command provides, use (doesn't show staged changes):

`git diff`
