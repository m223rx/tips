# Challenge: Maven Mastery – Automated Build and Dependency Management

## Difficulty
Medium

## Description
You are tasked with creating a **fully functional Java application** that demonstrates advanced Maven capabilities. The project must be set up from scratch (no existing project files) and showcase the following Maven features:

1. **Modular multi‑module structure** – at least three modules:
   - `core` – contains the main business logic.
   - `api` – defines an interface that `core` implements.
   - `app` – a simple console application that uses `core` through the `api` module.

2. **Dependency management** – use a parent `pom.xml` to centrally manage versions of common libraries (e.g., Google Guava, Apache Commons Lang) and enforce a consistent Java version across modules.

3. **Custom Maven plugin execution** – configure the **Maven Shade plugin** (or another plugin of your choice) to create an **executable “fat JAR”** for the `app` module that bundles all dependencies.

4. **Profiles** – define at least two Maven profiles:
   - `dev` – includes a logging framework (e.g., Log4j) and enables debug output.
   - `prod` – disables debug logs and sets an optimized compiler flag.

5. **Testing** – write at least one unit test per module using JUnit (or TestNG) and configure the **Maven Surefire plugin** to generate a test report.

Your final deliverable is the complete directory structure with all `pom.xml` files and source code that can be built and run using the standard Maven commands:

```bash
mvn clean install          # builds all modules and runs tests
mvn -Pdev package          # builds using the dev profile
mvn -Pprod package         # builds using the prod profile
java -jar app/target/app-*.jar   # runs the executable fat JAR
```

## Requirements
- Create a **parent `pom.xml`** that uses the `<modules>` section to aggregate the three sub‑modules.
- All modules must inherit from the parent POM using `<relativePath>` or `<parent>` configuration.
- Centralize the Java version (e.g., 17) and dependency versions in the parent POM.
- Use **Maven Enforcer plugin** to enforce the Java version and prevent the use of disallowed dependencies.
- Include a `README.md` that explains how to build and run the project, as well as a short description of the application's functionality.
- Ensure the project builds successfully on a fresh environment with only Maven installed (no IDE specific files).

## Bonus
- Add a **Maven Release plugin** configuration to automate version bumping and Git tagging.
- Publish the generated JAR to a local Maven repository using the **Maven Deploy plugin**.
- Include a **Dockerfile** that builds and runs the application inside a lightweight container, using Maven to compile the code during the Docker build.
- Integrate **SpotBugs** (or another static analysis tool) via the Maven SpotBugs plugin and make the build fail if any critical bugs are detected.