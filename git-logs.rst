Using Git's Logs.
-----------------

+ Commands.
  - git log

    It views git repository's history.

  - git log --graph

    It shows a textual graph of a project's commit history.

  - git log --stat

    It shows statistics of the files with each commit.

  - git log --pretty=format:

    It formats the output of a git log command to display specific fields.

  - man git-log

    Local docs on using the 'git log'command.

+ Command Interaction.

  Let us take a look the other features of git log and the chronological history of the repository.

  $ git log

    commit ca8ece359dca836340b25e0b8cb0076b27ccf70e (HEAD -> master, origin/master)
    Author: Julian <jjulianvargas@gmail.com>
    Date:   Wed Mar 13 20:19:07 2019 -0700

        Garbage Collection...

    commit e349753a85f22fcd75621136ca1da5140a04d8fe
    Author: Julian <jjulianvargas@gmail.com>
    Date:   Wed Mar 13 19:33:01 2019 -0700

        Working with 'git diff'...

  - When we are working with multiple branches, it is useful to work with the following command.

    $ git log --graph

      * commit ca8ece359dca836340b25e0b8cb0076b27ccf70e (HEAD -> master, origin/master)
      | Author: Julian <jjulianvargas@gmail.com>
      | Date:   Wed Mar 13 20:19:07 2019 -0700
      |
      |     Garbage Collection...
      |
      * commit e349753a85f22fcd75621136ca1da5140a04d8fe
      | Author: Julian <jjulianvargas@gmail.com>
      | Date:   Wed Mar 13 19:33:01 2019 -0700
      |
      |     Working with 'git diff'...

  - We can show the history by limiting for a period of time.

    $ git log --since="4 days ago"

      * commit ca8ece359dca836340b25e0b8cb0076b27ccf70e (HEAD -> master, origin/master)
      | Author: Julian <jjulianvargas@gmail.com>
      | Date:   Wed Mar 13 20:19:07 2019 -0700
      |
      |     Garbage Collection...
      |
      * commit e349753a85f22fcd75621136ca1da5140a04d8fe
      | Author: Julian <jjulianvargas@gmail.com>
      | Date:   Wed Mar 13 19:33:01 2019 -0700
      |
      |     Working with 'git diff'...

  - We can tell git log to match a specific string.

    $ git log -S build

      commit a55390f8cfb0cdb54ab035c20352ba1b57d6a964
      Author: Julian <jjulianvargas@gmail.com>
      Date:   Sun Mar 3 21:19:10 2019 -0800

          Updating committing and ignoring files...

      commit 2c9b406da22b79cfbe9ad6bcf3f38e080f7a3167
      Author: Julian <jjulianvargas@gmail.com>
      Date:   Sun Mar 3 21:16:47 2019 -0800

      Updating and ignoring vim backups...

  - With the following command, we can display basic statitics of each of the commits.

    commit ca8ece359dca836340b25e0b8cb0076b27ccf70e (HEAD -> master, origin/master)
    Author: Julian <jjulianvargas@gmail.com>
    Date:   Wed Mar 13 20:19:07 2019 -0700

        Garbage Collection...

     housekeeping.rst | 50 ++++++++++++++++++++++++++++++++++++++++++++++++++
     1 file changed, 50 insertions(+)

    commit e349753a85f22fcd75621136ca1da5140a04d8fe
    Author: Julian <jjulianvargas@gmail.com>
    Date:   Wed Mar 13 19:33:01 2019 -0700

        Working with 'git diff'...

     command-diff.rst | 45 +++++++++++++++++++++++++++++++++++++++++++++
     1 file changed, 45 insertions(+)

  - We can display a short summary as follows.

    $ git log --shortstat

          [ summary ]

  - git log gives the option to format the output. check man pages of the command for advance options.

    - %h  --> hash.

    - %an --> author's name.

    - %ar --> time related output.

    - %s  --> subject line.

    $ git log --pretty=format:"%h - %an - %ar - %s"

    ca8ece3 - Julian - 25 hours ago - Garbage Collection...

    e349753 - Julian - 25 hours ago - Working with 'git diff'...

    8296969 - Julian - 2 days ago - git revert samples

    4d9d7ca - Julian - 2 days ago - Working wit 'git revert'...

+ git tool is powerful and there are several option that we can interact with them.
