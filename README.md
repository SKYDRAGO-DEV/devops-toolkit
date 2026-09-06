# devops-toolkit

> **Legacy / superseded repository**

A small historical infrastructure-and-CI reference containing an AWS Terraform example and an older CI/CD workflow experiment.

For the actively maintained infrastructure foundation on this profile, see [`cloud-infra`](https://github.com/SKYDRAGO-DEV/cloud-infra).

## Why this repository remains public

This repository preserves earlier infrastructure work and commit history, but it is **not a flagship project** and should not be interpreted as a production-ready DevOps platform.

The current implementation contains:

- `terraform/aws-infra/main.tf` — an AWS VPC/subnet Terraform example
- `.github/workflows/ci.yml` — static Terraform validation

The previous README described GCP infrastructure, Kubernetes templates, monitoring stacks, and production-grade deployment capabilities that are not present in the repository. Those claims have been removed.

## Validation

CI performs static Terraform quality checks without applying infrastructure:

```text
terraform fmt -check
      ↓
terraform init -backend=false
      ↓
terraform validate
```

No cloud credentials are required for these checks.

## Repository layout

```text
devops-toolkit/
├── terraform/
│   └── aws-infra/
│       └── main.tf
├── .github/
│   └── workflows/
│       └── ci.yml
└── README.md
```

## Security and scope

- No cloud credentials should be committed.
- Terraform state may contain sensitive values and should be protected outside source control.
- The configured backend identifiers are examples tied to the original environment and should be changed before reuse.
- This repository does not claim active production deployment, monitoring, Kubernetes, container publishing, or financial-system infrastructure.

## Portfolio role

**Classification: MERGE / ARCHIVE candidate.**

Useful concepts have a stronger home in `cloud-infra`; this repository is retained only as historical engineering context until repository-level archive controls are applied.
