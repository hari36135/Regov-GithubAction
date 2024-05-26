# Regov-GithubAction

Greetings Team,

I'm pleased to share that as per the task requirements, I've implemented a four-stage pipeline comprising QA (code quality check), dev, UAT, and prod environments. This pipeline facilitates the deployment of AWS resources across multiple environments with manual approval steps. The process involves deploying IAM roles via Terraform. Initially, SonarQube conducts code quality checks, providing insights into code smells, accessible via the SonarQube console. Subsequently, upon completion of the code quality check, the remaining stages are deployed following the necessary approvals.

Please note: The installation of SonarQube is not included in this repository. I have configured SonarQube separately and obtained the required credentials.

Tools/Technologies Utilized:

1. GitHub Re-usable Workflows
2. Terraform
3. Terraform Workspaces
4. SonarQube
5. GitHub Environments, Secrets


    ## Directory Structure
    ```shell
    Regov-GithubAction
    ├── .github
    │   └── workflows
    │       ├── aws_tf_appy.yml
    │       ├── pipeline.yml
    │       └── sonar-project.properties
    ├── IAMRoles
    │   ├── dev.tfvars
    │   ├── IAM.tf
    │   ├── Main.tf
    │   ├── prod.tfvars
    │   ├── uat.tfvars
    │   └── variables.tf
    ├── README.md
    ├── S3Bucket
    │   ├── dev.tfvars
    │   ├── Main.tf
    │   ├── prod.tfvars
    │   ├── S3Bucket.tf
    │   ├── uat.tfvars
    │   └── variables.tf
    └── sonar-project.properties
