workspace(name = "com_github_containous_traefik")

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "io_bazel_rules_go",
    sha256 = "7be7dc01f1e0afdba6c8eb2b43d2fa01c743be1b9273ab1eaf6c233df078d705",
    urls = ["https://github.com/bazelbuild/rules_go/releases/download/0.16.5/rules_go-0.16.5.tar.gz"],
)

http_archive(
    name = "bazel_gazelle",
    sha256 = "6e875ab4b6bf64a38c352887760f21203ab054676d9c1b274963907e0768740d",
    urls = ["https://github.com/bazelbuild/bazel-gazelle/releases/download/0.15.0/bazel-gazelle-0.15.0.tar.gz"],
)

load("@io_bazel_rules_go//go:def.bzl", "go_register_toolchains", "go_rules_dependencies")

go_rules_dependencies()

go_register_toolchains()

load("@bazel_gazelle//:deps.bzl", "gazelle_dependencies", "go_repository")

gazelle_dependencies()

go_repository(
    name = "com_github_containous_go_bindata",
    importpath = "github.com/containous/go-bindata",
    sha256 = "666333eef6f2ed99f8b54c1f7b97912e985f65a4b62f3aacf0b312d1ffbdce18",
    strip_prefix = "go-bindata-532cb0b0736b109aefe85e24e37a2ef35eafc6a8",
    urls = ["https://github.com/containous/go-bindata/archive/532cb0b0736b109aefe85e24e37a2ef35eafc6a8.tar.gz"],
)
