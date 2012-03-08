ioquake3 documentation project
==============================

ioquake3 developers have stated that they do not want inline documentation
because all of the forked projects will have merging problems.  This uses
documentation outside of the code to avoid that problem.

For instance, code/qcommon/qcommon.h is documented in code/qcommon/dox/qcommon.h.dox.
Doxygen knows that the documentation in that *.dox is for the qcommon.h file due to
the \file command.

As you can see, external documentation is a lot more annoying since you have to
duplicate so much of the code structure.  However, it is possible and maintainable.
Doxygen will produce warnings when the documentation is out of sync with the code.

Commands
--------

tags = ctags -R.  Use this for vi or anything that expects normal ctags format.
TAGS = etags -R.  Use this for Emacs.
Doxyfile = doxygen -g and then edited it.  Use this to build HTML documentation.
  You will need several dependencies and it is setup for Linux paths.

docs/ has all of the new content.

Added a new target 'doc' in the Makefile to build all 3 types of documentation.
