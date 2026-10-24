# Terraform Proof of Concept (POC)

This repository serves as a **Terraform brush-up and Proof of Concept (POC)** demonstrating infrastructure deployment automation on AWS (EC2) using Terraform. It includes a complete step-by-step lifecycle flow, from server provisioning to access configuration and resource destruction.

## 🚀 Features & Step-by-Step Flow

Based on the included POC documentation assets, the workflow covers:
- **Environment Setup:** Installing Terraform on an Ubuntu environment.
- **Server Configuration:** Attaching appropriate IAM roles to the Terraform control server.
- **Access Authorization:** Configuring specific execution roles to securely authorize EC2 infrastructure access.
- **Terraform Lifecycle:** Full execution flow covering initialization, execution planning, infrastructure application, and automated cleanup.

## 🛠️ Tech Stack

- **Infrastructure as Code (IaC):** Terraform
- **Cloud Provider:** Amazon Web Services (AWS)
- **Host OS:** Ubuntu Linux

## 📦 File Structure & Assets

The `POC/` directory contains visual verification screenshots mapping out each stage of the setup:

* **`install_terraform_on_ubuntu.png`** – Installing and verifying the Terraform CLI on Ubuntu.
* **`attaching_role_to_terraform_Server.png`** – Attaching the required execution IAM role to the control instance.
* **`role_to_authorize_terraform_access_EC2.png`** – IAM configuration allowing secure management of targeted EC2 resources.
* **`main.tf.screenshot.png`** – Visual reference of the core declarative configuration file.
* **`terraform_init.png`** – Initializing the working directory and downloading cloud provider plugins.
* **`terraform_plan.png`** – Generating and inspecting the execution plan before modifying live assets.
* **`terraform_apply.png`** – Building the target architecture on AWS.
* **`EC2_console.png`** – Post-deployment validation within the AWS Management Console.
* **`terraform_destroy.png`** – Tearing down all managed infrastructure to prevent ongoing billing.

## 🚦 Usage

1. **Initialize the workspace:**
   ```bash
   terraform init
   ```

2. **Preview proposed infrastructure changes:**
   ```bash
   terraform plan
   ```

3. **Deploy the resources to AWS:**
   ```bash
   terraform apply
   ```

4. **Clean up all deployed assets:**
   ```bash
   terraform destroy
   ```
