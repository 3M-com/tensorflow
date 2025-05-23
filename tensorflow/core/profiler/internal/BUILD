load("//tensorflow:tensorflow.bzl", "if_not_windows", "tf_cc_test")
load("//tensorflow/core/platform:rules_cc.bzl", "cc_library")

package(
    # copybara:uncomment default_applicable_licenses = ["//tensorflow:license"],
    default_visibility = ["//tensorflow:internal"],
    licenses = ["notice"],
)

cc_library(
    name = "tfprof_stats",
    srcs = ["tfprof_stats.cc"],
    hdrs = ["tfprof_stats.h"],
    deps = [
        ":tfprof_code",
        ":tfprof_graph",
        ":tfprof_node",
        ":tfprof_op",
        ":tfprof_scope",
        ":tfprof_show",
        ":tfprof_timeline",
        ":tfprof_utils",
        "//tensorflow/c:checkpoint_reader",
        "//tensorflow/core:lib",
        "//tensorflow/core:protos_all_cc",
        "//tensorflow/core/platform:regexp",
        "//tensorflow/core/profiler:protos_all_cc",
        "//tensorflow/core/profiler:tfprof_options",
        "@com_google_absl//absl/strings",
        "@com_google_absl//absl/strings:str_format",
    ],
)

cc_library(
    name = "tfprof_timeline",
    srcs = ["tfprof_timeline.cc"],
    hdrs = ["tfprof_timeline.h"],
    deps = [
        ":tfprof_node_show",
        ":tfprof_utils",
        "//tensorflow/core:lib",
        "@com_google_absl//absl/strings",
        "@com_google_absl//absl/strings:str_format",
        "@jsoncpp_git//:jsoncpp",
    ],
)

cc_library(
    name = "tfprof_node",
    srcs = ["tfprof_node.cc"],
    hdrs = ["tfprof_node.h"],
    deps = [
        ":tfprof_utils",
        "//tensorflow/core:protos_all_cc",
        "//tensorflow/core/platform:regexp",
        "//tensorflow/core/profiler:protos_all_cc",
        "//tensorflow/core/profiler:tfprof_options",
        "@com_google_absl//absl/strings:str_format",
    ],
)

cc_library(
    name = "tfprof_scope",
    srcs = ["tfprof_scope.cc"],
    hdrs = ["tfprof_scope.h"],
    deps = [
        ":tfprof_constants",
        ":tfprof_node",
        ":tfprof_show",
        ":tfprof_tensor",
        ":tfprof_utils",
        "//tensorflow/c:checkpoint_reader",
        "//tensorflow/core:lib",
        "//tensorflow/core/platform:regexp",
        "//tensorflow/core/profiler:protos_all_cc",
        "//tensorflow/core/profiler:tfprof_options",
        "@com_google_absl//absl/strings:str_format",
    ],
)

cc_library(
    name = "tfprof_op",
    srcs = ["tfprof_op.cc"],
    hdrs = ["tfprof_op.h"],
    deps = [
        ":tfprof_constants",
        ":tfprof_node",
        ":tfprof_show_multi",
        ":tfprof_tensor",
        ":tfprof_utils",
        "//tensorflow/core:lib",
        "//tensorflow/core/platform:regexp",
        "//tensorflow/core/profiler:protos_all_cc",
        "//tensorflow/core/profiler:tfprof_options",
        "@com_google_absl//absl/strings",
        "@com_google_absl//absl/strings:str_format",
    ],
)

cc_library(
    name = "tfprof_code",
    srcs = ["tfprof_code.cc"],
    hdrs = ["tfprof_code.h"],
    deps = [
        ":tfprof_constants",
        ":tfprof_node",
        ":tfprof_show_multi",
        ":tfprof_timeline",
        ":tfprof_utils",
        "//tensorflow/core:lib",
        "//tensorflow/core:lib_internal",
        "//tensorflow/core/platform:regexp",
        "//tensorflow/core/profiler:protos_all_cc",
        "//tensorflow/core/profiler:tfprof_options",
        "@com_google_absl//absl/strings",
        "@com_google_absl//absl/strings:str_format",
        "@local_tsl//tsl/profiler/protobuf:profile_proto_cc",
    ],
)

cc_library(
    name = "tfprof_graph",
    srcs = ["tfprof_graph.cc"],
    hdrs = ["tfprof_graph.h"],
    deps = [
        ":tfprof_constants",
        ":tfprof_node",
        ":tfprof_show",
        ":tfprof_tensor",
        ":tfprof_utils",
        "//tensorflow/core:lib",
        "//tensorflow/core:protos_all_cc",
        "//tensorflow/core/platform:regexp",
        "//tensorflow/core/profiler:protos_all_cc",
        "//tensorflow/core/profiler:tfprof_options",
        "@com_google_absl//absl/strings:str_format",
    ],
)

cc_library(
    name = "tfprof_node_show",
    srcs = ["tfprof_node_show.cc"],
    hdrs = ["tfprof_node_show.h"],
    deps = [
        ":tfprof_constants",
        ":tfprof_node",
        ":tfprof_utils",
        "//tensorflow/core:lib",
        "//tensorflow/core/profiler:protos_all_cc",
        "//tensorflow/core/profiler:tfprof_options",
    ],
)

