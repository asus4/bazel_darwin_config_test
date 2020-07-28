load("@rules_cc//cc:defs.bzl", "cc_binary")


config_setting(
    name = "macos",
    values = {
        "apple_platform_type": "macos",
        "cpu": "darwin",
    },
)

config_setting(
    name = "macos_x86_64",
    values = {
        "apple_platform_type": "macos",
        "cpu": "darwin_x86_64",
    },
)

cc_binary(
    name = "hello-world",
    srcs = select({
        "macos": ["hello-darwin.cc"],
        "macos_x86_64": ["hello-darwin_x86_64.cc"],
    })
)

