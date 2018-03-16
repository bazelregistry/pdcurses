cc_library(
	name = "PDCurses-wincon",
	hdrs = glob(["*.h"]),
	srcs = glob(["*.c", "*.h"]),
	linkopts = ["-DEFAULTLIB:user32.lib", "-DEFAULTLIB:advapi32.lib"],
	deps = [
		"//:PDCurses-hdrs"
	],
	visibility = ["//:__pkg__"]
)
