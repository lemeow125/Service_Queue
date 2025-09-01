# Service Queue Templates

This repository contains a collection of templates tailored for DevOps practices designed to assist with Service Queue deployments.

## `build.yml` Environment Variables

| Variable Name              | Description                                      | Value Value                                      |
|----------------------------|--------------------------------------------------|----------------------------------------------------|
| `FORGEJO_REGISTRY_URL`     | Artifact registry to push built image to         | `git.06222001.xyz`                                 |
| `FORGEJO_REGISTRY_USERNAME`| Credentials used to push to the image registry   | `N/A (redacted)`                                   |
| `FORGEJO_REGISTRY_PASSWORD`| Credentials used to push to the image registry   | `N/A (redacted)`                                   |
| `REGISTRY_IMAGE_TAG`       | Docker image container tag to push to registry                      | `git.06222001.xyz/keannu125/drf_template:latest`   |
| `DISCORD_WEBHOOK_ID`       | Discord Webhook ID used for Build Status Updates | `N/A (redacted)`                                   |

## `deploy.yml` Environment Variables

| Variable Name        | Description                                         | Value                        |
|----------------------|-----------------------------------------------------|--------------------------------------|
| `SSH_HOST`           | SSH host for deployment                            | `N/A (redacted)`              |
| `PROJECT_DIRECTORY`  | Directory on remote host for deployment            | `/mnt/nvme/files/docker projects/drf_template`                     |
| `SSH_KEY`            | Private SSH key for authentication                 | `N/A (redacted)`              |
| `REGISTRY_IMAGE_TAG` | Docker image tag to deploy                         | `git.06222001.xyz/keannu125/drf_template:latest` |
| `DOCKER_VOLUME_DB`   | Docker volume name for the database                | `drf_template_db_data`               |
| `DOCKER_COMPOSE_URL` | URL to fetch docker-compose.yml                    | `https://raw.githubusercontent.com/lemeow125/DRF_Template/refs/heads/master/docker-compose.prod.yml` |
| `DISCORD_WEBHOOK_ID` | Discord Webhook ID for deployment notifications    | `N/A (redacted)`                     |
| `DISCORD_WEBHOOK_TOKEN` | Discord Webhook Token for deployment notifications | `N/A (redacted)`                  |

> **Note:**  
> Actual values may differ based on your pipeline configuration.
> Usage of `.deploy_ephemeral.yml` does not require `DOCKER_VOLUME_DB`
> For more information, consult your Woodpecker CI/CD maintainer.