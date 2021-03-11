load("@build_bazel_rules_apple//apple:ios.bzl", "ios_application")
load("@build_bazel_rules_swift//swift:swift.bzl", "swift_library")
#load("@build_bazel_rules_swift_local_config//:toolchain", "swift_library")

swift_library(
    name = "Sources",
    srcs = glob(["src/**"]),
    deps = [
        "//Lib-Swift:Lib_Swift",
        "@Rx//:RxSwift"
    ]
)

ios_application(
    name = "AppA-iOS",
    bundle_id = "be.tulipemoutarde.appa",
    families = ["iphone"],
    infoplists = [":Info.plist"],
    minimum_os_version = "11.0",
    visibility = ["//visibility:public"],
    deps = [":Sources"],
)
