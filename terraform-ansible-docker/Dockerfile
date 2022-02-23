# Pull base image.
FROM ubuntu:latest

ENV TERRAFORM_VERSION 0.14.11

RUN \

# Update packages
apt-get update -y && \

# Install unzip
apt-get install unzip -y && \

# Install wget
apt-get install wget -y && \

# Install vim
apt-get install vim -y


################################
# Install python
################################

RUN apt-get install -y python3-pip
RUN pip3 install --upgrade pip

# Check that it's installed -> python3 -V && pip --version

################################
# Install Terraform
################################

# Download terraform for linux -> https://releases.hashicorp.com/terraform/
RUN wget -O /terraform.zip "https://releases.hashicorp.com/terraform/${TERRAFORM_VERSION}/terraform_${TERRAFORM_VERSION}_linux_amd64.zip"

# Unzip terraform
RUN unzip terraform.zip

# Move to local bin
RUN mv terraform /usr/local/bin/

# Check that it's installed -> terraform --version 

################################
# Install Ansible
################################

RUN apt-get install ansible -y