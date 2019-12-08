# bgfx.bazel - bgfx building in bazel
# Author: Alex Rozgo <alex.rozgo@gmail.com>

load("@rules_cc//cc:defs.bzl", "cc_library")

package(default_visibility = ["//visibility:public"])

srcs = [
    "src/**/*.cpp",
    "3rdparty/libsquish/*.cpp",
    "3rdparty/libsquish/*.h",
    "3rdparty/libsquish/*.inl",
    "3rdparty/edtaa3/*.cpp",
    "3rdparty/edtaa3/*.h",
    "3rdparty/etc1/*.cpp",
    "3rdparty/etc1/*.h",
    "3rdparty/etc2/*.cpp",
    "3rdparty/etc2/*.hpp",
    "3rdparty/nvtt/**/*.cpp",
    "3rdparty/nvtt/**/*.h",
    "3rdparty/nvtt/**/*.inl",
    "3rdparty/pvrtc/*.cpp",
    "3rdparty/pvrtc/*.h",
    "3rdparty/astc/*.cpp",
    "3rdparty/astc/*.h",
    "3rdparty/tinyexr/*.h",
    "3rdparty/iqa/include/*.h",
    "3rdparty/iqa/source/*.c",
]

cc_library(
    name = "bimg",
    srcs = glob(srcs),
    hdrs = glob([
        "**/*.h",
        "src/bimg_p.*",
        "3rdparty/lodepng/*.cpp",
    ]),
    includes = [
        "3rdparty",
        "3rdparty/iqa/include",
        "3rdparty/nvtt",
        "include",
    ],
    linkstatic = True,
    deps = [
        "@astc_codec",
        "@bx",
    ],
)
