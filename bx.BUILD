# bgfx.bazel - bgfx building in bazel
# Author: Alex Rozgo <alex.rozgo@gmail.com>

load("@rules_cc//cc:defs.bzl", "cc_library")

package(default_visibility = ["//visibility:public"])

bx_srcs = [
    "src/allocator.cpp",
    "src/bx.cpp",
    "src/commandline.cpp",
    "src/crtnone.cpp",
    "src/debug.cpp",
    "src/dtoa.cpp",
    "src/easing.cpp",
    "src/file.cpp",
    "src/filepath.cpp",
    "src/hash.cpp",
    "src/math.cpp",
    "src/mutex.cpp",
    "src/os.cpp",
    "src/process.cpp",
    "src/semaphore.cpp",
    "src/settings.cpp",
    "src/sort.cpp",
    "src/string.cpp",
    "src/thread.cpp",
    "src/timer.cpp",
    "src/url.cpp",
]

cc_library(
    name = "bx",
    srcs = bx_srcs,
    hdrs = glob([
        "**",
    ]),
    includes = [
        "3rdparty",
        "include",
    ],
    linkstatic = True,
    deps = [
    ],
)
