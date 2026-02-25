# AWS S3 Backup Cost Optimization using Terraform + Python

## 📌 Project Overview

This project automates secure backup of local files to AWS S3 and implements cost optimization using lifecycle policies.

The infrastructure is provisioned using Terraform (Infrastructure as Code), and backups are uploaded using a Python automation script (boto3).

Older backup files are automatically transitioned to Amazon S3 Glacier to reduce long-term storage costs.

---

## 🛠️ Tech Stack

- AWS S3
- AWS Glacier
- Terraform
- Python (boto3)
- AWS CLI

---

## 🏗️ Architecture Flow

Local Files  
   ↓  
Python Backup Script  
   ↓  
AWS S3 Bucket  
   ↓  
Lifecycle Policy  
   ↓  
Glacier Storage (Cost Optimized)

---

## 📂 Project Structure

AWS-S3-Backup-Cost-Optimization/
│
├── Terraform/
│   ├── main.tf
│   ├── variables.tf
│   ├── outputs.tf
│   └── terraform.tfvars
│
├── AutoBackupScript.py
└── README.md

---

# 🚀 How to Run This Project

## Step 1: Clone Repository

git clone https://github.com/SayaliKokane5/AWS-S3-Backup-Cost-Optimization.git
cd AWS-S3-Backup-Cost-Optimization

---

## Step 2: Configure AWS CLI

aws configure

Provide:
- AWS Access Key
- AWS Secret Key
- Default region (example: us-east-1)
- Output format (json)

---

## Step 3: Setup Infrastructure Using Terraform

Navigate to Terraform folder:

cd Terraform

Initialize Terraform:

terraform init

Check execution plan:

terraform plan

Apply configuration:

terraform apply -auto-approve

This will create:
- S3 bucket
- Lifecycle rule to move objects to Glacier
- Required IAM configuration

---

## Step 4: Install Python Dependency

pip install boto3

---

## Step 5: Run Backup Script

Go back to project root folder:

cd ..
python AutoBackupScript.py

The script will:
- Compress local files
- Add timestamp
- Upload backup to S3 bucket
- Store backup in defined storage class

---

# 💰 Cost Optimization Strategy

S3 lifecycle rule automatically transitions:

Standard Storage → Glacier (after defined number of days)

This significantly reduces storage cost for old backups.

---

# 🔐 Security Best Practices

- IAM-based access control
- Infrastructure as Code (Terraform)
- Automated backup process
- Version-controlled configuration

---

# 🧹 Destroy Infrastructure (Optional)

cd Terraform
terraform destroy -auto-approve

---

# 📈 Resume Highlights

- Designed automated AWS S3 backup system using Terraform & Python
- Implemented lifecycle policies to reduce storage cost
- Built Infrastructure as Code (IaC) for repeatable cloud deployments
- Automated backup uploads using boto3

---

## 👩‍💻 Author

Sayali Kokane  
DevOps Engineer | AWS | Terraform | Automation
