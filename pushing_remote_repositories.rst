Pushing to Remote Repositories.
----------------------------------------------------------------------------

+ Commands.

  - git push -u [remote] [local-branch]

    It pushes local changes to the upstrean git repository.

  - man git-push

    Local documentation on using the 'git push' command.

+ Commands Interaction.

  For this demo, we need to change to the 'development' branch or we can create a new branch by.

  * Creating a new branch.

    $ git branch new_branch

  * Change to an existing branch in this demo 'development'.

    $ git checkout development

  - Adding a file to the branch 'developoment'

    $ echo "Do not forget to include SSH key to your github account..." >> README.md

  - commiting

    $ git commit -a -m "Updating README file..."

    [development e99fd41] README.rst has been updated to include ssh key...

    1 file changed, 1 insertion(+)

  - Pushing to the remote repository. e.g. git push -u origin [name-of-branch]

    $ git push -u origin developement

          git will ask us to enter our github username and

          password so it will display the following message at

          the end of the 'git push' process:

           * [new branch]      development -> development

           Branch 'development' set up to track remote branch

           'development' from 'origin'.

  At this point all the changes have been taken care.


