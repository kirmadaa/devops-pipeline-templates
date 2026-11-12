# devops-pipeline-templates

Reusable CI/CD pipeline templates for **GitHub Actions** and **Azure DevOps**: build, test, container image, and gated multi-environment deploys.

Copy a template into your own repo and adjust the values marked `CHANGE`. The templates live under `templates/` on purpose, so they don't run on this repository.

## Templates

| Template | Platform | What it does |
|---|---|---|
| [`templates/github-actions/ci.yml`](templates/github-actions/ci.yml) | GitHub Actions | Install, lint, test and build a Node.js project on a version matrix, with concurrency control and a least-privilege token |
| [`templates/github-actions/docker-publish.yml`](templates/github-actions/docker-publish.yml) | GitHub Actions | Build a container image with Buildx and layer caching, then publish it to GHCR with branch, semver and SHA tags |
| [`templates/azure-devops/azure-pipelines.yml`](templates/azure-devops/azure-pipelines.yml) | Azure DevOps | Multi-stage pipeline: build and test, deploy to staging, then deploy to production behind environment approvals |

## How to use

1. Copy the template you need into your repository (GitHub Actions files go in `.github/workflows/`, the Azure DevOps file goes in the repo root).
2. Search for `CHANGE` and adjust the marked values.
3. For Azure DevOps, create the `staging` and `production` environments and add approvers to `production`.

## Author

Himanshu Tripathi, freelance DevOps & Cloud engineer (AWS, Azure, Azure DevOps, Kubernetes, OpenShift). See [my profile](https://github.com/kirmadaa) for services and contact details.
