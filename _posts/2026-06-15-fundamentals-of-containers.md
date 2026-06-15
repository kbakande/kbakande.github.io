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
