config_setting(
	name = "x64_windows_msvc",
	values = {
		"cpu": "x64_windows_msvc"
	},
)

config_setting(
	name = "x64_windows",
	values = {
		"cpu": "x64_windows"
	},
)

cc_library(
	name = "PDCurses-hdrs",
	hdrs = [
		"curses.h",
		"curspriv.h",
		"panel.h",
		"term.h",
	],
	visibility = ["//:__subpackages__"],
)

cc_library(
	name = "PDCurses",
	deps = [
		":PDCurses-hdrs",
		"//pdcurses:PDCurses-pdcurses",
	] + select({
		":x64_windows": ["//wincon:PDCurses-wincon"],
		":x64_windows_msvc": ["//wincon:PDCurses-wincon"],
	}),
	visibility = ["//visibility:public"]
)
