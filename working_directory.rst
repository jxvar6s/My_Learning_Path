Basics of Git File System.
--------------------------

+ /path/to/your/git/project
  - Working directory
  - When we enter git init a .git directory is created
    - .git --> has all files to keep track of the files
      project.

      When a file is created in the directory project, it is
      in a staging area until it is added to the project with
      git add [nameOfFile]

    - $ ls .git/ --> What is it inside of this directory?

      COMMIT_EDITMSG --> Contains all the messages that have
                        been commited.
      HEAD --> Reference to the current branch that we are
              working on.
      config --> It has user's configuration.

      description --> Plain text that containg the name of the
              repo used by git.
      hooks --> Contains scripts that it can be used to automate
              tasks.
      index --> It keeps track of items on staging area and it
              keeps track of files that are ready to be committed
      info --> It tells what file are going to be ignore.

      log --> It contains log files of the repository activity.
            commits and changes.
      objects --> A database of compressed files.

      refs --> It contains reference files in folders for the
            branches that interact with the repositories.
