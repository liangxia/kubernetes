load("@io_bazel_rules_go//go:def.bzl", "go_test")

go_test(
    name = "go_default_test",
    srcs = [
        "certreload_test.go",
        "main_test.go",
    ],
    tags = ["integration"],
    deps = [
        "//cmd/kube-apiserver/app/options:go_default_library",
        "//staging/src/k8s.io/apiserver/pkg/server/dynamiccertificates:go_default_library",
        "//test/integration/framework:go_default_library",
    ],
)

filegroup(
    name = "package-srcs",
    srcs = glob(["**"]),
    tags = ["automanaged"],
    visibility = ["//visibility:private"],
)

filegroup(
    name = "all-srcs",
    srcs = [":package-srcs"],
    tags = ["automanaged"],
    visibility = ["//visibility:public"],
)
