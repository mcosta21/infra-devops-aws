# Pull base image.
FROM ubuntu:latest

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
# Install Terraform
################################

# Download terraform for linux -> https://releases.hashicorp.com/terraform/
RUN wget https://releases.hashicorp.com/terraform/0.14.11/terraform_0.14.11_linux_amd64.zip

# Unzip terraform
RUN unzip terraform_0.14.11_linux_amd64.zip

# Move to local bin
RUN mv terraform /usr/local/bin/

# Check that it's installed
RUN terraform --version 

################################
# Install python
################################

RUN apt-get install -y python3-pip
RUN pip3 install --upgrade pip
RUN python3 -V
RUN pip --version