# Udemy.com : .NET Core Microservices 

# Docker setup
# Setup shared drive
# - Right click docker icon in taskbar and select settings
# - Click Shared Drives
# - Check the drive containing the Actio project
# - Enter the Windows account password when prompted
# - Ensure the checkbox next to the drive letter is checked when complete

# Docker commands
#
# IMPORTANT: Run Powershell as Admin
#
# To build the api and service images
# cd to C:\Users\jspar\source\repos\GitHub\micro-test-system\sandBoxes\JS>
# Docker build -f Dockerfile-api -t actio.api .
# Docker build -f Dockerfile-activities -t actio.services.activities .
# Docker build -f Dockerfile-identity -t actio.services.identity .


# To run the container
# cd to C:\Users\jspar\source\repos\GitHub\micro-test-system\sandBoxes\JS>
# Docker-compose up

# Docker-compose down

# Publishing images to docker hub
# Tag the image
# docker tag actio.api [dockerhub username]/actio.api
# 
# login to dockerhub
# docker login [Can provide different url i.e actio.azure.uk] 
# enter username
# enter password
#
# Push the image to docker hub
# docker push [dockerhub username]/actio.api
# 

# To tag and push
# docker push [dockerhub username]/actio.api:tagnam

# Pull the image from dockerhub
# docker pull [dockerhub username]/actio.api

# repeat for actio.services.identity and actio.services.activities
# Dont forget to create the repos in dockerhub website first

# Running on Ubuntu VM using VirtualBox
# Install Ubuntu and sudo apt get update
# Install VirtualBox guest editions
# Install docker...
# First, in order to ensure the downloads are valid, add the GPG key for the official Docker repository to your system:

# curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
# Add the Docker repository to APT sources:

# sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
# Next, update the package database with the Docker packages from the newly added repo:

# sudo apt-get update
# Make sure you are about to install from the Docker repo instead of the default Ubuntu 16.04 repo:

# apt-cache policy docker-ce
# You should see output similar to the follow:

# Output of apt-cache policy docker-ce
# docker-ce:
#   Installed: (none)
#   Candidate: 18.06.1~ce~3-0~ubuntu
#   Version table:
#      18.06.1~ce~3-0~ubuntu 500
#         500 https://download.docker.com/linux/ubuntu xenial/stable amd64 Packages

# Notice that docker-ce is not installed, but the candidate for installation is from the Docker repository for Ubuntu 16.04 (xenial).

# Finally, install Docker:

# sudo apt-get install -y docker-ce
# Docker should now be installed, the daemon started, and the process enabled to start on boot. Check that it's running:

# sudo systemctl status docker
# 
# 
# 
# create a shared folder from the VirutalBox Settings menu:
# - Folder Path: [path to windows folder to be shared]
# - Folder Name: ubuntu_shared
# - Read-only: checked
# - Auto-mount: checked
# - Mount point: blank
# - Make Permanent: checked
# Open a Terminal window in Ubuntu
#  mkdir ~/shared-windows10
#  sudo mount -t vboxsf ubuntu_shared ~/shared-windows10