# Final Exam - 3504

## DOCKERIZE TECHCO WEBSITE ON AWS EC2

### Author: Eduardo Raphael de Araujo


# Instructions:

This project containerized TechCo Company's website on AWS EC2

# Create AWS EC2
  - Create a key pair
  - Create a Linux EC2 Instance
  - Configure SSH and HTTP ports for external access

# Install Docker on EC2 Instance

  sudo yum install -y docker

Configur Docker service to run

  sudo service docker start

# Dockerhub

If you don't have a Dockerhub account, create one on Dockerhub.

# DockerFile

DockerFile was created and added to the root of the project.

# Github Actions

The following have been configured as repository secrets for the deploy.yml file:

Username of DockerHub - DOCKERHUB_USER
Password of DockerHub - DOCKERHUB_PWD
Docker Image name - DOCKERHUB_IMAGE
Container name - CONTAINER_NAME
IP from EC2 - EC2_PUBLIC_IP
User of the instance - EC2_USER
Key pair generated when creating the EC2 - SSH_PRIVATE_KEY

# Workflow

After every push to the main branch the GitHub Actions will generate the Docker Image, push it to DockerHub and then download the image on EC2 and build the container.




