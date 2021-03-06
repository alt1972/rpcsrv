dnl Process this file with autoconf 2.52+ to produce a configure script.
dnl
dnl Copyright (C) 2001 Philipp Rumpf
dnl Copyright (C) 2004 Henrique de Moraes Holschuh <hmh@debian.org>
dnl
dnl This program is free software; you can redistribute it and/or modify
dnl it under the terms of the GNU General Public License as published by
dnl the Free Software Foundation; either version 2 of the License, or
dnl (at your option) any later version.
dnl
dnl This program is distributed in the hope that it will be useful,
dnl but WITHOUT ANY WARRANTY; without even the implied warranty of
dnl MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
dnl GNU General Public License for more details.
dnl
dnl You should have received a copy of the GNU General Public License
dnl along with this program; if not, write to the Free Software
dnl Foundation, Inc., 59 Temple Place, Suite 330, Boston, MA  02111-1307  USA

AC_INIT(rpcsrv, 0.1git, [Jeff Garzik <jgarzik@pobox.com>])
AC_PREREQ(2.52)
AC_CONFIG_SRCDIR([main.cc])
AM_INIT_AUTOMAKE([gnu])
AH_TOP([#ifndef __RPCSRV_CONFIG_H__
#define __RPCSRV_CONFIG_H__])
AH_BOTTOM([#endif /* __RPCSRV_CONFIG_H__ */])
AC_CONFIG_HEADERS([rpcsrv-config.h])

dnl Make sure anyone changing configure.ac/Makefile.am has a clue
AM_MAINTAINER_MODE

dnl Checks for programs
AC_PROG_CC
AC_PROG_CXX
AC_PROG_RANLIB

dnl Checks for header files.
AC_HEADER_STDC
dnl AC_CHECK_HEADERS(sys/ioctl.h unistd.h)

dnl Checks for typedefs, structures, and compiler characteristics.
AC_TYPE_SIZE_T
AC_TYPE_PID_T

dnl -----------------------------
dnl Checks for required libraries
dnl -----------------------------

AX_PTHREAD
AX_CHECK_OPENSSL
AX_BOOST_BASE(1.37.0)
AX_BOOST_SYSTEM
AX_BOOST_THREAD
AX_BOOST_DATE_TIME
AX_BOOST_PROGRAM_OPTIONS

dnl AC_CHECK_LIB(gssrpc, gssrpc_svc_register, GSSRPC_LIBS=-lgssrpc, exit 1)

dnl AC_CHECK_LIB(argp, argp_parse, ARGP_LIBS=-largp)

dnl -------------------------------------
dnl Checks for optional library functions
dnl -------------------------------------
dnl AC_CHECK_FUNCS(fdatasync lseek64 srand48_r xdr_u_quad_t)

dnl -----------------
dnl Configure options
dnl -----------------

dnl --------------------------
dnl autoconf output generation
dnl --------------------------

dnl AC_SUBST(GSSRPC_LIBS)
dnl AC_SUBST(DB4_LIBS)
dnl AC_SUBST(EVENT_LIBS)
dnl AC_SUBST(ARGP_LIBS)

AC_CONFIG_FILES([json/Makefile Makefile])
AC_OUTPUT
