# Terraform AWS IAM Role for GitHub Actions

This repository provides a Terraform module to create an IAM role with the necessary permissions and trust policies for GitHub Actions to manage AWS Organizations resources.

## Usage

### Module

```hcl
module "github_actions_iam_role" {
  source = "github.com/infraspecdev/terraform-aws-github-actions-iam-role?ref=main"

  aws_account_id   = "YOUR_AWS_ACCOUNT_ID"
  github_username  = "YOUR_GITHUB_USERNAME"
  repository_names = "YOUR_REPO_NAMES"
  role_name        = "GitHubActionsRole"
}
```

## Variables

- **aws_account_id**: The AWS Account ID where the IAM role will be created.
- **github_username**: The GitHub username or organization name.
- **repository_names**: The list of GitHub repository names.
- **role_name**: (Optional) The name of the IAM role. Default is `GitHubActionsRole`.

## Outputs

- **role_arn**: The ARN of the IAM role.
