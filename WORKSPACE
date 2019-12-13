# bgfx.bazel - bgfx building in bazel
# Author: Alex Rozgo <alex.rozgo@gmail.com>

load("@bazel_tools//tools/build_defs/repo:git.bzl", "git_repository")
load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

git_repository(
    name = "gtest",
    commit = "ba96d0b1161f540656efdaed035b3c062b60e006",
    remote = "https://github.com/google/googletest.git",
)

http_archive(
    name = "honggfuzz",
    build_file = "//third_party:honggfuzz.BUILD",
    sha256 = "9d420326979fed4a065fa6176d5e09bd513cd2820fe216ae8b684aa6780d72b2",
    strip_prefix = "honggfuzz-1.7",
    url = "https://github.com/google/honggfuzz/archive/1.7.zip",
)

http_archive(
    name = "benchmark",
    sha256 = "61ae07eb5d4a0b02753419eb17a82b7d322786bb36ab62bd3df331a4d47c00a7",
    strip_prefix = "benchmark-1.4.1",
    url = "https://github.com/google/benchmark/archive/v1.4.1.zip",
)
