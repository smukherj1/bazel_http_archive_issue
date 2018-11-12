workspace(name="smukherj1_bazel_http_archive_issue")

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "io_bazel_rules_docker",
    strip_prefix = "rules_docker-e991b9e50b6ea7941011125c8e5755d8dd870abc",
    urls = ["https://github.com/bazelbuild/rules_docker/archive/e991b9e50b6ea7941011125c8e5755d8dd870abc.tar.gz"],
)

load("@io_bazel_rules_docker//container:container.bzl", container_repositories = "repositories")


# Loads bazel skylib 0.2.0 that doesn't have @bazel_skylib//:bzl_library.bzl
container_repositories()

# Skylark documentation generator
http_archive(
  name = "io_bazel_rules_sass",
  strip_prefix = "rules_sass-c93cadb20753f4e4d4eabe83f8ea882bfb8f2efe",
  url = "https://github.com/bazelbuild/rules_sass/archive/c93cadb20753f4e4d4eabe83f8ea882bfb8f2efe.tar.gz",
)

# Comment out the following line for the issue to go away!
load("@io_bazel_rules_sass//:package.bzl", "rules_sass_dependencies")

# Load bazel skylib that has @bazel_skylib//:bzl_library.bzl
http_archive(
    name = "bazel_skylib",
    strip_prefix = "bazel-skylib-8cecf885c8bf4c51e82fd6b50b9dd68d2c98f757",
    urls = ["https://github.com/bazelbuild/bazel-skylib/archive/8cecf885c8bf4c51e82fd6b50b9dd68d2c98f757.tar.gz"],
)