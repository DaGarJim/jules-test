# Core Bank Platform

This repository contains the source code for the Core Bank Platform, a monorepo built with Bazel.

## Structure

The repository is structured as a monorepo with the following directories:

*   `apps/`: Contains the individual applications of the platform.
    *   `apps/onboarding/hello-world`: A "Hello World" Spring Boot microservice.
*   `libs/`: Contains shared libraries.
*   `infra/`: Contains infrastructure-as-code, including the `skaffold.yaml` file.
*   `docs/`: Contains documentation.

## Spec-Driven Development

This project is set up for spec-driven development using `spec-kit`. The `.specify/` and `.github/` directories contain the configuration for this.

## Bazel

The project uses Bazel as the build system. The Bazel configuration is in the `WORKSPACE`, `.bazelversion`, and root `BUILD` files.

### Building and Running the "Hello World" Microservice

To build the "Hello World" microservice, run the following command from the root of the repository:

```bash
bazel build //apps/onboarding/hello-world:hello-world_deploy.jar
```

To run the microservice, you can use the following command:

```bash
java -jar bazel-bin/apps/onboarding/hello-world/hello-world_deploy.jar
```

Alternatively, you can use `bazel run`:

```bash
bazel run //apps/onboarding/hello-world:hello-world
```

The application will be available at `http://localhost:8080`.