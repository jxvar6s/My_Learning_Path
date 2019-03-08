Using Tags.
-----------

Commands.

- git tag -a [tag-name] -m "message"

  It creates an annotated tag.

- git tag

  It views all tags for the repository.

- git tag [tag-name] -m "message"

  It creates a lightweight tag.

- git tag -d [tag name]

  It deletes a specific tag.

- man git-tag

  Local docs for the git tag command.

What is a tag?

  It is used to mark a specific commit in our project so
  it let us put a sticky note in a particular point in
  in our project.

+ Annotated tag.

  It is the most common used in projects.

  $ git tag -a v0.1 -m "message"

  The following command show the tag we just create.

  $ git tag
  v0.1

  The following commond, it shows detail information about the project.

  $ git show v0.1

      [ detail info about the project ]

+ Lightweight tag.

  In contrast to annotated tag, lightweigth tag is used for private or temporarily tag.

  $ git tag [name of the tag]

+ Deleting tags.

  In case we typed a wrong tag, we can delete it as follows.

  $ git tag -d [name of the tag]


This is the basic of taggin in git.
