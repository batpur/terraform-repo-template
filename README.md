<!-- BEGIN_TF_DOCS -->
# Creating modules for AWS I&A Organization

This repo template is used to seed Terraform Module templates for the [AWS I&A GitHub organization](https://github.com/aws-ia). Usage of this template is allowed per included license. PRs to this template will be considered but are not guaranteed to be included. Consider creating an issue to discuss a feature you want to include before taking the time to create a PR.
### TL;DR

1. [install pre-commit](https://pre-commit.com/)
2. configure pre-commit: `pre-commit install`
3. install required tools
    - [tflint](https://github.com/terraform-linters/tflint)
    - [tfsec](https://aquasecurity.github.io/tfsec/v1.0.11/)
    - [terraform-docs](https://github.com/terraform-docs/terraform-docs)
    - [golang](https://go.dev/doc/install) (for macos you can use `brew`)
    - [coreutils](https://www.gnu.org/software/coreutils/)

Write code according to [I&A module standards](https://aws-ia.github.io/standards-terraform/)

## Module Documentation

**Do not manually update README.md**. `terraform-docs` is used to generate README files. For any instructions an content, please update [.header.md](./.header.md) then simply run `terraform-docs ./` or allow the `pre-commit` to do so.

## Terratest

Please include tests to validate your examples/<> root modules, at a minimum. This can be accomplished with usually only slight modifications to the [boilerplate test provided in this template](./test/examples\_basic\_test.go)

### Configure and run Terratest

1. Install

    [golang](https://go.dev/doc/install) (for macos you can use `brew`)
2. Change directory into the test folder.
    
    `cd test`
3. Initialize your test
    
    go mod init github.com/[github org]/[repository]

    `go mod init github.com/aws-ia/terraform-aws-vpc`
4. Run tidy

    `git mod tidy`
5. Install Terratest

    `go get github.com/gruntwork-io/terratest/modules/terraform`
6. Run test (You can have multiple test files).
    - Run all tests

        `go test`
    - Run a specific test with a timeout

        `go test -run examples_basic_test.go -timeout 45m`

## Module Standards

For best practices and information on developing with Terraform, see the [I&A Module Standards](https://aws-ia.github.io/standards-terraform/)

## Continuous Integration

The I&A team uses AWS CodeBuild to perform continuous integration (CI) within the organization. Our CI uses the a repo's `.pre-commit-config.yaml` file as well as some other checks. All PRs with other CI will be rejected. See our [FAQ](https://aws-ia.github.io/standards-terraform/faq/#are-modules-protected-by-ci-automation) for more details.

## Requirements

| Name | Version |
|------|---------|
| <a name="requirement_terraform"></a> [terraform](#requirement\_terraform) | >= 0.14.0 |
| <a name="requirement_aws"></a> [aws](#requirement\_aws) | >= 3.72.0 |
| <a name="requirement_awscc"></a> [awscc](#requirement\_awscc) | >= 0.21.0 |

## Providers

No providers.

## Modules

No modules.

## Resources

No resources.

## Inputs

No inputs.

## Outputs

No outputs.
<!-- END_TF_DOCS -->
