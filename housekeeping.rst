Garbage Collection.
--------------------

+ Commands.

  - git gc

    The git garbage collection command cleans out old objects that can not be referenced by the database anymore, and it compressescontents within .git directory to save space.

  - git gc --prune

    By default, it cleans out objects that are older than two weeks.

  - man git-gc

    Local docs on using the 'git gc'command.

+ CLI Interaction.

  Sometimes we need to perform some maintenance in our repository and we can do it by
  using 'git gc'.

  $ git gc --prune

  Enumerating objects: 80, done.

  Counting objects: 100% (80/80), done.

  Delta compression using up to 4 threads

  Compressing objects: 100% (78/78), done.

  Writing objects: 100% (80/80), done.

  Total 80 (delta 40), reused 0 (delta 0)

  - Another command we can use is: 'git gc --auto' this command checks if the repository needs cleaning.

    $ git gc --auto

    It won't return anything if the repository does not need to be clean.

  - We can configure the flag --prune for expiration date as follows.

    $ git config gc.pruneexpire "30 days"

    The previous configuration will run every 30 day.



