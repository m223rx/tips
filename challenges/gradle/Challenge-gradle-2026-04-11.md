# Challenge: Build a Custom Gradle Plugin for Code Quality

## Difficulty  
Medium / Hard  

## Description  
You are tasked with creating a reusable Gradle plugin that helps a Java (or Kotlin) project maintain a high level of code quality. The plugin should bundle together a set of static analysis tools (e.g., Checkstyle, SpotBugs, and Detekt for Kotlin) and provide a single, convenient task to run all of them. It must be publishable to a local Maven repository so that other projects can apply it using the `plugins` block.  

The plugin should be written using the **Gradle Kotlin DSL** (or Groovy if you prefer) and include proper documentation, versioning, and sensible defaults that can be overridden by the consuming project.

## Requirements  

1. **Plugin Structure**  
   - Create a Gradle project that builds a **Gradle plugin** (i.e., `java-gradle-plugin`).  
   - The plugin must have an appropriate `Plugin` implementation class that registers all necessary tasks and extensions.  

2. **Bundled Tools**  
   - Include **Checkstyle** for Java, **SpotBugs** for Java, and **Detekt** for Kotlin (or any two static analysis tools of your choice).  
   - Configure each tool with a default configuration file packaged inside the plugin JAR.  

3. **Custom Task**  
   - Provide a single task called `codeQualityCheck` that depends on the individual analysis tasks (e.g., `checkstyleMain`, `spotbugsMain`, `detekt`).  
   - The task should generate a combined HTML report summarizing the results of all analyses.  

4. **Extension for Customization**  
   - Expose an extension (e.g., `codeQuality {}`) that allows the consuming build to:  
     - Enable/disable each analysis tool individually.  
     - Override the location of configuration files.  
     - Set the version of each tool.  

5. **Publishing**  
   - Publish the plugin to a **local Maven repository** (`~/.m2/repository`) using the `maven-publish` plugin.  
   - Provide a `pluginBundle` (or `gradlePlugin` DSL) entry so that the plugin can be applied via:  

   ```kotlin
   plugins {
       id("com.example.code-quality") version "1.0.0"
   }
   ```

6. **Documentation**  
   - Write a concise `README.md` that explains:  
     - How to apply the plugin.  
     - How to configure the extension.  
     - How to locate the generated report.  

7. **Testing**  
   - Create a separate sample Java/Kotlin project that applies your plugin from the local Maven repository and demonstrates:  
     - Running `./gradlew codeQualityCheck`.  
     - Overriding at least one configuration option via the extension.  

## Bonus  

- **CI Integration**: Provide a sample GitHub Actions workflow that runs `codeQualityCheck` on each push and fails the build if any violations are found.  
- **Multi‑project Support**: Ensure the plugin works correctly in a multi‑module Gradle build, aggregating reports from all subprojects into a single root report.  
- **Auto‑Fix**: Add an optional task (e.g., `codeQualityFix`) that attempts to automatically resolve style violations using tools that support auto‑formatting (such as Spotless).  
- **Version Catalog**: Publish a version catalog file (`versions.toml`) alongside the plugin to simplify version management for the bundled tools.  