Committin to Git -- repo --
----------------------------

+ Commands usage.

  - git commit

    It opens text editor to prepare for a commit of files in the
    staging area.

  - git commit -m "Message"

    It bypasses the editor and perforns a commit with the speci
    fied message.

  - git commit -a -m "message"

    commit a modified file in the staging area.

  - man git-commit

    Local docs for the commit command for git.

+ Command's Interaction.

  The following command opens the text editor and display all
  the files that they have to be committed. We have to enter the
  message on the top first line. Note: We can call it the long way.

  $ git commit

        ---> Type the message in this line <---
  Please enter the commit message for your changes. Lines starting
  # with '#' will be ignored, and an empty message aborts the commit.
  #
  # On branch master
  #
  # Initial commit
  #
  # Changes to be committed:
  #       new file:   LICENSE
  #       new file:   README.rst

  save the file and quit. Remember that the commit messages are
  stored in .git/COMMIT_EDITMSG

  $ cat .git/COMMIT_EDITMSG
  Our first file committed.

  # Please enter the commit message for your changes. Lines starting
  # with '#' will be ignored, and an empty message aborts the commit.
  #
  # On branch master
  #
  # Initial commit
  #
  # Changes to be committed:
  #       new file:   LICENSE
  #       new file:   README.rst

  The short way for committing is as follows.

  $ git commit -m "Adding files to the repo..."

  - We can remove  a file from the project but we can keep it
    in the project directory.

    $ git rm --cached name-of-file

    Do not forget to update the git database to reflect the
    change.

    $ git status -s
    D  name-of-file
    ?? name-of-file

  - We update the database by committing.

  $ git commit -m "Delete name-of-file"

    # The outputs reflects the change.


