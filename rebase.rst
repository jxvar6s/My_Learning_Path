Rebasing
---------

+ Commands.

  - git rebase [branch]

      It replays changes made to one branch over the top of another branch.

  - man git-rebase

      Local docs on using the 'git rebase' command.

  - One way to depict rebase, it is more like appending the change from one branch to another.

+ Interaction.

  - First let's change to "developement" branch.

    $ git checkout development

    Let's open and make a change in one of the files.

    $ vim README.rst

        "Make the change --> save and quit."

        :wq

  - Now, let's commited to our developement branch.

    $ git commit -a -m "Updating instructions..."

  - Let's seitch back to master branch.

    $ git checkout master

  - Now instead of merging the development branch, we will rebase the master branch by
    replaying the changes we made in the file over top of the master branch.

    $ git rebase development

+ Conclusion.

  In contrast to git merge, git rebase looks slightly cleaner. If we rebase then we
  rebase only what we have work on.


