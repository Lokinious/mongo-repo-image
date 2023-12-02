# MongoDB Docker Setup

This repository contains a Dockerfile for setting up a MongoDB instance with basic authentication. Follow the steps below to run the MongoDB image.

## Prerequisites

Make sure you have Docker installed on your machine. You can download Docker from [here](https://www.docker.com/get-started).

## Steps to Run MongoDB Docker Image

```bash
# Clone this repository to your local machine:
git clone https://github.com/your-username/your-repo.git
cd your-repo

# Build the Docker image:
docker build -t my-mongodb-image .

# Run the MongoDB container:
docker run -d --name my-mongodb-container -p 27017:27017 my-mongodb-image

# Verify that the MongoDB container is running:
docker ps

# Connect to MongoDB using a MongoDB client or use the connection string in your application.
# Connection String:
# mongodb://admin:adminpassword@localhost:27017
# Replace `admin` with your desired username and `adminpassword` with your chosen password.

# To stop the MongoDB container, use the following command:
docker stop my-mongodb-container

## Additional Notes

- The default root username is set to `admin`, and the password is set to `adminpassword` in this example. Please update these credentials in both the Dockerfile and your connection string for security purposes.

- Ensure that you handle sensitive information securely, especially in production environments.

- For more information on configuring MongoDB authentication and security, refer to the [MongoDB documentation](https://docs.mongodb.com/manual/core/authentication/).
