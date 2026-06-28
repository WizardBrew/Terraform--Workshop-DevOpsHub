
## 🧭 Key Discussion Points

- link: https://wizardbrew.github.io/Terraform--Workshop-DevOpsHub/
### 1. 🌍 Terraform Introduction
- Overview of Terraform and its role in Infrastructure as Code (IaC)

### 2. 🧾 HashiCorp Configuration Language (HCL)
- Syntax and structure of HCL
- Declarative approach to infrastructure

### 3. 🛠️ Installation & Setup
- Download and install Terraform using binary  
  🔗 [Terraform 1.13.1 Windows Binary](#)
- Verify installation and environment setup

### 4. ⚖️ Benefits & Cons of Terraform
- Pros: Scalability, modularity, multi-cloud support  
- Cons: Learning curve, state file management

### 5. 🧑‍💻 AWS CLI Integration
- Installing AWS CLI on local machine  
  🔗 [AWS CLI Installation Guide](#)
- Configuring CLI for Terraform use

### 6. 🧠 Understanding IaC
- What is Infrastructure as Code?
- Why IaC matters for DevOps and cloud automation

### 7. 🔗 Terraform ↔ AWS Connectivity
- How Terraform authenticates and provisions AWS resources
- Provider configuration and backend setup

### 8. 🧪 Practical Demo: AWS + Terraform
- Created IAM user and group for Terraform
- Attached policy for programmatic access
- Generated access keys for authentication
- Configured AWS CLI with credentials ▸ Used AMI image and named it Devmachine
- Validated Terraform configuration ▸ Used terraform validate to check syntax and logical consistency ▸ Optional: used JSON output for CI/CD integration

---

## ✅ Action Items

- [ ] Share Terraform setup scripts
- [ ] Document IAM policy attachment steps
- [ ] Publish AWS CLI + Terraform integration guide
- [ ] Record demo walkthrough for team reference

---

## 🚀 Workflow Commands

| **Command** | **Explanation** |
|-------------|-----------------|
| `terraform init` | Initializes working directory, downloads providers/modules. Run first in any new project. |
| `terraform plan` | Previews changes without applying. Safe way to check infra updates. |
| `terraform plan -out=plan.tfplan` | Saves plan to file for later apply. |
| `terraform apply` | Applies changes interactively. |
| `terraform apply -auto-approve` | Applies without confirmation (CI/CD use). |
| `terraform destroy` | Destroys all managed infra. Use carefully. |
| `terraform destroy -target=aws_instance.web` | Destroys only a specific resource. |

----
## 🛠 Validation & Formatting

| **Command** | **Explanation** |
|-------------|-----------------|
| `terraform validate` | Checks `.tf` files for syntax/config errors. |
| `terraform fmt` | Formats `.tf` files into canonical HCL style. |
| `terraform fmt -check` | Checks formatting only (CI-friendly). |
| `terraform fmt -recursive` | Formats files in subdirectories too. |

---
## 📦 State Management

| **Command** | **Explanation** |
|-------------|-----------------|
| `terraform state list` | Lists all resources tracked in state. |
| `terraform state show <resource>` | Shows attributes of a resource. |
| `terraform state mv <src> <dst>` | Moves/renames resource in state. |
| `terraform state rm <resource>` | Removes resource from state (infra stays). |
| `terraform state pull` | Downloads remote state as JSON. |
| `terraform state push <file>` | Uploads local state file to backend. |
| `terraform import <resource> <id>` | Imports existing infra into state. |
| `terraform force-unlock <lock-id>` | Releases a stuck state lock. |

---
## 🌍 Workspaces

| **Command** | **Explanation** |
|-------------|-----------------|
| `terraform workspace list` | Lists all workspaces (dev, staging, prod). |
| `terraform workspace show` | Shows current workspace. |
| `terraform workspace new <name>` | Creates new workspace for environment separation. |
| `terraform workspace select <name>` | Switches workspace. |
| `terraform workspace delete <name>` | Deletes a workspace (not current). |

---
## 🔍 Inspection & Debugging

| **Command** | **Explanation** |
|-------------|-----------------|
| `terraform show` | Displays current state or saved plan. |
| `terraform show plan.tfplan` | Shows saved plan file. |
| `terraform output` | Lists all output values. |
| `terraform output -json` | Outputs values as JSON. |
| `terraform graph | dot -Tpng > graph.png` | Generates dependency graph. |
| `terraform providers` | Lists required providers. |
| `terraform version` | Shows installed version. |

---
## ⚠️ Best Practices

- Always run `terraform plan` before `apply`.  
- Use **workspaces** for environment separation.  
- Keep **state files secure** (they contain secrets).  
- Use **remote backends** (S3, Azure Blob, GCS) for collaboration.  
- Apply `terraform fmt` & `terraform validate` in CI/CD pipelines.  

---




## 📎 Resources

- [Terraform Docs](https://developer.hashicorp.com/terraform/docs)
- [AWS CLI Docs](https://docs.aws.amazon.com/cli/latest/userguide/)
- [Infrastructure as Code Overview](https://learn.hashicorp.com/tutorials/terraform/infrastructure-as