cc_library(
    name = "tfprof_show",
    srcs = ["tfprof_show.cc"],
    hdrs = ["tfprof_show.h"],
    deps = [
        ":tfprof_constants",
        ":tfprof_node",
        ":tfprof_node_show",
        ":tfprof_tensor",
        ":tfprof_timeline",
        ":tfprof_utils",
        "//tensorflow/c:checkpoint_reader",
        "//tensorflow/core:lib",
        "//tensorflow/core:protos_all_cc",
        "//tensorflow/core/platform:regexp",
        "//tensorflow/core/profiler:protos_all_cc",
        "//tensorflow/core/profiler:tfprof_options",
        "@com_google_absl//absl/strings",
        "@com_google_absl//absl/strings:str_format",
    ],
)

cc_library(
    name = "tfprof_show_multi",
    srcs = ["tfprof_show_multi.cc"],
    hdrs = ["tfprof_show_multi.h"],
    deps = [
        ":tfprof_constants",
        ":tfprof_node",
        ":tfprof_node_show",
        ":tfprof_scope",
        ":tfprof_show",
        ":tfprof_tensor",
        ":tfprof_timeline",
        ":tfprof_utils",
        "//tensorflow/core:lib",
        "//tensorflow/core/platform:regexp",
        "//tensorflow/core/profiler:protos_all_cc",
        "//tensorflow/core/profiler:tfprof_options",
        "@com_google_absl//absl/strings",
        "@com_google_absl//absl/strings:str_format",
    ],
)

tf_cc_test(
    name = "tfprof_show_test",
    size = "small",
    srcs = ["tfprof_show_test.cc"],
    data = ["//tensorflow/core/profiler/internal/testdata:profiler_testdata"],
    deps = [
        ":tfprof_constants",
        ":tfprof_stats",
        ":tfprof_tf_testlib",
        ":tfprof_utils",
        "//tensorflow/core:lib",
        "//tensorflow/core:test",
        "//tensorflow/core/profiler:protos_all_cc",
        "//tensorflow/core/profiler:tfprof_options",
    ],
)

tf_cc_test(
    name = "tfprof_timeline_test",
    size = "small",
    srcs = ["tfprof_timeline_test.cc"],
    data = ["//tensorflow/core/profiler/internal/testdata:profiler_testdata"],
    deps = [
        ":tfprof_constants",
        ":tfprof_stats",
        ":tfprof_tf_testlib",
        ":tfprof_utils",
        "//tensorflow/core:lib",
        "//tensorflow/core:lib_internal",
        "//tensorflow/core:test",
        "//tensorflow/core/profiler:protos_all_cc",
        "//tensorflow/core/profiler:tfprof_options",
    ],
)

cc_library(
    name = "tfprof_utils",
    srcs = ["tfprof_utils.cc"],
    hdrs = ["tfprof_utils.h"],
    copts = if_not_windows(["-Wno-sign-compare"]),
    deps = [
        "//tensorflow/core:lib",
        "//tensorflow/core/platform:regexp",
        "//tensorflow/core/profiler:tfprof_options",
        "@com_google_absl//absl/strings",
        "@com_google_absl//absl/strings:str_format",
    ],
)

cc_library(
    name = "print_model_analysis_hdr",
    hdrs = ["print_model_analysis.h"],
    deps = ["//tensorflow/core:framework"],
)

cc_library(
    name = "print_model_analysis",
    srcs = ["print_model_analysis.cc"],
    hdrs = ["print_model_analysis.h"],
    deps = [
        ":tfprof_stats",
        "//tensorflow/core/profiler:protos_all_cc",
        "//tensorflow/core/profiler:tfprof_options",
        "//tensorflow/core/profiler/internal/advisor:tfprof_advisor",
        "@com_google_absl//absl/strings:str_format",
    ],
    alwayslink = 1,
)

tf_cc_test(
    name = "tfprof_stats_test",
    size = "small",
    srcs = ["tfprof_stats_test.cc"],
    data = ["//tensorflow/core/profiler/internal/testdata:profiler_testdata"],
    deps = [
        ":tfprof_constants",
        ":tfprof_stats",
        ":tfprof_tf_testlib",
        ":tfprof_utils",
        "//tensorflow/core:lib",
        "//tensorflow/core:test",
        "//tensorflow/core/profiler:protos_all_cc",
        "//tensorflow/core/profiler:tfprof_options",
    ],
)

cc_library(
    name = "tfprof_tensor",
    srcs = ["tfprof_tensor.cc"],
    hdrs = ["tfprof_tensor.h"],
    copts = if_not_windows(["-Wno-sign-compare"]),
    deps = [
        "//tensorflow/core:framework",
        "//tensorflow/core:lib",
        "//tensorflow/core/profiler:protos_all_cc",
        "@com_google_absl//absl/strings",
        "@com_google_absl//absl/strings:str_format",
    ],
)

tf_cc_test(
    name = "tfprof_tensor_test",
    size = "small",
    srcs = ["tfprof_tensor_test.cc"],
    data = ["//tensorflow/core/profiler/internal/testdata:profiler_testdata"],
    deps = [
        ":tfprof_stats",
        ":tfprof_tf_testlib",
        ":tfprof_utils",
        "//tensorflow/core:lib",
        "//tensorflow/core:test",
        "//tensorflow/core/profiler:protos_all_cc",
        "//tensorflow/core/profiler:tfprof_options",
    ],
)

cc_library(
    name = "tfprof_constants",
    hdrs = ["tfprof_constants.h"],
)

cc_library(
    name = "tfprof_tf_testlib",
    testonly = 1,
    deps = [
        ":tfprof_tf_lib",
        "//tensorflow/core:test",
        "//tensorflow/core:test_main",
        "//tensorflow/core:testlib",
    ],
)

cc_library(
    name = "tfprof_tf_lib",
    deps = [
        "//tensorflow/core:lib",
        "//tensorflow/core:protos_all_cc",
        "//tensorflow/core/platform:regexp",
    ],
)
