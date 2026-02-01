# Process this file with autoconf to produce a configure script.
AC_PREREQ([2.71])
AC_INIT([bk-terak-emu],[2006],[http://sourceforge.net/projects/bk-terak-emu/])
AC_CONFIG_SRCDIR([terakdisk.c])
AC_CONFIG_HEADERS([config.h])

# Checks for programs.
AC_PROG_CC
AC_PROG_INSTALL

case "$GCC" in
yes) CFLAGS="-Wall $CFLAGS" ;;
esac

# Checks for libraries.
AC_SEARCH_LIBS(SDL_Init, SDL)
AC_SEARCH_LIBS([bindtextdomain], [intl])

# Checks for header files.
m4_warn([obsolete],
[The preprocessor macro `STDC_HEADERS' is obsolete.
  Except in unusual embedded environments, you can safely include all
  ISO C90 headers unconditionally.])dnl
# Autoupdate added the next two lines to ensure that your configure
# script's behavior did not change.  They are probably safe to remove.
AC_CHECK_INCLUDES_DEFAULT
AC_PROG_EGREP

AC_CHECK_HEADERS([fcntl.h libintl.h locale.h malloc.h sgtty.h stdlib.h string.h sys/ioctl.h sys/param.h sys/socket.h sys/time.h unistd.h])

# Checks for typedefs, structures, and compiler characteristics.
AC_CHECK_HEADER_STDBOOL
AC_C_INLINE
AC_TYPE_OFF_T
m4_warn([obsolete],
[Update your code to rely only on HAVE_SYS_TIME_H,
then remove this warning and the obsolete code below it.
All current systems provide time.h; it need not be checked for.
Not all systems provide sys/time.h, but those that do, all allow
you to include it and time.h simultaneously.])dnl
AC_CHECK_HEADERS_ONCE([sys/time.h])
# Obsolete code to be removed.
if test $ac_cv_header_sys_time_h = yes; then
  AC_DEFINE([TIME_WITH_SYS_TIME],[1],[Define to 1 if you can safely include both <sys/time.h>
	     and <time.h>.  This macro is obsolete.])
fi
# End of obsolete code.


# Checks for library functions.
AC_FUNC_MALLOC
AC_FUNC_MMAP
AC_FUNC_SELECT_ARGTYPES
AC_CHECK_FUNCS([atexit isascii memset munmap select setlocale strcasecmp strchr strdup strspn])

AC_CONFIG_FILES([Makefile po/Makefile.in])
AC_OUTPUT

GETTEXT_PACKAGE=bk
