# Terraform – Broken Code Exercise (Fix & Learn)

This repository contains **intentionally broken Terraform code** for an ECS + ALB setup in AWS.

Your task (or the learner’s task) is simple:

> **Try to run the code, see what breaks, fix it, and understand why.**

This helps beginners learn Terraform by debugging real mistakes.

## 🔧 What this code is supposed to create

- A VPC with public subnets
- An ECS Cluster running an Nginx container
- An Application Load Balancer (ALB) in front of ECS
- Optional RDS database (for practice)

## ❌ What’s wrong with the current code?

A few examples:

- Resource names use **hyphens**, which Terraform does not allow
- Variables are mismatched or unused
- ECS task definition is incomplete
- ALB references the wrong resources
- Outputs point to resources that don’t exist

There are **syntax errors**, **reference errors**, and **design issues**.  
Your job is to fix them.

## ✔️ What to do

1. Clone the repo  
2. Run:
```
terraform init
terraform validate
```
You will see errors. Fix them one by one.

3. Once validation works:
```
terraform plan
terraform apply
```

4. Test the ALB by visiting its DNS name.

5. Clean up:
```
terraform destroy
```

## 🎯 Learning goals

By fixing this code, you will learn:

- Correct Terraform resource naming
- How variables and outputs work
- ECS + ALB integration
- How to troubleshoot Terraform errors
- How AWS networking pieces connect together

## 📌 Assumptions you may need to make

- AWS region
- ECS launch type (**Fargate** or **EC2**)
- Whether RDS should be enabled
- Naming conventions

There is no single “correct” solution — the goal is learning.

## 🙌 Want to contribute?

Feel free to:

- Improve the code
- Add modules
- Add security best practices
- Add diagrams or comments
