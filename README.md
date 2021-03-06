> In progress...

# Infrastructure as a code - AWS

This project implements a infrastructure using Terraform, Ansible, Docker, and Jenkins, and it provides all resources into AWS Cloud.

![Infrastructure Schema AWS](https://github.com/mcosta21/infra-devops-aws/blob/main/.github/infra-schema-aws.png)

## Pipeline Jenkins

<div align="center">
  <img width="500" src="https://github.com/mcosta21/infra-devops-aws/blob/main/.github/pipeline-jenkins.png" alt="Pipeline Jenkins" />
</div>

## Terraform + Ansible - Docker Image

```bash
# Build the image
docker build -t terraform-ansible-image .\terraform-ansible-docker\

# See image created
docker image ls

# Run container from image
docker run --name terraform-ansible terraform-ansible-image

# See container created
docker container ls
```
