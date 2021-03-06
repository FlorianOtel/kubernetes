package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_library(
    name = "go_default_library",
    srcs = [
        "admission.go",
        "config.go",
        "doc.go",
    ],
    tags = ["automanaged"],
    deps = [
        "//pkg/admission:go_default_library",
        "//pkg/api:go_default_library",
        "//plugin/pkg/webhook:go_default_library",
        "//vendor:github.com/golang/glog",
        "//vendor:k8s.io/apimachinery/pkg/runtime/schema",
        "//vendor:k8s.io/apimachinery/pkg/util/yaml",
        "//vendor:k8s.io/apiserver/pkg/util/cache",
        "//vendor:k8s.io/client-go/pkg/api/errors",
        "//vendor:k8s.io/client-go/pkg/apis/imagepolicy/install",
        "//vendor:k8s.io/client-go/pkg/apis/imagepolicy/v1alpha1",
        "//vendor:k8s.io/client-go/pkg/runtime/schema",
        "//vendor:k8s.io/client-go/rest",
    ],
)

go_test(
    name = "go_default_test",
    srcs = [
        "admission_test.go",
        "certs_test.go",
        "config_test.go",
    ],
    library = ":go_default_library",
    tags = ["automanaged"],
    deps = [
        "//pkg/admission:go_default_library",
        "//pkg/api:go_default_library",
        "//pkg/apis/imagepolicy/install:go_default_library",
        "//pkg/apis/imagepolicy/v1alpha1:go_default_library",
        "//pkg/client/unversioned/clientcmd/api/v1:go_default_library",
        "//vendor:k8s.io/apiserver/pkg/authentication/user",
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
)
