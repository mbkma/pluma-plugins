plugindir = $(PLUMA_PLUGINS_LIBS_DIR)

if ENABLE_PYTHON
plugin_PYTHON = plugins/gpdefs.py
endif

plugin_LTLIBRARIES =
plugin_in_files =
dist_plugin_in_files =
appstreamdir = $(datadir)/metainfo
appstream_in_files =
dist_appstream_in_files =
gsettings_SCHEMAS =

include plugins/codecomment/Makefile.am
include plugins/synctex/Makefile.am
include plugins/terminal/Makefile.am

@GSETTINGS_RULES@

%.plugin: %.plugin.desktop.in $(wildcard $(top_srcdir)/po/*po)
	$(AM_V_GEN) $(MSGFMT) --desktop --keyword=Name --keyword=Description --template $< -d $(top_srcdir)/po -o $@

GENERATED_PLUGIN_FILES = $(plugin_in_files:.plugin.desktop.in=.plugin)

plugin_DATA = $(GENERATED_PLUGIN_FILES)

$(appstream_DATA): $(appstream_in_files) $(wildcard $(top_srcdir)/po/*po)
	$(AM_V_GEN) $(MSGFMT) --xml --template $< -d $(top_srcdir)/po -o $@

GENERATED_APPSTREAM_FILES = $(appstream_in_files:.xml.in=.xml)

appstream_DATA = $(GENERATED_APPSTREAM_FILES)

DISTCLEANFILES +=			\
	plugins/gpdefs.py		\
	$(GENERATED_PLUGIN_FILES)	\
	$(GENERATED_APPDATA_FILES)

CLEANFILES +=				\
	$(GENERATED_PLUGIN_FILES)	\
	$(GENERATED_APPSTREAM_FILES)

EXTRA_DIST +=								\
	plugins/gpdefs.py.in						\
	$(plugin_in_files)						\
	$(dist_plugin_in_files)						\
	$(appstream_in_files)						\
	$(dist_appstream_in_files)					\
	$(gsettings_SCHEMAS)
