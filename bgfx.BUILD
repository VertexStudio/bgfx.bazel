# bgfx.bazel - bgfx building in bazel
# Author: Alex Rozgo <alex.rozgo@gmail.com>

load("@rules_cc//cc:defs.bzl", "cc_binary", "cc_library")

package(default_visibility = ["//visibility:public"])

exports_files(glob(
    [
        "examples/common/**",
        "examples/29-debugdraw/**",
    ],
))

srcs = [
    "src/bgfx.cpp",
    "src/debug_renderdoc.cpp",
    "src/dxgi.cpp",
    "src/glcontext_egl.cpp",
    "src/glcontext_glx.cpp",
    "src/glcontext_wgl.cpp",
    "src/glcontext_html5.cpp",
    "src/nvapi.cpp",
    "src/renderer_d3d11.cpp",
    "src/renderer_d3d12.cpp",
    "src/renderer_d3d9.cpp",
    "src/renderer_gl.cpp",
    "src/renderer_gnm.cpp",
    "src/renderer_noop.cpp",
    "src/renderer_nvn.cpp",
    "src/renderer_vk.cpp",
    "src/shader_dx9bc.cpp",
    "src/shader_dxbc.cpp",
    "src/shader_spirv.cpp",
    "src/topology.cpp",
    "src/vertexdecl.cpp",
]

cc_library(
    name = "bgfx",
    srcs = srcs + glob([
        "src/**/*.h",
        "src/**/*.inl",
        "3rdparty/dear-imgui/**/*.cpp",
        "3rdparty/meshoptimizer/src/**/*.cpp",
    ]),
    hdrs = glob([
        "**/*.h",
        "**/*.inl",
    ]),
    copts = [
    ],
    includes = [
        "3rdparty",
        "3rdparty/khronos",
        "include",
    ],
    linkstatic = True,
    deps = [
        "@bimg",
    ],
)

cc_library(
    name = "common",
    srcs = glob(["examples/common/**/*.cpp"]),
    hdrs = glob(["examples/common/**/*.h"]),
    defines = [
        "ENTRY_CONFIG_IMPLEMENT_MAIN=1",
    ],
    includes = [
        "examples/common",
    ],
    linkstatic = True,
    deps = [
        ":bgfx",
    ],
)

examples_deps = [
    ":common",
]

examples_linkopts = [
    "-lX11",
    "-lGL",
    "-lpthread",
    "-ldl",
]

cc_binary(
    name = "29-debug_draw",
    srcs = ["examples/29-debugdraw/debugdraw.cpp"],
    linkopts = examples_linkopts,
    deps = examples_deps,
)
