Tracking Remote Repositories.
---------------------------------------------------------------------------

+ Commands.

  - git remote -v

    It shows the remote servers that are being tracked for the current repository,
    and their latest statistics.

  - git fetch

    It fetches new commit information down from their remote server for the
    current repository, it does not commit anything to local database.

  - man git-fetch

    Local documentation on using the 'git fetch' command.

  - man git-remote

    Local documentation on using the 'git remote' command.

  Let's clone a remote repository.

  $ git clone git@github:content-source-control-git.git

  We are using git protocol for the cloning through a ssh tunnel connection
  . the git protocol will allows to handle the pushes an pulls while ssh handles
  the authentication for us.

  $ ls

  content-source-control-git

  Now, we run the following command to check statistics and how the repo has been set to.

  Checking the repository verbosely.

  $ git remote -v

  It also check aliases and the urls which it refers to.

  To check if anything is new in our repository.

  $ git remote show origin

  * remote origin

  Fetch URL: git@github.com:linuxacademy/content-source-control-git.git

  Push  URL: git@github.com:linuxacademy/content-source-control-git.git

  HEAD branch: master

  Remote branches:

  master         tracked

  readme-updates tracked

  test           tracked

  test2          tracked

  Local branch configured for 'git pull':

  master merges with remote master

  Local ref configured for 'git push':

  master pushes to master (up to date)

  The following command allows us to check if everything is up to date and attempt to pull something we might not have.
