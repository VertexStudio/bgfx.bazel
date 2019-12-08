# bgfx.bazel - bgfx building in bazel
# Author: Alex Rozgo <alex.rozgo@gmail.com>

load("@bazel_tools//tools/build_defs/repo:git.bzl", "new_git_repository")

new_git_repository(
    name = "bx",
    build_file = "@//:bx.BUILD",
    remote = "git://github.com/bkaradzic/bx.git",
    commit = "4ecfa360574ae7d7b0c58af7426ac59491b028d9",
    shallow_since = "1575526247 -0800",
)

new_git_repository(
    name = "bimg",
    build_file = "@//:bimg.BUILD",
    remote = "git://github.com/bkaradzic/bimg.git",
    commit = "ed5fec9e82f975b2b37641e238f6f78d51c5b82c",
    shallow_since = "1574906069 -0800",
)

new_git_repository(
    name = "bgfx",
    build_file = "@//:bgfx.BUILD",
    remote = "git://github.com/bkaradzic/bgfx.git",
    commit = "aa1aed4ce19094ad3c5925d27eb8ee46ee05ff5f",
    shallow_since = "1575733189 -0800"
)

local_repository (
    name="astc_codec",
    path="../bgfx/bimg/3rdparty/astc-codec",
)
