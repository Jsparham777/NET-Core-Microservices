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