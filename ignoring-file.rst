Certain File Types Will Be Ignored.
-----------------------------------

+ Commands used.

  - .git/info/exclude

    Original file that contains file patterns that git will not
    track.

  - .gitignore

    Ignore file local to a git repository commonly used to
    exclude files base on patterns.

  - git check-ignore <pattern>

    It is used to debug git ignore to see what is and is not
    being excluded from git.

  - man gitignore

    Local docs for the gitignore file.

  - There are file that we do not want to keep track so some pro
    jects create .gitignore file.

    Let's build the .gitignore file in our repository.

    $ mkdir build

    $ touch .gitignore

    $ git add .gitignore

    $ git status
    On branch master
    Changes to be committed:
      (use "git reset HEAD <file>..." to unstage)

            new file:   .gitignore

    Untracked files:
      (use "git add <file>..." to include in what will be committed)

            commiting.rst

  - Commit the changes.

    $ git commit -m "Adding a gitignore file..."

    Note: Everything we list in this file will be ignored by git

  - Let's tell .gitignore what to ignore.

    $ echo "build/*" >> .gitignore

    $ touch build/hello.txt

    $ ls build/
    hello.txt

  - We can set up a backup file through vim

    $ vim committing.rst
      [ lines of code ]

    :set backup

    We will notice a ~ at the end of the file name.

    $ ls
    committing.rst~

  - Let's tell .gitignore to ignore this kind of files

    $ echo *~ >> .gitignore

  - Do not forget to add and to commit the changes.

    $ git commit -a -m "Updating and ignoring vim backups"
