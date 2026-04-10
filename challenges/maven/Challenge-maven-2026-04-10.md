# Challenge: Maven Multi‑Module Build & Custom Plugin

## Difficulty  
Medium

## Description  
You are tasked with creating a **Maven** based Java project that demonstrates a realistic multi‑module setup and includes a custom Maven plugin. The project should consist of three modules:

1. **core** – contains the main business logic.  
2. **api** – provides a RESTful API that depends on `core`.  
3. **cli** – a command‑line interface that also depends on `core` and uses the API to make HTTP calls.

In addition to the multi‑module structure, you must develop a **custom Maven plugin** that will:

- Scan all Java source files in the `core` module for classes annotated with `@Deprecated`.
- Generate a report (`target/deprecated-report.txt`) listing the fully qualified class names and the line numbers where the deprecations occur.
- Fail the build if more than **5** deprecated classes are found.

Your overall goal is to set up the Maven `pom.xml` files correctly, implement the custom plugin, and ensure the build behaves as specified.

## Requirements  

- **Project Structure**
  - Use a parent `pom.xml` that defines the common Maven version, Java version (Java 17), and shared plugin configurations.
  - Each module (`core`, `api`, `cli`) must have its own `pom.xml` that inherits from the parent.
  - `api` must depend on `core`; `cli` must depend on both `core` and `api`.

- **Dependencies**
  - `core` uses only the standard JDK (no external dependencies).
  - `api` uses **Spring Boot** (or **Jakarta EE**) to expose a simple REST endpoint.
  - `cli` uses a library such as **Picocli** or **JCommander** for command‑line parsing.

- **Custom Plugin**
  - Implement the plugin in Java and package it as a Maven plugin (`maven-plugin` packaging).
  - The plugin should be bound to the `verify` phase of the build lifecycle.
  - The report must be generated in the `core` module’s `target` directory.
  - If the count of deprecated classes exceeds 5, the plugin should abort the build with a clear error message.

- **Build Verification**
  - Running `mvn clean verify` from the root should compile all modules, execute the custom plugin, generate the report, and succeed only when the deprecation limit is respected.
  - Provide a sample `README.md` in the root explaining how to run the build, generate the report, and interpret its output.

## Bonus  

- **CI Integration**: Add a simple **GitHub Actions** workflow that runs the Maven build on every push and fails the job if the custom plugin aborts the build.
- **Plugin Configuration**: Make the maximum allowed number of deprecated classes configurable via a plugin parameter (default = 5) and demonstrate usage in the parent `pom.xml`.
- **Documentation Generation**: Extend the custom plugin to also generate a Markdown version of the deprecation report (`DEPRECATED.md`) with links to the source files on GitHub (assume the repository URL is known).