# K8-Gaming-Project
K8-Gaming-Project

This project demonstrates how to build a Prince of Persia game environment using AWS EKS Fargate and containers. Inspired by the tutorial on [Dev.to](https://dev.to/aws-builders/create-an-aws-eks-fargate-v130-and-play-prince-of-persia--a40), this repository contains all the necessary configurations, scripts, and resources for setting up and running the game in a cloud-native Kubernetes environment.

📜 Project Overview

The K8-Gaming-Project aims to deploy a containerized version of the Prince of Persia game in an AWS EKS Fargate environment. This setup leverages the serverless nature of Fargate, allowing for automatic scaling and seamless deployment of the game with minimal management. The game environment is set up in a Kubernetes cluster with containers running the game logic, assets, and web interfaces.

This repository is based on the detailed guide available on [Dev.to](https://dev.to/aws-builders/create-an-aws-eks-fargate-v130-and-play-prince-of-persia--a40): Create an AWS EKS Fargate V1.30 and play Prince of Persia, which outlines the process of setting up the infrastructure and deploying the game on AWS using Kubernetes and Fargate.

🛠️ Tech Stack 

AWS EKS (Elastic Kubernetes Service): Kubernetes service for managing containerized applications. 

AWS Fargate: Serverless compute engine to run containers without managing servers. 

Docker: Containerization tool used to package the game and its environment. 

Kubernetes: Orchestration platform to manage the containers and scale the application. 

Helm: Kubernetes package manager to simplify deployment and configuration. 

AWS CLI: Command-line tool to interact with AWS services and manage infrastructure.

--------------------------------------------------------------------------------------------------------

Prerequisites 

AWS Account: You need an AWS account to provision and manage resources on AWS. 

AWS CLI: Install and configure the AWS CLI. 

kubectl: Kubernetes command-line tool to interact with the cluster. 

Helm: Kubernetes package manager. 

Docker: For building and running containerized applications. 