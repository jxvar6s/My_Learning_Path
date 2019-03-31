git status Usage.
-----------------

+ Commands.
  - git status

    View the state of your staged and upstaged files in your
    working directory.

  - git status -s

    View the output in shortened format.

  - git status -v

    get more verbose output, including what was changed in a
    file.

  - man git-status

    Local docs for the git status command.

+ CLI Interaction.

  - Create a file

  $ touch LICENSE

  $ git status
  On branch master

  No commits yet

  Changes to be committed:
    (use "git rm --cached <file>..." to unstage)

          new file:   README.rst

  Untracked files:
    (use "git add <file>..." to include in what will be committed)

          LICENSE

  LICENSE file is untracked until we add the file.

  - Another way to show the status is.

  $ git status -s
  A  README.rst
  ?? LICENSE

  ?? show that LICENSE file has not been added.

  - Let's modify the lICENSE file and check its status.

  $ echo "This is my license file..." > LICENSE

  - We can check the status with git status or git status -s

  $ git status -s
  AM  LICENSE           # M --> It has been modified
  A   README.rst

  - Once we add the file, M status will change to A

  $ git add LICENSE

