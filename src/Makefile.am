AM_CPPFLAGS =
METASOURCES = AUTO

EXTRA_DIST =
EXTRA_DIST +=				\
	libtool-version

noinst_DATA = libtool-version

lib_LTLIBRARIES = libuio.la

include_HEADERS = uio_helper.h

libuio_la_SOURCES = uio_helper.c

libuio_la_LDFLAGS = -version-info `grep -v '^\#' $(srcdir)/libtool-version`

AM_CFLAGS = -DUIO_LIB_NAME=\"libuio\" -DUIO_LIB_CUR=`grep -v '^\#' \
	$(srcdir)/libtool-version | cut -d: -f1` -DUIO_LIB_REV=`grep -v '^\#' $(srcdir)/libtool-version | \
	cut -d: -f2` -DUIO_LIB_AGE=`grep -v '^\#' $(srcdir)/libtool-version | cut \
	-d: -f3`
