# 🚀 Terraform AWS Infrastructure – VPC, Subnet & EC2 (IaC Project)

This project demonstrates **Infrastructure as Code (IaC)** using **Terraform** to provision AWS resources automatically instead of manually creating them from the console.

---

## 📌 **Project Objective**

Deploy AWS infrastructure using Terraform, including:

- Custom VPC
- Subnet (Public)
- Internet Gateway
- Route Table & Association
- Security Group
- EC2 Instance (Free Tier Eligible)

This follows IaC principles for consistent, automated, and version-controlled cloud provisioning.

---

## 🧩 **Tech Stack**

| Component     | Technology  |
|--------------|-------------|
| IaC Tool     | Terraform   |
| Cloud        | AWS (Free Tier) |
| Language     | HCL (HashiCorp Configuration Language) |
| OS Tested On | Windows     |

---

## 🏗 **Terraform Configuration Structure**

```
.
├── main.tf         # Contains provider + all AWS resources
├── outputs.tf      # Prints useful resource values (e.g., EC2 Public IP)
└── screenshots/    # CLI & AWS console results (optional)
```

---

## 📂 **What `main.tf` Contains**

Resources defined:

✔ Provider block  
✔ VPC  
✔ Subnet (Public)  
✔ Internet Gateway  
✔ Route Table & Association  
✔ Security Group  
✔ EC2 Instance  

---

## 📤 **Outputs**

`outputs.tf` exposes important deployment results such as:

- EC2 Public IP (for SSH / testing)

---

## 🛠 **Terraform Commands Used**

```bash
terraform init      # Download providers & initialize
terraform plan      # Preview changes before deployment
terraform apply     # Provision AWS resources
terraform destroy   # Delete all created resources
```

---

## 🌐 **Deployed Architecture Diagram (Conceptual)**

```
                 Internet
                     |
             ┌────────────────┐
             |  Internet GW   |
             └────────────────┘
                     |
             ┌────────────────┐
             |  Route Table   |
             └────────────────┘
                     |
             ┌────────────────────────┐
             | Public Subnet (EC2)     |
             └────────────────────────┘
                     |
             ┌────────────────────────┐
             |     VPC (10.0.0.0/16)   |
             └────────────────────────┘
```

---

## 📸 **Screenshots**

Screenshots available under `/screenshots/` folder:

✔ `terraform init`  
✔ `terraform plan`  
✔ `terraform apply`  
✔ EC2 instance in AWS console  
✔ VPC networking components  

---

## 🎥 **Demo Video**

Execution Demo (Google Drive Link):

👉 https://drive.google.com/file/d/1KhuEjRiv1D12StbXuSnZINybXdOX9MXv/view?usp=drive_link

---

## ⚙️ **How to Run This Project**

### **Prerequisites**
- AWS Account (Free Tier)
- Terraform installed
- AWS CLI configured via:
  ```
  aws configure
  ```
  or environment variables.

### **Run Deployment**
```bash
terraform init
terraform apply
```

### **Destroy to avoid costs**
```bash
terraform destroy
```

---

## 🧹 **Cost & Cleanup Notice**

Although this is Free Tier compatible, always destroy infrastructure after testing:

```bash
terraform destroy
```

---

## 🎯 **Key Learnings**

Through this project I learned:

✔ Terraform resource provisioning on AWS  
✔ Infrastructure as Code workflows  
✔ Dependency graph & state handling  
✔ Reproducible & automated deployments  
✔ AWS networking fundamentals (VPC, Subnets, IGW)  

---

## 📌 **Future Enhancements**

Planned improvements:

- Add private subnet + NAT Gateway
- Add RDS or DynamoDB
- Apply remote backend for state storage (S3 + DynamoDB)
- Add CI/CD automation (GitHub Actions)

---

## 👤 **Author**

**Name:** _Gayathri N._

If you found this helpful, feel free to ⭐ the repo!
