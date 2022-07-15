load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
  name = "rules_pkg",
  urls = [
    "https://mirror.bazel.build/github.com/bazelbuild/rules_pkg/releases/download/0.7.0/rules_pkg-0.7.0.tar.gz",
    "https://github.com/bazelbuild/rules_pkg/releases/download/0.7.0/rules_pkg-0.7.0.tar.gz",
  ],
  sha256 = "8a298e832762eda1830597d64fe7db58178aa84cd5926d76d5b744d6558941c2",
)

load("@rules_pkg//:deps.bzl", "rules_pkg_dependencies")

rules_pkg_dependencies()

load("@bazel_tools//tools/build_defs/repo:git.bzl", "git_repository")

git_repository(
  name = "rules_dotnet",
  remote = "https://github.com/bazelbuild/rules_dotnet",
  # branch = "next",
  commit = "5fc875093b558a199fbe739f0717dfe09ff626e5",
  shallow_since = "1655891408 +0000",
)

load(
  "@rules_dotnet//dotnet:repositories.bzl",
  "dotnet_register_toolchains",
  "rules_dotnet_dependencies",
)

rules_dotnet_dependencies()

dotnet_register_toolchains("dotnet", "6.0.300")

load("//deps:paket.bzl", "paket")

paket()
