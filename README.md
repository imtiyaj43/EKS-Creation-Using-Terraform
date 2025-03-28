# EKS Creation Using Terraform

This repository provides Terraform scripts to deploy an Amazon EKS (Elastic Kubernetes Service) cluster on AWS. It automates the setup of the EKS cluster, worker nodes, and necessary networking components.

## Prerequisites

Before using this repository, ensure you have the following:

- Terraform installed ([Install Terraform](https://developer.hashicorp.com/terraform/tutorials/aws-get-started/install-cli))
- AWS CLI installed and configured ([Install AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html))
- kubectl installed ([Install kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/))
- AWS IAM permissions to create EKS clusters and related resources
- Steps are mention in the Steps to follow file
## Usage

1. Clone the Repository:
   ```
   git clone https://github.com/imtiyaj43/EKS-Creation-Using-Terraform.git
   cd EKS-Creation-Using-Terraform
   ```

2. Initialize Terraform:
   ```
   terraform init
   ```

3. Plan the Deployment:
   ```
   terraform plan
   ```
   This will show you the resources that Terraform will create.

4. Apply the Configuration:
   ```
   terraform apply -auto-approve
   ```
   This command will create the EKS cluster and related resources.

5. Configure kubectl:
   ```
   aws eks update-kubeconfig --region <your-region> --name <your-cluster-name>
   ```
   Replace `<your-region>` and `<your-cluster-name>` with appropriate values.

6. Verify the Cluster:
   ```
   kubectl get nodes
   ```
   If successful, this command will display the worker nodes in the cluster.

## Destroying the Infrastructure

To delete the EKS cluster and all associated resources, run:
   ```
   terraform destroy -auto-approve
   ```

## Notes

- Ensure your AWS credentials are properly set up before running Terraform.
- Modify `variables.tf` to customize the cluster settings.
- This setup follows AWS best practices for deploying an EKS cluster using Terraform.

## Contribution

Feel free to submit issues or contribute by creating a pull request.


