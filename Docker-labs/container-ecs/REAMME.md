# Cloud-Native Web Application: Dockerized & Deployed on AWS ECS (Fargate)

A hands-on implementation demonstrating the containerization of a lightweight web server and its deployment to a highly available, serverless infrastructure on AWS using Amazon ECR and ECS (Fargate).

## 🏗️ Architecture Overview

The deployment pipeline and runtime architecture follow standard cloud-native best practices:

1. **Local Containerization:** Built a lightweight Nginx container hosting a custom static application.
2. **Secure Authentication:** Utilized IAM user policies (`AmazonEC2ContainerRegistryPowerUser`) to securely authenticate the local Docker daemon with the AWS cloud environment.
3. **Artifact Registry:** Tagged and pushed the immutable container image to a private **Amazon ECR** repository.
4. **Serverless Orchestration:** Defined an **ECS Task Definition** utilizing the `awsvpc` network mode, enabling dedicated ENIs for fine-grained security group control.
5. **Runtime Infrastructure:** Deployed the application via an **ECS Service** onto an **Amazon ECS Cluster** backed by serverless **AWS Fargate** compute engines.

---

## 🛠️ Tech Stack & Tools Used
* **Containerization:** Docker / Dockerfile
* **Base Web Server:** Nginx (Alpine Linux flavor)
* **Cloud Platform:** Amazon Web Services (AWS)
* **AWS Services:** ECR (Elastic Container Registry), ECS (Elastic Container Service), Fargate, IAM

---