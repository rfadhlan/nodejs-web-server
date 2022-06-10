# nodejs-web-server
---
## Build With
* [Node.js](https://nodejs.org)

## Architecture


# :cloud: How To Deploy Flask API On Google Cloud Platform (Cloud Run)
  1. Create Flask API
  2. Create Dockerfile 
     ```Dockerfile
     ...
     FROM python:3.9.0
     # Copy local code to the container image
     COPY . /app

     # Sets the working directory
     WORKDIR /app

     # Upgrade PIP
     RUN pip install --upgrade pip

     #Install python libraries from requirements.txt
     RUN pip install --no-cache-dir -r requirements.txt

     # Set $PORT environment variable
     ENV PORT 8080

     # Run the web service on container startup
     CMD exec gunicorn --bind :$PORT --workers 1 --threads 8 --timeout 0 main:app
     ```
  3. Go to Google Cloud Platform (https://console.cloud.google.com/)
  4. Create a Project
  5. Click cloud shell to clone git
  6. Clone the git with this command
     ```Command
     ...
     git clone (github links https)
     ```
  7. Then type `ls` to see that we have sucess clone the github
  8. Change the directory to github, type `cd (directory that we want to use)`
  9. Clcik Terminal
  10. In Terminal, we click `cloud clone`
  11. Than we click `Deploy to Cloud Run`
  12. In  `Deploy to Cloud Run` we can settings configurations before deploy
  13. And than after we settings the configurations we clik `Deploy`
