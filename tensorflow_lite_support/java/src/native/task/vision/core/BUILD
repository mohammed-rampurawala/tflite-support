load("@org_tensorflow//tensorflow/lite:build_def.bzl", "tflite_jni_binary")

package(
    default_visibility = ["//tensorflow_lite_support:users"],
    licenses = ["notice"],  # Apache 2.0
)

exports_files(["base_vision_api_jni.cc"])

cc_library(
    name = "base_vision_api_native",
    srcs = [
        ":libbase_vision_jni.so",
    ],
)

tflite_jni_binary(
    name = "libbase_vision_jni.so",
    srcs = [
        "base_vision_api_jni.cc",
    ],
    linkscript = "//tensorflow_lite_support/java:default_version_script.lds",
    deps = [
        "//tensorflow_lite_support/cc/task/vision/core:frame_buffer",
        "//tensorflow_lite_support/cc/utils:jni_utils",
        "//tensorflow_lite_support/java/jni",
        "//tensorflow_lite_support/java/src/native/task/vision:jni_utils",
    ],
)
