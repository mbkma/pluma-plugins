if ENABLE_TERMINAL
plugins_terminaldir = $(plugindir)
plugins_terminal_PYTHON = plugins/terminal/terminal.py

plugin_in_files += plugins/terminal/terminal.plugin.desktop.in
appstream_in_files += plugins/terminal/pluma-terminal.metainfo.xml.in
gsettings_SCHEMAS += plugins/terminal/org.mate.pluma.plugins.terminal.gschema.xml
else
dist_plugin_in_files += plugins/terminal/terminal.plugin.desktop.in
dist_appstream_in_files += plugins/terminal/pluma-terminal.metainfo.xml.in
endif
