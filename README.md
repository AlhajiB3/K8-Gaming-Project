# K8-Gaming-Project
K8-Gaming-Project
This project demonstrates how to build a Prince of Persia game environment using AWS EKS Fargate and containers. Inspired by the tutorial on Dev.to, this repository contains all the necessary configurations, scripts, and resources for setting up and running the game in a cloud-native Kubernetes environment.

📝 Table of Contents
Project Overview
Tech Stack
Getting Started
How to Run the Game
Deployment
Folder Structure
Contributing
License
📜 Project Overview
The K8-Gaming-Project aims to deploy a containerized version of the Prince of Persia game in an AWS EKS Fargate environment. This setup leverages the serverless nature of Fargate, allowing for automatic scaling and seamless deployment of the game with minimal management. The game environment is set up in a Kubernetes cluster with containers running the game logic, assets, and web interfaces.

This repository is based on the detailed guide available on Dev.to: Create an AWS EKS Fargate V1.30 and play Prince of Persia, which outlines the process of setting up the infrastructure and deploying the game on AWS using Kubernetes and Fargate.

🛠️ Tech Stack
AWS EKS (Elastic Kubernetes Service): Kubernetes service for managing containerized applications.
AWS Fargate: Serverless compute engine to run containers without managing servers.
Docker: Containerization tool used to package the game and its environment.
Kubernetes: Orchestration platform to manage the containers and scale the application.
Helm: Kubernetes package manager to simplify deployment and configuration.
AWS CLI: Command-line tool to interact with AWS services and manage infrastructure.
Terraform: Infrastructure as code tool used for provisioning AWS resources.
🚀 Getting Started
To get started with this project, follow these steps to set up your local environment and deploy the application on AWS.

Prerequisites
AWS Account: You need an AWS account to provision and manage resources on AWS.
AWS CLI: Install and configure the AWS CLI.
kubectl: Kubernetes command-line tool to interact with the cluster.
Helm: Kubernetes package manager.
Docker: For building and running containerized applications.
Terraform: To manage and provision AWS resources.
Install Prerequisites
Install the AWS CLI:

bash
Copy
Edit
pip install awscli
Install kubectl (Kubernetes command-line tool):

macOS: brew install kubectl
Windows: Use the Kubernetes official documentation for installation.
Install Helm:

bash
Copy
Edit
brew install helm
Install Docker: You can download it from Docker's official website.

Install Terraform: You can follow the instructions on the Terraform website.

🎮 How to Run the Game
Follow these steps to deploy and play Prince of Persia on AWS using the resources from this repository:

Clone the repository:

bash
Copy
Edit
git clone https://github.com/your-username/K8-Gaming-Project.git
cd K8-Gaming-Project
Configure AWS CLI:

bash
Copy
Edit
aws configure
Set up the EKS cluster using Terraform:

Make sure to change the AWS region in terraform.tfvars if needed.
Run the following commands:
bash
Copy
Edit
terraform init
terraform apply
Deploy with Helm: Use Helm to deploy the necessary Kubernetes resources for your game.

bash
Copy
Edit
helm install prince-of-persia ./helm/prince-of-persia
Verify the deployment: Check if the pods and services are running successfully:

bash
Copy
Edit
kubectl get pods
kubectl get svc
Access the game: After deployment, you should be able to access the game through a LoadBalancer service exposed via AWS EKS. You’ll get the URL to play the game.

🌐 Deployment
This project uses AWS EKS to run containers in a serverless environment. The deployment is fully managed and uses Fargate to scale automatically based on usage. The infrastructure is provisioned using Terraform and deployed using Helm for Kubernetes resources.

Terraform provisions the infrastructure, including the EKS cluster, networking, and security.
Helm is used to deploy and manage the game within the Kubernetes cluster.
🗂️ Folder Structure
Here’s a breakdown of the important folders and files in this project:

bash
Copy
Edit
/K8-Gaming-Project
│
├── /helm/                        # Helm charts for Kubernetes deployment
│   └── prince-of-persia/         # Helm chart for the Prince of Persia game
├── /terraform/                   # Terraform configuration files
│   └── main.tf                   # Terraform AWS EKS setup
├── /docker/                      # Dockerfiles for building game containers
│   └── Dockerfile                # Dockerfile for Prince of Persia game
└── README.md                     # Project README
👩‍💻 Contributing
Contributions to this project are welcome! If you'd like to improve the project, fix bugs, or add features, feel free to submit a pull request.

Steps to contribute:
Fork the repository.
Create a new branch.
Make your changes.
Open a pull request for review.
📝 License
This project is licensed under the MIT License - see the LICENSE file for details.