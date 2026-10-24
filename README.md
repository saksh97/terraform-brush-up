# Terraform Brush-Up & AWS Infrastructure Automation

Welcome to the **terraform-brush-up** repository! This project serves as a comprehensive refresher and practical sandbox for Infrastructure as Code (IaC) deployment workflows. 

The primary implementation, configuration parameters, and visual confirmations are housed within the **`POC/`** (Proof of Concept) directory.

---

## 🚀 Proof of Concept (POC) Overview

The `POC/` folder contains a full step-by-step documentation lifecycle showing how to provision, execute, and decommission automated AWS infrastructure. 

### Core Components Housed in `POC/`
The subdirectory tracks the exact flow of building a secure infrastructure setup on an AWS EC2 platform:

*   **Host Environment Configuration:** Quick-start execution logs confirming the automated installation workflow for setting up the Terraform CLI utility on an Ubuntu Linux container.
*   **Security & Identity Access (IAM):** Visual mapping of policy attachments, including mounting IAM instance profile control roles to individual deployment servers and authorizing target EC2 infrastructure operations.
*   **Declarative Infrastructure Scripting:** A snapshot baseline reference of the primary architecture schema (`main.tf`) executing core provider setups.
*   **State & Lifecycle Management:** The complete operational timeline illustrating state backend initializations, execution plan caching, environment changes application, and clean state teardowns.

---

## 📦 Detailed Subdirectory Index

If you look inside the `POC/` directory, you will find structural screenshots mapping directly to the following execution steps:

| Section | Target File Asset | Milestone Documented |
| :--- | :--- | :--- |
| **1. Server Setup** | `install_terraform_on_ubuntu.png` | Verifying structural host configuration on Ubuntu |
| | `attaching_role_to_terraform_Server.png` | Binding the baseline security IAM execution profiles |
| | `role_to_authorize_terraform_access_EC2.png` | Mapping fine-grained target EC2 cloud access policies |
| **2. Deployment** | `main.tf.screenshot.png` | Declarative definitions layout overview |
| | `terraform_init.png` | Downscaling environment plugins during workspace boot |
| | `terraform_plan.png` | Generating dry-run change matrices before asset creation |
| | `terraform_apply.png` | Allocating real live physical infrastructure onto AWS clouds |
| **3. Clean Up** | `EC2_console.png` | Verification of successful provision status inside AWS |
| | `terraform_destroy.png` | Automated resource termination pipelines to mitigate billing |

---

## 🛠️ Global Project Tech Stack

*   **Infrastructure Engine:** Terraform (IaC)
*   **Public Cloud Provider:** Amazon Web Services (AWS)
*   **Control Node Host:** Ubuntu Linux Engine

---

## 🚦 Quick Operational Commands

To reproduce the workspace sequence documented inside the POC, navigate into your working directory and execute the foundational lifecycle suite:

```bash
# 1. Initialize local working plugin environments
terraform init

# 2. Preview infrastructure changes dry-run matrix
terraform plan

# 3. Create target objects live on cloud environments
terraform apply

# 4. Decommission and wipe clean active workspace resources
terraform destroy
```

For a comprehensive view of all workflow screenshots along with their inline descriptions, please explore the [Detailed POC Guide](./POC/README.md).
