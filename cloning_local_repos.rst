Cloning Local Repositories.
----------------------------

+ Commands.

  - git clone [local repo] [new repo]

    It clones a local repository to a new repository on the local file system.

  - man git-clone

    Local docs on using the 'git clone' command.

+ Command Interaction.

  There are times when we need to clone a local repository to revert a commit.

    $ ls

    new_project

    $ git clone new_project copy_new_project

    cloning into 'copy_new_project

    done.

    * The previous example can be seen as keeping us away of tearing down our local repository.

    * Cloning can be useful for testing a new feature on our project.
