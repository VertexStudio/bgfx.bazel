# bgfx.bazel - bgfx building in bazel
# Author: Alex Rozgo <alex.rozgo@gmail.com>

load("@rules_cc//cc:defs.bzl", "cc_binary", "cc_library")

package(default_visibility = ["//visibility:public"])

cc_library(
    name = "bgfx",
    deps = [
        "@bgfx//:common",
    ],
)

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
        "@bgfx//:common",
    ],
)
