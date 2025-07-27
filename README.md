# AWS DevSecOps Pipeline with Terraform, GitHub Actions & Kubernetes Sealed Secrets

## 📌 Project Overview
This project implements a **secure and automated CI/CD pipeline** on AWS using:
- **AWS CodePipeline with Terraform**
- **DevSecOps security scanning**
- **GitHub Actions for CI/CD**
- **Kubernetes Sealed Secrets for secure secret management**

The pipeline provisions infrastructure, integrates security tools, and automates deployment.

---

## ✅ Features
- AWS CodePipeline provisioned using **Terraform**
- CI/CD workflow with **GitHub Actions**
- Security scanning:
  - `tfsec` for Terraform code
  - `Trivy` for Docker image scanning
- Secrets management using **Kubernetes Sealed Secrets**
- Deployment automation to AWS (CodeDeploy / EC2) and Kubernetes

---

## 🛠️ Tools & Technologies Used
- **Infrastructure as Code:** Terraform
- **Pipeline Service:** AWS CodePipeline
- **Build & Deploy:** AWS CodeBuild, AWS CodeDeploy, EC2
- **CI/CD Automation:** GitHub Actions
- **Security Tools:** tfsec, Trivy
- **Secrets Management:** Kubernetes Sealed Secrets
- **Cloud Platform:** AWS
- **Testing:** Terratest for infrastructure testing

---

## ✅ Tasks Implemented

### **Task 1: CodePipeline using Terraform**
- Provisioned AWS CodePipeline using Terraform.
- Pipeline includes:
  - **Source stage:** GitHub integration
  - **Build stage:** AWS CodeBuild
  - **Deploy stage:** AWS CodeDeploy / EC2
- Defined infrastructure:
  - CodePipeline, CodeBuild, CodeDeploy
  - IAM roles and policies
  - S3 bucket for artifact storage
- Wrote infrastructure tests using **Terratest**.
- Applied Terraform and confirmed pipeline setup.

### **Task 2: DevSecOps Integration**
- **GitHub Actions** workflow for CI/CD:
  - Runs on every code push.
  - Executes security scans:
    - `tfsec` for Terraform
    - `Trivy` for Docker image
  - Applies **SealedSecrets** for Kubernetes secret management.
  - Triggers deployment to Kubernetes and updates infrastructure.

---

## ⚙️ How to Run the Project
1. Clone the repository:
   ```bash
   git clone https://github.com/Purnima993/devops-pipeline.git
2. Navigate into the project:
cd devops-pipeline

3. Initialize and apply Terraform:
terraform init
terraform apply

4. Verify AWS CodePipeline setup in AWS console.

5. Push code changes to GitHub to trigger the GitHub Actions workflow.

6. Check:

   -Security scans (tfsec, Trivy)

   -Deployment using Sealed Secrets and Kubernetes.

📂 Project Structure

devops-pipeline/
│
├── terraform/               # Terraform modules for AWS resources
├── .github/workflows/       # GitHub Actions workflows
├── sealed-secrets/          # Kubernetes Sealed Secrets configurations
├── scripts/                 # Helper scripts for deployment
├── Dockerfile               # Docker image for application
└── README.md                # Project documentation

🖊️ Author
Purnima Sethi
GitHub Profile

📜 License
This project is licensed under the MIT License.
