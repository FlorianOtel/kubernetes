package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_binary",
    "go_library",
    "go_test",
    "cgo_library",
)

go_library(
    name = "go_default_library",
    srcs = [
        "plugins.go",
        "server.go",
    ],
    tags = ["automanaged"],
    deps = [
        "//cmd/kube-apiserver/app/options:go_default_library",
        "//pkg/admission:go_default_library",
        "//pkg/api:go_default_library",
        "//pkg/api/unversioned:go_default_library",
        "//pkg/apis/autoscaling:go_default_library",
        "//pkg/apis/batch:go_default_library",
        "//pkg/apis/extensions:go_default_library",
        "//pkg/apiserver:go_default_library",
        "//pkg/apiserver/authenticator:go_default_library",
        "//pkg/auth/authorizer/union:go_default_library",
        "//pkg/auth/user:go_default_library",
        "//pkg/capabilities:go_default_library",
        "//pkg/cloudprovider:go_default_library",
        "//pkg/cloudprovider/providers:go_default_library",
        "//pkg/controller/informers:go_default_library",
        "//pkg/controller/serviceaccount:go_default_library",
        "//pkg/generated/openapi:go_default_library",
        "//pkg/genericapiserver:go_default_library",
        "//pkg/genericapiserver/authorizer:go_default_library",
        "//pkg/genericapiserver/validation:go_default_library",
        "//pkg/master:go_default_library",
        "//pkg/registry/cachesize:go_default_library",
        "//pkg/serviceaccount:go_default_library",
        "//pkg/util/net:go_default_library",
        "//pkg/util/wait:go_default_library",
        "//pkg/version:go_default_library",
        "//plugin/pkg/admission/admit:go_default_library",
        "//plugin/pkg/admission/alwayspullimages:go_default_library",
        "//plugin/pkg/admission/antiaffinity:go_default_library",
        "//plugin/pkg/admission/deny:go_default_library",
        "//plugin/pkg/admission/exec:go_default_library",
        "//plugin/pkg/admission/gc:go_default_library",
        "//plugin/pkg/admission/imagepolicy:go_default_library",
        "//plugin/pkg/admission/initialresources:go_default_library",
        "//plugin/pkg/admission/limitranger:go_default_library",
        "//plugin/pkg/admission/namespace/autoprovision:go_default_library",
        "//plugin/pkg/admission/namespace/exists:go_default_library",
        "//plugin/pkg/admission/namespace/lifecycle:go_default_library",
        "//plugin/pkg/admission/persistentvolume/label:go_default_library",
        "//plugin/pkg/admission/podnodeselector:go_default_library",
        "//plugin/pkg/admission/resourcequota:go_default_library",
        "//plugin/pkg/admission/security/podsecuritypolicy:go_default_library",
        "//plugin/pkg/admission/securitycontext/scdeny:go_default_library",
        "//plugin/pkg/admission/serviceaccount:go_default_library",
        "//plugin/pkg/admission/storageclass/default:go_default_library",
        "//plugin/pkg/auth/authenticator/request/union:go_default_library",
        "//vendor:github.com/golang/glog",
        "//vendor:github.com/pborman/uuid",
        "//vendor:github.com/spf13/cobra",
        "//vendor:github.com/spf13/pflag",
    ],
)

go_test(
    name = "go_default_test",
    srcs = ["server_test.go"],
    library = "go_default_library",
    tags = ["automanaged"],
    deps = ["//cmd/kube-apiserver/app/options:go_default_library"],
)