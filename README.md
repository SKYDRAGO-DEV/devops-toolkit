# devops-toolkit

> Production-grade DevOps automation toolkit | Terraform, Kubernetes, CI/CD, Monitoring & Cloud Infrastructure as Code

[![Terraform](https://img.shields.io/badge/Terraform-7B36BC?style=flat-square&logo=terraform)](https://www.terraform.io/)
[![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes)](https://kubernetes.io/)
[![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker)](https://docker.com/)
[![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=github-actions)](https://github.com/features/actions)

## Modules

| Module | Description | Status |
|--------|-------------|--------|
| `terraform/aws-infra` | AWS baseline infrastructure | ✅ Stable |
| `terraform/gcp-infra` | GCP baseline infrastructure | 🚧 Beta |
| `kubernetes/app-templates` | K8s application templates | ✅ Stable |
| `ci-cd` | GitHub Actions workflows | ✅ Stable |
| `monitoring` | Prometheus + Grafana stack | 🚧 Beta |

## Quick Start

\`\`\`bash
# Terraform AWS setup
cd terraform/aws-infra
terraform init
terraform plan -var-file=prod.tfvars
terraform apply

# Kubernetes deployment
kubectl apply -f kubernetes/app-templates/api-service.yaml

# CI/CD pipeline (GitHub Actions)
gh workflow run deploy
\`\`\`

## Directory Structure

\`\`\`
.
├── terraform/           # Infrastructure as Code
│   ├── aws-infra/       # AWS resources
│   └── gcp-infra/       # GCP resources
├── kubernetes/          # K8s manifests
│   ├── app-templates/   # Reusable templates
│   └── monitoring/      # Observability stack
├── ci-cd/               # CI/CD pipelines
└── scripts/             # Automation scripts
\`\`\`

## License

MIT © SKYDRAGO-DEV
