# bgfx.bazel - bgfx building in bazel
# Author: Alex Rozgo <alex.rozgo@gmail.com>

load("@rules_cc//cc:defs.bzl", "cc_binary")

package(default_visibility = ["//visibility:public"])

cc_binary(
    name = "debugdraw",
    srcs = ["tests/debugdraw.cpp"],
    linkopts = [
        "-lX11",
        "-lGL",
        "-lpthread",
        "-ldl",
    ],
    deps = [
        "//bgfx:common",
    ],
)
