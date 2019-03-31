Create Local Repository.
------------------------

+ Create a Local Git Repo.
  - git init /path/to/your/directory

    It initializes a git repo, either by creating a new
    directory or adding the git repository files to an existing
    directory.

  - git init --bare /path/to/your/directory

    It initializes a bare git repo, for larger projects so it
    contains no working area.

+ Empty Repo.
  $ git init anybody-there

  $ ls -al anybody-there
  . .. .git

+ Repository.
  - The first command was the simplest way to create a repo.
    $ ls -a anybody-there/.git
    .   branches  description  hooks  info     refs
    ..  config    HEAD         index  objects

+ Empty Directory Becoming A Repo.
  $ ls -a test/
  . ..
  $ git init test/
  Initialized empty Git repository in /home/user/git/test/.git

  $ ls -a test/
  . .. .git

  $ git init --bare mega-project.git
  Initialized empty Git repository in /home/user/git/mega-project.git

  $ ls -a mega-project.git
  .   branches  description  hooks  info     refs
  ..  config    HEAD         index  objects

