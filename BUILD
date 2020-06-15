load("@npm_bazel_typescript//:index.bzl", "ts_library")
load("@build_bazel_rules_nodejs//:index.bzl", "nodejs_binary")

nodejs_binary(
    name = "tsc_wrapped_with_buildozer",
    data = [
        "@npm//@bazel/typescript",
        "@npm//builtins",
    ],
    entry_point = "@npm//:node_modules/@bazel/typescript/internal/tsc_wrapped/tsc_wrapped.js",
    visibility = ["//:__subpackages__"],
)

ts_library(
    name = "semver",
    srcs = ["semver.ts"],
    deps = [
        "@npm//@types/node",
        "@npm//semver"
    ],
    visibility = ["//visibility:public"],
)
