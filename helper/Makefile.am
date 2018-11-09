include $(top_srcdir)/platform/@with_platform@/Makefile.inc

pkgconfigdir = $(libdir)/pkgconfig
pkgconfig_DATA = $(top_builddir)/pkgconfig/libodphelper-linux.pc

LIB   = $(top_builddir)/lib
AM_CFLAGS  = -I$(srcdir)/include
AM_CFLAGS += -I$(top_srcdir)/platform/@with_platform@/include
AM_CFLAGS += -I$(top_srcdir)/include

AM_LDFLAGS += -version-number '$(ODP_LIBSO_VERSION)'

if HAVE_THUNDERX
AM_CFLAGS +=  -DHAVE_THUNDERX
endif

helperincludedir = $(includedir)/odp/helper/
helperinclude_HEADERS = \
		  $(srcdir)/include/odp/helper/linux.h \
		  $(srcdir)/include/odp/helper/chksum.h\
		  $(srcdir)/include/odp/helper/eth.h\
		  $(srcdir)/include/odp/helper/icmp.h\
		  $(srcdir)/include/odp/helper/ip.h\
		  $(srcdir)/include/odp/helper/ipsec.h\
		  $(srcdir)/include/odp/helper/odph_api.h \
		  $(srcdir)/include/odp/helper/odph_hashtable.h \
		  $(srcdir)/include/odp/helper/odph_lineartable.h \
		  $(srcdir)/include/odp/helper/odph_cuckootable.h \
		  $(srcdir)/include/odp/helper/odph_iplookuptable.h \
		  $(srcdir)/include/odp/helper/odph_iplookuptablev6.h \
		  $(srcdir)/include/odp/helper/strong_types.h\
		  $(srcdir)/include/odp/helper/tcp.h\
		  $(srcdir)/include/odp/helper/table.h\
		  $(srcdir)/include/odp/helper/udp.h

noinst_HEADERS = \
		 $(srcdir)/include/odph_debug.h \
		 $(srcdir)/include/odph_list_internal.h

__LIB__libodphelper_linux_la_SOURCES = \
					eth.c \
					ip.c \
					chksum.c \
					linux.c \
					hashtable.c \
					cuckootable.c \
					iplookuptable.c \
					iplookuptablev6.c \
					lineartable.c

lib_LTLIBRARIES = $(LIB)/libodphelper-linux.la
