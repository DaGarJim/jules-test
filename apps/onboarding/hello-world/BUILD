java_library(
    name = "lib",
    srcs = glob(["src/main/java/**/*.java"]),
    deps = [
        "@maven//:org_springframework_boot_spring_boot_starter_web",
    ],
)

java_binary(
    name = "hello-world",
    runtime_deps = [
        ":lib",
        "@maven//:org_springframework_boot_spring_boot_starter_web",
    ],
    main_class = "com.example.helloworld.HelloWorldApplication",
)