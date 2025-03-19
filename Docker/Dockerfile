# Use the Official Node.js 16 image as base image
FROM node:20

# Set the working directory in the container (Linux)
WORKDIR /app

#Install Newman globally
RUN npm install -g newman

#Install Newman html report
RUN npm install -g newman-reporter-html

#Install Newman Reporter HTMLExtra
RUN npm install -g newman-reporter-htmlextra

# Copy your postman collection and environment files to the working directory
COPY Gorestenvironment.json .
COPY GoRestAPIWorkflow.json .

#set the Command to run Newman and execute your Postman collection
CMD ["newman", "run", "Gorestenvironment.json", "-e", "GoRestAPIWorkflow.json", "-r", "cli"]