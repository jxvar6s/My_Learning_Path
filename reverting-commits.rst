Reverting a Commit.
-------------------

+ Commands.

  - git revert [commit]

    It reverts a commit in the project.

  - man git-revert

    Local docs on using the revert command.

+ Commands Interaction.

  - Let's modify a file in our project.

    $ echo "Append this text to the file" >> README.rst

    $ git commit -a -m "Updating README.rst"

    [master 7f3aafb] Updating readme.rst...

    1 file changed, 1 insertion(+)

    Perhaps we do not need keep the previous commit but we need to keep the historical
    record of our project.

  - Now, let's revert the previous commit.

    $ git revert HEAD

      This command opens up HEAD file.

      Modify the commit message   --> save and quit

              Press ESC --> :wq

      [master 6a9b7bb] Revert "Updating readme.rst...modified commit"

      1 file changed, 1 deletion(-)

  - Let's check our log

    $ git log

    commit 6a9b7bbb08c8c9cec9c51d5e06389ae4adacf558 (HEAD -> master)

    Author: Julian <jjulianvargas@gmail.com>

    Date:   Tue Mar 12 22:42:06 2019 -0700

    Revert "Updating readme.rst...modified commit"      <-- commit reverted

    This reverts commit 7f3aafb8309839eb4fb2dfd5f6f883670265b776.

+ Conclusion.

  As we can read, This is one of the way that we can use git revert to undo commits.
