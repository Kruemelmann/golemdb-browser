load("@aspect_rules_deno//deno:defs.bzl", "deno_binary")

deno_binary(
    name = "golemdb-browser",
    allow = ["write","env","read","net"],
    main = "main.ts",
    unstable_apis = True,
    deps = [
        "main.ts",
        "dev.ts",
        "fresh.gen.ts",
        "//routes:routes",
    ],
)
