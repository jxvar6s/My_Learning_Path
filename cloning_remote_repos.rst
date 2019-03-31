Cloning Remote Repositories.
-----------------------------

We are going to learne how to clone a remote repository. Follow the command.

+ Commands.

  - git clone [remote URL]

    It clones a remote git repository to the local file system.

  - man git-clone

    Local documentation on using the 'git clone' command.

+ Command Interaction.

  $ git clone https://github.com/CloudAssessments/fs-photos.git

  Cloning into 'fs-photos'...

  remote: Enumerating objects: 114, done.

  remote: Total 114 (delta 0), reused 0 (delta 0), pack-reused 114

  Receiving objects: 100% (114/114), 82.96 KiB | 493.00 KiB/s, done.

  Resolving deltas: 100% (53/53), done.

  $ ls

  fs-photos  My_Learning_Path

  git $ cd fs-photos/

  $fs-photos[master] $ ls

  docker-compose.yml  Dockerfile  package.json  package-lock.json  README.md  src  test

  - At this point, we can enter the following command to display the working tree of the repository.

    $ git log --graph

        [ graph displayed ]

    fs-photos[master] $ git status

    On branch master

    Your branch is up to date with 'origin/master'.


    nothing to commit, working tree clean

+ Conclusion.

  This is how we can clone a remote repository.

