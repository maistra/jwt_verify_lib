licenses(["notice"])  # Apache 2

package(default_visibility = ["//visibility:public"])

exports_files(["LICENSE"])

cc_library(
    name = "jwt_verify_lib",
    srcs = [
        "src/check_audience.cc",
        "src/jwks.cc",
        "src/jwt.cc",
        "src/status.cc",
        "src/struct_utils.cc",
        "src/verify.cc",
    ],
    hdrs = [
        "jwt_verify_lib/check_audience.h",
        "jwt_verify_lib/jwks.h",
        "jwt_verify_lib/jwt.h",
        "jwt_verify_lib/status.h",
        "jwt_verify_lib/struct_utils.h",
        "jwt_verify_lib/verify.h",
        "src/common.h",
    ],
    deps = [
        "//external:abseil_flat_hash_set",
        "//external:abseil_strings",
        "//external:abseil_time",
        "//external:protobuf",
	"//external:bssl_wrapper_lib",
        "@openssl//:openssl-lib",
    ],
)

cc_test(
    name = "check_audience_test",
    timeout = "short",
    srcs = [
        "src/check_audience_test.cc",
    ],
    linkopts = [
        "-lm",
        "-lpthread",
    ],
    linkstatic = 1,
    deps = [
        ":jwt_verify_lib",
        "//external:googletest_main",
    ],
)

cc_test(
    name = "jwt_test",
    timeout = "short",
    srcs = [
        "src/jwt_test.cc",
    ],
    linkopts = [
        "-lm",
        "-lpthread",
    ],
    linkstatic = 1,
    deps = [
        ":jwt_verify_lib",
        "//external:googletest_main",
    ],
)

cc_test(
    name = "jwks_test",
    timeout = "short",
    srcs = [
        "src/jwks_test.cc",
        "src/test_common.h",
    ],
    linkopts = [
        "-lm",
        "-lpthread",
    ],
    linkstatic = 1,
    deps = [
        ":jwt_verify_lib",
        "//external:googletest_main",
    ],
)

cc_test(
    name = "verify_x509_test",
    timeout = "short",
    srcs = [
        "src/test_common.h",
        "src/verify_x509_test.cc",
    ],
    linkopts = [
        "-lm",
        "-lpthread",
    ],
    linkstatic = 1,
    deps = [
        ":jwt_verify_lib",
        "//external:googletest_main",
    ],
)

cc_test(
    name = "verify_audiences_test",
    timeout = "short",
    srcs = [
        "src/test_common.h",
        "src/verify_audiences_test.cc",
    ],
    linkopts = [
        "-lm",
        "-lpthread",
    ],
    linkstatic = 1,
    deps = [
        ":jwt_verify_lib",
        "//external:googletest_main",
    ],
)

cc_test(
    name = "verify_time_test",
    timeout = "short",
    srcs = [
        "src/test_common.h",
        "src/verify_time_test.cc",
    ],
    linkopts = [
        "-lm",
        "-lpthread",
    ],
    linkstatic = 1,
    deps = [
        ":jwt_verify_lib",
        "//external:googletest_main",
    ],
)

cc_test(
    name = "verify_jwk_rsa_test",
    timeout = "short",
    srcs = [
        "src/test_common.h",
        "src/verify_jwk_rsa_test.cc",
    ],
    linkopts = [
        "-lm",
        "-lpthread",
    ],
    linkstatic = 1,
    deps = [
        ":jwt_verify_lib",
        "//external:googletest_main",
    ],
)

cc_test(
    name = "verify_jwk_rsa_pss_test",
    timeout = "short",
    srcs = [
        "src/test_common.h",
        "src/verify_jwk_rsa_pss_test.cc",
    ],
    linkopts = [
        "-lm",
        "-lpthread",
    ],
    linkstatic = 1,
    deps = [
        ":jwt_verify_lib",
        "//external:googletest_main",
    ],
)

cc_test(
    name = "verify_jwk_ec_test",
    timeout = "short",
    srcs = [
        "src/test_common.h",
        "src/verify_jwk_ec_test.cc",
    ],
    linkopts = [
        "-lm",
        "-lpthread",
    ],
    linkstatic = 1,
    deps = [
        ":jwt_verify_lib",
        "//external:googletest_main",
    ],
)

cc_test(
    name = "verify_jwk_hmac_test",
    timeout = "short",
    srcs = [
        "src/test_common.h",
        "src/verify_jwk_hmac_test.cc",
    ],
    linkopts = [
        "-lm",
        "-lpthread",
    ],
    linkstatic = 1,
    deps = [
        ":jwt_verify_lib",
        "//external:googletest_main",
    ],
)

cc_test(
    name = "verify_jwk_okp_test",
    timeout = "short",
    srcs = [
        "src/test_common.h",
        "src/verify_jwk_okp_test.cc",
    ],
    linkopts = [
        "-lm",
        "-lpthread",
    ],
    linkstatic = 1,
    deps = [
        ":jwt_verify_lib",
        "//external:googletest_main",
    ],
)

cc_test(
    name = "verify_pem_rsa_test",
    timeout = "short",
    srcs = [
        "src/test_common.h",
        "src/verify_pem_rsa_test.cc",
    ],
    linkopts = [
        "-lm",
        "-lpthread",
    ],
    linkstatic = 1,
    deps = [
        ":jwt_verify_lib",
        "//external:googletest_main",
    ],
)

cc_test(
    name = "verify_pem_ec_test",
    timeout = "short",
    srcs = [
        "src/test_common.h",
        "src/verify_pem_ec_test.cc",
    ],
    linkopts = [
        "-lm",
        "-lpthread",
    ],
    linkstatic = 1,
    deps = [
        ":jwt_verify_lib",
        "//external:googletest_main",
    ],
)

cc_test(
    name = "verify_pem_okp_test",
    timeout = "short",
    srcs = [
        "src/test_common.h",
        "src/verify_pem_okp_test.cc",
    ],
    linkopts = [
        "-lm",
        "-lpthread",
    ],
    linkstatic = 1,
    deps = [
        ":jwt_verify_lib",
        "//external:googletest_main",
    ],
)
