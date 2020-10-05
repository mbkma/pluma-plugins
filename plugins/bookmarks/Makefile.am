plugin_LTLIBRARIES += plugins/bookmarks/libbookmarks.la

plugins_bookmarks_libbookmarks_la_CPPFLAGS =			\
	-I$(top_srcdir)						\
	-I$(top_srcdir)/plugins/bookmarks

plugins_bookmarks_libbookmarks_la_CFLAGS =			\
	$(PLUMA_CFLAGS) 					\
	$(WARN_CFLAGS)						\
	$(DISABLE_DEPRECATED_CFLAGS)

plugins_bookmarks_libbookmarks_la_LDFLAGS = $(PLUGIN_LIBTOOL_FLAGS)
plugins_bookmarks_libbookmarks_la_LIBADD = $(PLUMA_LIBS)

plugins_bookmarks_libbookmarks_la_SOURCES =					\
	plugins/bookmarks/pluma-bookmarks-plugin.h				\
	plugins/bookmarks/pluma-bookmarks-plugin.c

plugin_in_files += plugins/bookmarks/bookmarks.plugin.desktop.in

appstream_in_files += plugins/bookmarks/pluma-bookmarks.metainfo.xml.in
