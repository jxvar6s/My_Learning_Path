Using the diff Command.
-----------------------

+ Commands

  - git diff

    It let us view the differences among two commits, files, blobs, or between the
    working tree and the staging area.

  - man git-diff

    Local docs on using the 'git diff' command.

+ CLI Interaction.

  If we have not changed any file then 'git diff' won't display any differences.

  $ git diff

  Let's make a change.

  $ echo "Hola" >> README.rst

  $ git diff

  git diff
  diff --git a/README.rst b/README.rst

  index 56b895c..092265f 100644

  --- a/README.rst

  +++ b/README.rst

  @@ -5,3 +5,4 @@ This repo is my taking notes through my path learning

  git, as a result; the purpose of these notes are merely practice.

  I know there are one to many ways to learn git and I hope these

  notes can be useful to someone.

  +Hola       <--- This is the difference.

