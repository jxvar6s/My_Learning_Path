Forking.
---------------------------------------------------------------------------

+ Forking a Git Priject.

  Forking a git project is more of a process than a command, in fact; we do
  this proces because we need to copy the repository (commits are preserve)
  or we are making a new project base on the fork repository.

+ Process.

           -------------------Forked project
          |                       Server

  Original|                      /      \

                       git push /         \ git push

                              /             \

                        developer 1    developer 2

                      --------------------------------
                      | contributing to the new      |

                      | project base on the original |
                      --------------------------------

+ Conclusion.

  1- Fork the repository.

  2- Make a modification to the forked repository by adding a new link.

  3- Send a pullrequest to the repository owner(s) by asking him/them to pull
    our changes into his/their repository.
