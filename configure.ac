# Input file for autoconf to generate the configure script.

# See https://www.gnu.org/software/autoconf/manual/autoconf.html for help on
# the macros used in this file.

AC_INIT([streamly], [0.7.2], [streamly@composewell.com], [streamly])

# To suppress "WARNING: unrecognized options: --with-compiler"
AC_ARG_WITH([compiler], [GHC])

# XXX Do this only for linux
AC_CHECK_DECLS([IN_MASK_CREATE],[],[],[#include <sys/inotify.h>])
AC_CHECK_DECLS([IN_EXCL_UNLINK],[],[],[#include <sys/inotify.h>])

# XXX Do this only for macOS
AC_CHECK_DECLS([kFSEventStreamCreateFlagFileEvents],[],[],[#include <CoreServices/CoreServices.h>])
AC_CHECK_DECLS([kFSEventStreamCreateFlagFullHistory],[],[],[#include <CoreServices/CoreServices.h>])
AC_CHECK_DECLS([kFSEventStreamEventFlagItemCloned],[],[],[#include <CoreServices/CoreServices.h>])
AC_CHECK_DECLS([kFSEventStreamEventFlagItemIsHardlink],[],[],[#include <CoreServices/CoreServices.h>])

# Check headers and functions required
AC_CHECK_HEADERS([time.h])
AC_CHECK_FUNCS([clock_gettime])

# Output
AC_CONFIG_HEADERS([src/config.h])
AC_OUTPUT
