# Challenge: Automated Docker Image Builder & Deployer

## Difficulty  
Medium

## Description  
You are part of a team that wants to streamline the process of delivering a microservice to a Kubernetes cluster. Your task is to create a command‑line tool (or script) that automates the entire release pipeline for a given Git repository:

1. **Clone** the repository (or work with the current working directory).  
2. **Detect** the latest Git commit hash and use it as the image tag.  
3. **Build** a Docker image using a provided `Dockerfile`.  
4. **Push** the image to a container registry (e.g., Docker Hub, GitHub Container Registry, or a private registry).  
5. **Update** a specified Kubernetes Deployment to use the newly pushed image tag, then perform a rolling update.  

Your tool should be usable in CI environments (e.g., GitHub Actions, GitLab CI) as well as locally by developers.

## Requirements  
- The tool must be executable from the command line with clear flags/arguments (e.g., `--repo`, `--registry`, `--deployment`, `--namespace`).  
- It should read authentication credentials for the Docker registry and the Kubernetes cluster from environment variables or standard config files (`~/.docker/config.json`, `~/.kube/config`).  
- If any step fails (clone, build, push, or deployment update), the tool must exit with a non‑zero status and provide a helpful error message.  
- Implement basic logging (info, warning, error) and an optional `--verbose` flag for detailed output.  
- The program must be written in a language commonly used for DevOps tasks (e.g., Python, Go, Bash).  
- Include a `README.md` that explains how to install, configure, and run the tool, plus examples of typical usage.  
- Provide a sample `Dockerfile` and a minimal Kubernetes manifest (Deployment) that can be used to test the tool.

## Bonus  
- Add support for **multi‑architecture** builds (e.g., `linux/amd64` and `linux/arm64`) using Docker Buildx.  
- Implement a **rollback** feature that reverts the Deployment to the previous image tag if the new rollout fails health checks.  
- Allow the tool to **detect** and skip building if the current commit hash already exists as a tag in the registry.  
- Provide an optional **webhook** endpoint that can be triggered by a CI system, returning JSON status of the pipeline execution.  
- Write unit tests for the core functionality and set up a CI workflow that validates the tool on every commit.  