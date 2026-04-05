# Challenge: Automated CI/CD Pipeline for a Microservice

## Difficulty
Medium

## Description
You are part of a DevOps team responsible for delivering a simple web microservice written in any language of your choice (e.g., Node.js, Python, Go). The goal of this challenge is to design and implement an **automated CI/CD pipeline** that builds, tests, containerizes, and deploys the service to a Kubernetes cluster (or an equivalent container orchestration platform).

Your pipeline should be version‑controlled, reproducible, and trigger automatically on code changes. The final deliverable is a repository that contains:

1. The microservice source code (a minimal “Hello, World!” HTTP endpoint is sufficient).
2. All configuration files required for the CI/CD workflow.
3. Documentation on how to set up and run the pipeline locally and in a cloud environment.

## Requirements
- **Source Control**: Use Git (GitHub, GitLab, or Bitbucket) to host the project.
- **Build Automation**: Create a build script or use a build tool that:
  - Installs dependencies.
  - Runs unit tests (at least one test case).
  - Lints the code (optional but recommended).
- **Containerization**:
  - Write a Dockerfile that builds a lightweight image for the service.
  - Ensure the image is built automatically as part of the pipeline.
- **CI Workflow**:
  - Use a CI platform (GitHub Actions, GitLab CI, Jenkins, CircleCI, etc.).
  - The pipeline must automatically run on each push to the main branch.
  - Steps include: checkout, build, test, lint, Docker image build, and push to a container registry (Docker Hub, GitHub Container Registry, GCR, etc.).
- **CD Deployment**:
  - Deploy the Docker image to a Kubernetes cluster (Minikube, Kind, K3s, or a managed service like GKE/EKS/AKS).
  - Provide Kubernetes manifests (Deployment, Service, Ingress if needed) or Helm chart.
  - The deployment should be triggered automatically after a successful image push.
- **Versioning**:
  - Tag Docker images with the Git commit SHA and/or semantic version.
- **Documentation**:
  - A `README.md` explaining:
    - How to run the service locally.
    - How to set up the CI/CD pipeline.
    - How to access the deployed service.
    - Any prerequisites (e.g., Docker, Kubernetes cluster, credentials).

## Bonus
- Implement **blue‑green** or **canary** deployment strategies.
- Include **security scanning** of Docker images (e.g., Trivy, Clair) within the CI pipeline.
- Set up **automatic rollbacks** on deployment failures.
- Use **Infrastructure as Code** (Terraform, Pulumi, or CloudFormation) to provision the Kubernetes cluster and any required cloud resources.
- Add **monitoring and alerting** (Prometheus + Grafana, or a cloud provider’s monitoring solution) for the deployed service.
- Create a **GitOps** workflow using tools like Argo CD or Flux CD to manage deployments.