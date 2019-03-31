Adding Files.
-------------

+ Commands that we will be using.
  - git add

    This command is used to add files to a git project and it
    adds them to the index file so they can be tracked in the
    staging area.

  - git status

    It can be used to see what files are in the staging area
    (notcommitted yet)

  - git rm

    It removes files from a preject.

+ Command Line Interaction.

  $ ls
  README.rst

  $ git add README.rst

  $ cat .git/index
  DIRC\{��Q�\{k)@���$     �����
                             8F=���όl������ic�
  README.rst\{E9�E�\

  Note: There is a cleaner view of the previous output.

  $ git status
  On branch master

  No commits yet

  Changes to be committed:
    (use "git rm --cached <file>..." to unstage)

          new file:   README.rst


  Note: git does not care about empty directories, if there is an empty directory in our
  repo and we want to git add it then git add will ignore it. in other words, it won't be
  add it.

  $ git rm README.rst

  To force the removal.

  $ git rm -f README.rst
