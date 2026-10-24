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

## 📦 Walkthrough & Step-by-Step Proof

The following screenshots detail each milestone of the Proof of Concept lifecycle within this directory:

### 1. Environment & Server Setup
Before executing any infrastructure code, the deployment host is configured and authenticated.

* **Terraform Installation**
  * Verifying installation steps on an Ubuntu instance.
  * ![Install Terraform](install_terraform_on_ubuntu.png)

* **IAM Instance Profile Assignment**
  * Attaching the required execution IAM role directly to the control server host.
  * ![Attach Role to Server](attaching_role_to_terraform_Server.png)

* **Access Authorization**
  * Ensuring the configuration grants the exact execution permissions needed to modify target EC2 instances.
  * ![EC2 Access Authorization](role_to_authorize_terraform_access_EC2.png)

### 2. Configuration & Execution Workflow
The deployment phase covers script structure validation followed by standard initialization and applying the declarative configurations.

* **Main Configuration Script**
  * Reference mapping out provider configuration and structural blocks within the primary file.
  * ![Main.tf Configuration](main.tf.screenshot.png)

* **Terraform Initialization (`terraform init`)**
  * Initializing the local backend provider plugins.
  * ![Terraform Init](terraform_init.png)

* **Execution Plan (`terraform plan`)**
  * Previewing dry-run modifications before provisioning real cloud resources.
  * ![Terraform Plan](terraform_plan.png)

* **Applying Changes (`terraform apply`)**
  * Allocating live assets onto Amazon Web Services.
  * ![Terraform Apply](terraform_apply.png)

### 3. Verification & Resource Teardown
Confirming that infrastructure was safely processed, monitored, and cleanly removed at lifecycle end.

* **AWS Management Console Validation**
  * Verifying instances were initialized and run properly.
  * ![EC2 Console Verification](EC2_console.png)

* **Infrastructure Demolition (`terraform destroy`)**
  * Cleaning up and decommissioning resources to minimize structural overhead or accidental runtime fees.
  * ![Terraform Destroy](terraform_destroy.png)

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
