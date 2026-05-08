# 🚀 End-to-End DevOps CI/CD Pipeline with Automated AWS EC2 Deployment

## 📌 Project Overview

This project demonstrates a complete DevOps workflow for deploying a containerized Python Flask application using modern DevOps tools and CI/CD practices.

The application is containerized using Docker, integrated with GitHub Actions for Continuous Integration and Continuous Deployment (CI/CD), pushed to Docker Hub, and automatically deployed to an AWS EC2 instance whenever new code is pushed to the GitHub repository.

This project helped me gain hands-on experience with real-world DevOps workflows, deployment automation, Docker image management, GitHub Actions pipelines, AWS infrastructure, and troubleshooting production-like issues.

----------------------------------------------------------------------------------------------------------------------------------

# 🏗️ Architecture

Developer → GitHub → GitHub Actions → Docker Hub → AWS EC2

----------------------------------------------------------------------------------------------------------------------------------

# 🛠️ Technologies Used

| Technology         | Purpose                      |
| ------------------ | ---------------------------- |
| 🐳 Docker          | Containerization             |
| ☁️ AWS EC2         | Application Hosting          |
| 🔄 GitHub Actions  | CI/CD Automation             |
| 📦 Docker Hub      | Docker Image Registry        |
| 🧑‍💻 Git & GitHub    | Version Control              |
| 🐍 Python Flask    | Sample Web Application       |
| 🔐 GitHub Secrets  | Secure Credential Management |
| 🐧 Linux           | Server Environment           |

----------------------------------------------------------------------------------------------------------------------------------

# 🔄 CI/CD Workflow

The project follows a fully automated CI/CD workflow:

✅ Developer pushes code to GitHub
✅ GitHub Actions workflow triggers automatically
✅ Docker image is built automatically
✅ Docker image is pushed to Docker Hub
✅ GitHub Actions connects to AWS EC2 through SSH
✅ Latest Docker image is pulled automatically
✅ Existing running container is stopped and removed
✅ Updated application container is deployed automatically on EC2

----------------------------------------------------------------------------------------------------------------------------------

# ☁️ AWS EC2 Automated Deployment

The application is hosted on an Ubuntu EC2 instance using Docker containers.

Deployment automation was achieved by integrating GitHub Actions with AWS EC2 using SSH-based deployment.

The deployment workflow includes:

* Docker installation and configuration on EC2
* Secure SSH authentication using GitHub Secrets
* Automated image pull from Docker Hub
* Automatic container restart during deployment
* Exposing application on port 80

The application gets updated automatically whenever new code is pushed to the repository.

----------------------------------------------------------------------------------------------------------------------------------

# 🔐 GitHub Secrets Used

| Secret Name     | Description                    |
| --------------- | ------------------------------ |
| DOCKER_USERNAME | Docker Hub Username            |
| DOCKER_PASSWORD | Docker Hub Access Token        |
| EC2_HOST        | AWS EC2 Public IP              |
| EC2_USERNAME    | EC2 Instance Username          |
| EC2_SSH_KEY     | Private SSH Key for Deployment |

----------------------------------------------------------------------------------------------------------------------------------

# ❗ Challenges Faced & Solutions

During this project, multiple real-world DevOps issues were encountered and resolved.

----------------------------------------------------------------------------------------------------------------------------------

 ❌ Missing requirements.txt File

 🔴 Error
    Could not open requirements file

 ✅ Solution

  * Created requirements.txt file
  * Added required Flask dependency

----------------------------------------------------------------------------------------------------------------------------------

 ❌ Docker Image Push Failed

 🔴 Error
  tag does not exist


 ✅ Solution

 * Tagged Docker image correctly before pushing to Docker Hub

----------------------------------------------------------------------------------------------------------------------------------

 ❌ Docker Hub Access Token Permission Error

 🔴 Error
  unauthorized: access token has insufficient scopes

 ✅ Solution

 * Created a new Docker Hub Access Token
 * Enabled proper push permissions

---------------------------------------------------------------------------------------------------------------------------------

 ❌ Port Already Allocated on EC2

 🔴 Error
  Bind for 0.0.0.0:80 failed: port is already allocated

 ✅ Solution

 * Stopped and removed old running container
 * Re-deployed updated container successfully

----------------------------------------------------------------------------------------------------------------------------------

 ❌ GitHub Actions SSH Deployment Issue

 🔴 Issue
  GitHub Actions could not connect to the EC2 instance during deployment.

 ✅ Solution

 * Generated SSH key pair
 * Added public SSH key to EC2 authorized_keys
 * Stored private SSH key securely in GitHub Secrets

----------------------------------------------------------------------------------------------------------------------------------

 # 🎯 Key Learnings

✅ Docker containerization
✅ Automated CI/CD pipeline implementation
✅ Docker Hub image management
✅ AWS EC2 deployment automation
✅ SSH-based automated deployment
✅ GitHub Actions workflow creation and management
✅ Secure secrets management
✅ Linux & Docker troubleshooting
✅ Real-world DevOps debugging experience

----------------------------------------------------------------------------------------------------------------------------------

# 🚀 Future Improvements

 🔹 Infrastructure provisioning using Terraform
 🔹 Kubernetes deployment using EKS
 🔹 Monitoring using Prometheus & Grafana

----------------------------------------------------------------------------------------------------------------------------------

# 👨‍💻 Author

# Affan Patel

Aspiring DevOps & Cloud Engineer 🚀

----------------------------------------------------------------------------------------------------------------------------------

⭐ Conclusion

This project provided hands-on experience with the complete DevOps lifecycle, including containerization, CI/CD automation, Docker image management, AWS EC2 deployment, and deployment automation using GitHub Actions.

It also helped in understanding and solving real-world DevOps and deployment-related issues commonly faced in production environments.


