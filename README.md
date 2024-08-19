# Welcome to the MongoDB Docker Setup! 🍃
Spin up your own MongoDB database with a sleek, web-based admin interface in just a few simple steps! This project leverages Docker Compose to seamlessly deploy both MongoDB and Mongo Express, making database management a breeze.

# MongoDB with Mongo Express using Docker Compose

This project provides a simple setup to run a MongoDB instance along with a Mongo Express web-based MongoDB admin interface using Docker Compose.

## Project Overview

This setup consists of two services:

1. **MongoDB**: A document-oriented NoSQL database used for high-volume data storage.
2. **Mongo Express**: A web-based MongoDB admin interface written in Node.js, used to view and manage your MongoDB databases.


## Key Features

  
  **MongoDB Service:**
        The MongoDB service is configured with a root user (admin) and password (password).
        The database service is accessible via port 27017 on localhost.
        
   **Mongo Express Service:**
        Provides a UI for managing the MongoDB instance.
        Accessible via port 8081 on localhost.
        Configured to connect to the MongoDB service using the same credentials.

## Prerequisites

Before you begin, ensure you have Docker and Docker Compose installed on your machine.

## Getting Started

 **Clone the repository:**
 
First, you need to clone this repository to your local machine. Open your terminal and run:

```bash

git clone https://github.com/omar1593321/MongoDB-Docker-Setup.git

```
This command will create a directory named MongoDB-Docker-Setup and download all the project files into it.


**Navigate to the project directory:**

Move into the newly created directory to access the Docker Compose file and other resources:

```bash

cd MongoDB-Docker-Setup

```
**Start the services using Docker Compose:**

With Docker and Docker Compose installed, you can now start both the MongoDB and Mongo Express services with a single command:

```
docker-compose -f docker_compose_mongo.yaml up
```
This command will:

   - Download the required Docker images (mongo and mongo-express) if they’re not already available locally.
   - Create and start the MongoDB container, initializing it with the root username and password you specified.
   - Create and start the Mongo Express container, linking it to your MongoDB instance.
   
You’ll see logs in the terminal as Docker pulls the images and starts the services. Once you see output indicating that both services are up and running, you're ready to proceed.

## Access Mongo Express

Mongo Express provides a convenient web interface for managing your MongoDB instance. To access it: http://localhost:8081 to manage your MongoDB instance.
 
Here, you can view and manage your databases, collections, and documents. The interface will prompt you for the credentials you set up in the docker-compose.yml file (admin and pass by default).

## Verify the MongoDB Connection

**To ensure everything is working correctly:**

  Open the Mongo Express UI.
  Check that the MongoDB server is connected, and you can see the default databases (like admin, local, etc.).

You can now start creating new databases, adding collections, and inserting documents using the Mongo Express interface.  

## Customize the Setup (Optional)

If you want to customize your MongoDB setup further, such as changing the default username and password or binding to a different host port, you can modify the docker-compose.yml file. After making changes, bring the services down with docker-compose down and then restart them with docker-compose up to apply the new configuration.

## Stopping the Services


**To stop and remove the services, run:**

```bash

docker-compose down

```
This will gracefully stop both services and clean up the resources, leaving your environment ready for the next time you need it.

## Contributing

Feel free to open issues or pull requests if you have any suggestions or improvements.

## Screen Shots :
![Screenshot 2024-08-19 232719](https://github.com/user-attachments/assets/470e8549-2f87-4e7a-b3de-16b1f28a4ab3)
