[![.github/workflows/deployment.yml](https://github.com/veidl/devops-blog/actions/workflows/deployment.yml/badge.svg)](https://github.com/veidl/devops-blog/actions/workflows/deployment.yml)

# DevOps Course Exercise 1

This project is a portfolio website for DevOps course exercise 1. The website is built with Next.js and Nextra.

## Workflows

All workflows can be found in the [.github/workflows](.github/workflows) folder.

### Development

On push (for every branch) following steps are triggered

* npm ci
* npm run lint
* npm run build (result of the build is ignored)

### Pull request

Merging to the main branch can only be done with a pull request. Pull request must pass the **Audit** and the **Lint & Build** pipeline.

### Deployment

When a pull request is merged to main the source code is dockerized and pushed
to [Dockerhub](https://hub.docker.com/r/veidl/blog)
