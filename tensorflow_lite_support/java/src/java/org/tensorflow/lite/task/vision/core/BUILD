load("@build_bazel_rules_android//android:rules.bzl", "android_library")
load("@org_tensorflow//tensorflow/java:build_defs.bzl", "JAVACOPTS")

package(
    default_visibility = ["//tensorflow_lite_support:users"],
    licenses = ["notice"],  # Apache 2.0
)

exports_files([
    "AndroidManifest.xml",
])

filegroup(
    name = "base_vision_api_src",
    srcs = glob(["**/*.java"]),
)

android_library(
    name = "base_vision_api",
    srcs = glob(["*.java"]),
    javacopts = JAVACOPTS,
    manifest = "AndroidManifest.xml",
    deps = [
        "//tensorflow_lite_support/java:tensorflowlite_support_java",
        "//tensorflow_lite_support/java/src/java/org/tensorflow/lite/task/core:base_task_api",
        "//tensorflow_lite_support/java/src/native/task/vision/core:base_vision_api_native",
        "@com_google_auto_value",
        "@org_checkerframework_qual",
        "@org_tensorflow//tensorflow/lite/java:tensorflowlite_java",
    ],
)
