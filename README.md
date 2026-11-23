# AZ-104 Azure Administrator Lab

Hands-on labs built while preparing for the **Microsoft Certified: Azure Administrator Associate (AZ-104)** certification.

## Objective

Build practical, repeatable experience with the Azure administration tasks covered by the AZ-104 exam. Each lab is completed three ways:

- **Azure Portal**: to learn how the services work and where things are configured
- **Azure CLI**: to script and automate the same tasks
- **Bicep**: to define the resources as Infrastructure as Code

After each lab I write a short summary of what I learned and publish it on LinkedIn.

## Scope

The repository contains **5 labs, one for each AZ-104 exam domain**:

| # | Lab | Exam domain | Key topics |
|---|-----|-------------|------------|
| 1 | Identities & Governance | Manage Azure identities and governance | Microsoft Entra ID users & groups, RBAC, Azure Policy, resource locks, tags, management groups, cost management |
| 2 | Storage | Implement and manage storage | Storage accounts, redundancy, Blob & Azure Files, access tiers, lifecycle management, SAS & access keys, network access |
| 3 | Compute | Deploy and manage Azure compute resources | Virtual Machines, availability sets/zones, VM Scale Sets, App Service, Azure Container Instances, Bicep/ARM deployments |
| 4 | Virtual Networking | Implement and manage virtual networking | VNets & subnets, peering, NSGs/ASGs, Azure DNS, Load Balancer, Application Gateway, Bastion, service & private endpoints |
| 5 | Monitor & Maintain | Monitor and maintain Azure resources | Azure Monitor, Log Analytics & KQL, alerts & action groups, Network Watcher, Azure Backup, Azure Site Recovery |

**Out of scope:** topics from other certifications (AZ-305, AZ-400, AZ-500), and production-grade or multi-tenant architectures. These labs are for learning only.

## Repository Structure

```
.
├── app/       # Sample application deployed in the labs (e.g. App Service / VM)
├── bicep/     # Bicep templates for each lab
├── content/   # LinkedIn posts summarizing each lab
├── docs/      # Lab guides, diagrams and screenshots
├── labs/      # Step-by-step instructions and Azure CLI scripts per lab
├── notes/     # Personal study notes and exam tips
└── README.md
```

## Roadmap

- [ ] **Setup**: Azure subscription, Azure CLI and Bicep installed, budget alert set up
- [ ] **Lab 1**: Identities & Governance
  - [ ] Portal walkthrough
  - [ ] Azure CLI scripts
  - [ ] Bicep templates
  - [ ] LinkedIn summary
- [ ] **Lab 2**: Storage
  - [ ] Portal walkthrough
  - [ ] Azure CLI scripts
  - [ ] Bicep templates
  - [ ] LinkedIn summary
- [ ] **Lab 3**: Compute
  - [ ] Portal walkthrough
  - [ ] Azure CLI scripts
  - [ ] Bicep templates
  - [ ] Deploy sample app from `app/`
  - [ ] LinkedIn summary
- [ ] **Lab 4**: Virtual Networking
  - [ ] Portal walkthrough
  - [ ] Azure CLI scripts
  - [ ] Bicep templates
  - [ ] LinkedIn summary
- [ ] **Lab 5**: Monitor & Maintain
  - [ ] Portal walkthrough
  - [ ] Azure CLI scripts
  - [ ] Bicep templates
  - [ ] LinkedIn summary
- [ ] **Exam prep**: practice assessments and review of weak areas
- [ ] **AZ-104 exam**

## Prerequisites

- An Azure subscription (a [free account](https://azure.microsoft.com/free/) works for most labs)
- [Azure CLI](https://learn.microsoft.com/cli/azure/install-azure-cli)
- [Bicep CLI](https://learn.microsoft.com/azure/azure-resource-manager/bicep/install) (`az bicep install`)
- [VS Code](https://code.visualstudio.com/) with the Bicep extension (recommended)

## Cost & Cleanup

Each lab uses its own resource group, so it can be deleted in one step when you finish:

```bash
az group delete --name <lab-resource-group> --yes --no-wait
```

Set up a budget alert in Cost Management before you start.

## References

- [AZ-104 exam page](https://learn.microsoft.com/credentials/certifications/azure-administrator/)
- [AZ-104 study guide](https://learn.microsoft.com/credentials/certifications/resources/study-guides/az-104)
- [Microsoft Learn: AZ-104 learning paths](https://learn.microsoft.com/training/courses/az-104t00)
- [Official AZ-104 labs (MicrosoftLearning)](https://github.com/MicrosoftLearning/AZ-104-MicrosoftAzureAdministrator)

## Disclaimer

This is a personal study project and is not affiliated with Microsoft.
