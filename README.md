# Trading Bot

This project is a trading bot that learns and trades based on the analysis of historical data, market patterns and relevant news. The application is made up of two parts:

- **Backend:** Developed in Java (Java 21) with Spring Boot, in charge of business logic, data access (MySQL) and scheduled tasks.
- **Frontend:** Web application in ReactJS using Vite and Tailwind CSS, which provides the user interface.

Additionally, the entire environment is deployed using Docker and Docker Compose, making it easy to get up and running in any environment.

---

## Table of Contents

- [Technologies Used](#technologies-used)
- [Project Structure](#project-structure)
- [Prerequisites](#prerequisites)
- [Environment Settings](#environment-settings)
- [Local Deployment](#local-deployment)
- [Additional Notes](#additional-notes)
- [Contributions](#contributions)
- [License](#license)---


## Technologies Used

- **Backend:**  
  - Java 21  
  -SpringBoot  
  -Maven  
  - Spring Data JPA (for persistence with MySQL)  
  - Spring Boot Actuator (monitoring)  
  - Spring Scheduling (periodic tasks)



- **Frontend:**  
  - ReactJS  
  - Vite  
  - Tailwind CSS

- **Database:**  
  - MySQL

- **DevOps:**  
  - Docker  
  - Docker Compose

---


## Project Structure

The main structure of the repository is as follows:


```
root/
├── backend/ # Backend source code (Spring Boot)
│ ├── src/ # Java code and resources
│ ├── pom.xml # Maven configuration file
│ └── Dockerfile # Dockerfile to build and run the backend
├── frontend/ # Frontend source code (React, Vite, Tailwind)
│ ├── src/ # JavaScript/JSX code
│ ├── package.json # Node.js project configuration
│ └── Dockerfile # Dockerfile to build and run the frontend
├── docker-compose.yml # Container orchestrator (backend, frontend and MySQL)
├── .env # Environment variables file (credentials, URLs, etc.)
└── .gitignore # Ex
```

---

## Prerequisites

Before deploying the project, make sure you have installed on your machine:

- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)
- Git (to clone the repository)

---

## Environment Configuration

1. **`.env` file:**  
   In the project root, create (or edit) the `.env` file to define the environment variables to be used in both Docker Compose and Spring Boot configuration. For example:

   ```dotenv
   # MySQL Credentials and Configuration
   MYSQL_ROOT_PASSWORD=rootpassword
   MYSQL_DATABASE=tradingdb
   MYSQL_USER=user
   MYSQL_PASSWORD=userpassword

   # Configuration for Spring Boot (backend)
   SPRING_DATASOURCE_URL=jdbc:mysql://mysql:3306/tradingdb
   SPRING_DATASOURCE_USERNAME=user
   SPRING_DATASOURCE_PASSWORD=userpassword
