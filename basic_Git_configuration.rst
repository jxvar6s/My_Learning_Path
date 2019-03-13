Basic Configuration.
--------------------

+ Using - git config

  - git config

    This command is used to configure various elements of your
    git environment.

  - git config --list

    View your configuration information for your git environment

  - man git-config

    Local docs for what you can configure for your git
    environment.

+ Interaction.

  $ git config --global user.name "your-name"

  $ git config --global user.email "your-name@email.com"

  - Configure your editor.

    - Find the full path of your editor's choice, in my case is vim.

      $ which vim

        /usr/bin/vim

      $ git config --global core.editor "/usr/bin/vim"

  - Displaying configuration list.

    $ git config --list

    core.editor=/usr/bin/vim

    user.name=your-name

    user.email=your-name@email.com

  - Displaying the content of .gitconfig

    $ cat ~/.gitconfig

    [user]
        name = your-name

        email = your-name@email.com
    [core]
        editor = /usr/bin/vim

  - If we need to configure a different email for a specific
    project. cd into that specific directory project.

      $ cd directory-name-of-project

      $ git config user.email "your-name@email.com"

      note: No --global flag is needed.
