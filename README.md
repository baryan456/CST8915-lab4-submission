# CST8915 Lab 4 – Introduction to Docker

**Student Name:** Aryan Banoth  
**Student Number:** 041293006  
**Course:** CST8915 – Full-Stack Cloud-Native Development  
**Lab:** Lab 4

## 1. Lab Overview

The objective of this lab was to understand Docker fundamentals, build and run containerized applications, explore Docker image layers, and use Docker Compose to manage a multi-container application.

During this lab, I worked with Docker on an Ubuntu virtual machine hosted in Microsoft Azure. I practised running containers, building a custom Docker image, examining image layers, and configuring a Flask web application with Redis.

## 2. Demo Video

[**YouTube Demo Link**](https://youtu.be/O4yPyYYvWOA)

## 3. Tasks Completed

### Docker Installation

I created an Ubuntu virtual machine in Azure and installed Docker Engine. I verified the installation by checking Docker information and running the Hello World container.

### Docker Fundamentals

I learned the fundamentals of Docker images and containers. I ran an NGINX container, checked its status, and tested the web server using a browser.

### Creating a Docker Image

I created a Flask application and wrote a Dockerfile to define its environment. I built a Docker image and ran the application inside a container.

### Docker Image Layers

I explored Docker image layers using commands such as `docker history` and `docker inspect`. I also examined how Docker layer caching helps make image builds more efficient.

### Container Writable Layers

I ran multiple containers from the same Docker image and explored their writable layers. I learned how Docker allows each container to maintain its own changes without automatically affecting other containers.

### Docker Compose

I used Docker Compose to define and run a Flask web application and a Redis service together. I verified the running services and tested the Flask application using `curl`. The application returned a page-view counter that increased with successive requests.

## 3. Reflection Questions

### Question 1: What is the difference between a Docker image and a Docker container?

A Docker image is a template that contains the application code, dependencies, and instructions required to run an application. A Docker container is a running or stopped instance of an image. Images can be used to create multiple containers, allowing applications to run consistently across different environments.

### Question 2: How does Docker's layered architecture improve efficiency?

Docker images are built from layers, with each layer representing filesystem changes introduced by an instruction in the Dockerfile. Docker can reuse unchanged layers through its build cache instead of rebuilding everything each time. This reduces build time and avoids unnecessary duplication of image data.

### Question 3: Why does each container have its own writable layer?

Each container has its own writable layer so that changes made while the container is running remain separate from the original image and from other containers. Multiple containers can share the same underlying image layers while maintaining their own files and modifications. This improves isolation and allows containers to operate independently.

### Question 4: What are the benefits of Docker Compose compared with running containers individually?

Docker Compose allows multiple related services to be defined in a single YAML configuration file. It simplifies container startup, networking, environment configuration, and service dependencies. Instead of managing each container with separate commands, I can use commands such as `docker compose up` and `docker compose down` to manage the application as a group.

## 4. Challenges and Lessons Learned

During this lab, I learned how to install Docker, build images, run containers, and explore Docker image and writable layers. I also gained practical experience using Docker Compose to run a Flask web application alongside Redis. Testing the application helped me understand how multiple services communicate within a containerized environment.

## 5. Conclusion

This lab helped me develop a practical understanding of Docker, including image creation, container execution, image layers, writable layers, and Docker Compose. I also learned how to run multiple services together and verify communication between them. These concepts provide a foundation for building and managing containerized cloud-native applications.