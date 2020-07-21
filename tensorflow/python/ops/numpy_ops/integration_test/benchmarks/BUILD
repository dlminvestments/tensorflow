load("//tensorflow:tensorflow.bzl", "cuda_py_test")

package(
    default_visibility = [
        "//tensorflow:internal",
    ],
    licenses = ["notice"],  # Apache 2.0
)

cuda_py_test(
    name = "micro_benchmarks",
    srcs = ["micro_benchmarks.py"],
    python_version = "PY3",
    shard_count = 5,
    deps = [
        ":numpy_mlp",
        ":tf_numpy_mlp",
        "//tensorflow:tensorflow_py",
        "//tensorflow/python:extra_py_tests_deps",
        "//tensorflow/python:framework_test_lib",
        "//tensorflow/python:platform",
        "//tensorflow/python:platform_benchmark",
        "//tensorflow/python/ops/numpy_ops:numpy",
        "//third_party/py/numpy",
        "@absl_py//absl/flags",
        "@absl_py//absl/logging",
    ],
)

py_library(
    name = "numpy_mlp",
    srcs = ["numpy_mlp.py"],
    deps = [
        "//third_party/py/numpy",
    ],
)

py_library(
    name = "tf_numpy_mlp",
    srcs = ["tf_numpy_mlp.py"],
    deps = [
        "//tensorflow:tensorflow_py",
        "//tensorflow/python/ops/numpy_ops:numpy",
    ],
)