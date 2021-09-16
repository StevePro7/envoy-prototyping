# envoy-prototyping
Envoy prototyping repository


.bazelrc
.clang-tidy


BUILD
:~/GitHub/StevePro7/envoy-prototyping/bazel/external

ignore some dependencies here
except google test
e.g.
deps = [
"@com_google_googletest//:gtest",
],


Issue
Error:(7, 11) no such package '@com_google_googletest//': The repository '@com_google_googletest' could not be resolved and referenced by '//bazel/external:all_external'

Solution
Workspace
load("//bazel:repositories.bzl", "envoy_dependencies")