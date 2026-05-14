# Challenge: Build a Multi‑Module Java Project with Gradle

## Difficulty
Medium

## Description
You are tasked with creating a **multi‑module Java project** that uses **Gradle** as its build system. The project should consist of a **core library**, a **service module**, and an **application module** that depends on the other two. The goal is to set up a clean, maintainable Gradle build that demonstrates best practices such as:

- Using the Gradle Wrapper
- Applying the appropriate plugins
- Declaring inter‑module dependencies
- Configuring source sets and Java version
- Publishing a JAR of the core library to a local Maven repository

The project will be compiled, tested, and run via Gradle commands only.

## Requirements
- **Gradle Wrapper**: Include the wrapper (`gradlew`, `gradlew.bat`, and the `gradle/wrapper` directory) so the build can be run without a pre‑installed Gradle distribution.
- **Root `settings.gradle`**: Configure the root project to include the three subprojects: `core`, `service`, and `app`.
- **Plugins**:
  - Apply the `java-library` plugin to `core` and `service`.
  - Apply the `application` plugin to `app`.
- **Java Version**: Set source and target compatibility to **Java 11** for all modules.
- **Inter‑module Dependencies**:
  - `service` depends on `core`.
  - `app` depends on both `core` and `service`.
- **Source Layout**: Use the conventional Gradle directory structure (`src/main/java`, `src/test/java`).
- **Testing**: Add at least one JUnit 5 test in each module and configure the `test` task to use JUnit Platform.
- **Packaging**:
  - The `core` module must produce a JAR that can be published to a **local Maven repository** (`~/.m2/repository`).
  - The `app` module should define the main class and be runnable via `./gradlew run`.
- **Custom Task**: Create a Gradle task named `printVersions` in the root project that prints the Java version and the Gradle version being used.

## Bonus
- Add **code coverage** reporting using JaCoCo and generate an HTML report for the whole project.
- Configure a **continuous integration** workflow (e.g., GitHub Actions) that runs `./gradlew build` on every push.
- Use **Gradle Kotlin DSL** (`build.gradle.kts`) instead of Groovy for all build scripts.
- Implement a **release** task that:
  - Increments a semantic version number defined in a `version.txt` file.
  - Tags the commit with the new version.
  - Publishes the `core` JAR to a remote Maven repository (you can mock this with a local directory).