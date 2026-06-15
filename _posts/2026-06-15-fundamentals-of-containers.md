---
layout: post
title: Fundamentals of Containers
---

Write a basic python application (main.py, requirement.txt)
write a Dockerfile that uses 'python:3.12' as base image
build the image from the dockerfile

```bash
docker build -t tutorial-img:1.0 .
```
run the container locally
docker run -i -t tutorial-img:1.0 --entrypoint

discuss entrypoint and cmd dynamics

rename the image by tagging it to remote registry storage format e.g
docker -t tutorial-img:latest <account_no>:dkr.ecr.amazon.com/aws/tutorial-img:latest

discuss why docker require password to athenticate to AWS ECR. This is a feature of
Docker as it uses basic HTTP authentication which is oassword and username. Howveer, cloud providers like aws and gcp uses IAM. As such, The valid token of a user IAM would have to be exchanged for password which is then paassed to local docker client to authenticate to remote docker registry on AWS or GCP

ECS deployment
1. Task definition: This specifies what is required to run an image as a container. The image link, memory, cpu, port, env var and secrets.
2. Task: This is a running container and would usually gets its own IP address through ENI
3. Service: This is a task manager that defines how the containers is run. How many copies is run and the launcy type specifying the infrastrcuture management
4. Cluster: This is a logical group of services used by ECS to manage services
5. ALB: It serves as the bridge between the internet and the aws services. It gets traffic from the inetrnet, send it to a target group. Any service attached to an ALB would register its tasks on the alb target group

There are two key roles
1. Task execution role which is used by ECS to start and manage containers/tasks such pulling image from ecr, writing logs to cloudwatch or pulling secrets from aws
2. Task role: This role is assumed by the application code inside the container to enable it execute its function such as 