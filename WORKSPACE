load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")
http_archive(
    name = "aspect_rules_deno",
    sha256 = "cfda7aeb308082a4525f391b66e81d4f15bd05c3f0a5131e4645e74ea1e32760",
    strip_prefix = "rules_deno-0.3.0",
    url = "https://github.com/aspect-build/rules_deno/archive/refs/tags/v0.3.0.tar.gz",
)

######################
# rules_deno setup #
######################

load(
    "@aspect_rules_deno//deno:repositories.bzl",
    "LATEST_VERSION",
    "deno_register_toolchains",
    "rules_deno_dependencies",
)

# Fetches the rules_deno dependencies.
# If you want to have a different version of some dependency,
# you should fetch it *before* calling this.
# Alternatively, you can skip calling this function, so long as you've
# already fetched all the dependencies.
rules_deno_dependencies()

deno_register_toolchains(
    name = "deno",
    deno_version = LATEST_VERSION,
)
