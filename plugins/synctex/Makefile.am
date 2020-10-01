if ENABLE_SYNCTEX
plugins_synctexdir = $(plugindir)/synctex
plugins_synctex_PYTHON =			\
	plugins/synctex/synctex/__init__.py	\
	plugins/synctex/synctex/synctex.py	\
	plugins/synctex/synctex/atril_dbus.py

plugin_in_files += plugins/synctex/synctex.plugin.desktop.in
appstream_in_files += plugins/synctex/pluma-synctex.metainfo.xml.in
else
dist_plugin_in_files += plugins/synctex/synctex.plugin.desktop.in
dist_appstream_in_files += plugins/synctex/pluma-synctex.metainfo.xml.in
endif
