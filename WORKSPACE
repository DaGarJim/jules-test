load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "rules_jvm_external",
    strip_prefix = "rules_jvm_external-6.2",
    sha256 = "06de74490a5f80b59a72b795a2d81f54d69f09e6c433c29a27c01bd4c9e5e792",
    url = "https://github.com/bazelbuild/rules_jvm_external/archive/refs/tags/6.2.zip",
)

load("@rules_jvm_external//:defs.bzl", "maven_install")

maven_install(
    artifacts = [
        "org.springframework.boot:spring-boot-starter-web:3.3.1",
        "org.springframework.boot:spring-boot-starter-test:3.3.1",
    ],
    repositories = [
        "https://repo1.maven.org/maven2",
    ],
    name = "maven",
)

http_archive(
    name = "rules_java",
    sha256 = "f36de739a855a44cb367c8282300b659c424d17300c3b3a30c5e69e771c46328",
    strip_prefix = "rules_java-7.6.0",
    url = "https://github.com/bazelbuild/rules_java/releases/download/7.6.0/rules_java-7.6.0.tar.gz",
)

load("@rules_java//java:defs.bzl", "java_library")
