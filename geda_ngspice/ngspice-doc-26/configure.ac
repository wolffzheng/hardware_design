#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

# To regenerate run:
#    autoreconf  -Wno-portability

AC_INIT(ngspice-doc,26,[http://ngspice.sourceforge.net/bugrep.html])
AC_PREREQ(2.61)

AC_CONFIG_AUX_DIR(config)

AM_INIT_AUTOMAKE

AC_CHECK_PROG(lyx_found, lyx, [yes])

if test "$lyx_found" != "yes"; then
   AC_MSG_ERROR([this package requires LyX])
fi

AC_CONFIG_FILES([Makefile])
AC_OUTPUT
