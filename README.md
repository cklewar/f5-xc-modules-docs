# F5-XC-MODULES v0.11.20

This release consists of Terraform template modules to bring up various F5XC components.

# Table of Contents

- [Usage](#usage)
- [F5XC Modules](#f5xc-modules)
- [AWS Modules](#aws-modules)
- [GCP Modules](#gcp-modules)
- [Azure Modules](#azure-modules)

# Usage

- The Terraform templates in this release ment to be used as modules in any root Terraform template environment
- Create a new Terraform project e.g. __f5xc-mcn__
- Clone module library with: `git clone -b  gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-modules` into the new created project folder
- Export P12 cert file password as environment variable: `export VES_P12_PASSWORD=MyPassword`

Folder structure example:

```bash
.
├── cert
└── modules
└── ck.tf
```

Terraform usage example:

```hcl
module "my_test_modul" {
  source = "./modules/f5xc/<module_name>"
  <Module Paramet A> = <Module Paramet A Value>
  <Module Paramet B> = <Module Paramet B Value>
  <Module Paramet C> = <Module Paramet C Value>
}
```

# F5XC Uses Cases

| Use Case                | Documentation               | Status                                                                                                                                                                                                                                                                          |
|-------------------------|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GCP Egress NAT Ingress LB | **[f5-xc-uc-gcp-smg-nat-lb](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-uc-gcp-smg-nat-lb)** | [![f5-xc-uc-gcp-smg-nat-lb](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-uc-gcp-smg-nat-lb/badges/0.11.18/pipeline.svg)](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-uc-gcp-smg-nat-lb) |

# F5XC Modules

| Module                             | Documentation         | Status                                                                                                                                         |
|------------------------------------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| API Credential | **[f5-xc-api-credential](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-api-credential)** | [![f5-xc-api-credential](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-api-credential/badges/0.11.19/pipeline.svg)](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-api-credential) |
| AWS TGW SNode | **[f5-xc-aws-tgw-snode](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-aws-tgw-snode)** | [![f5-xc-aws-tgw-snode](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-aws-tgw-snode/badges/0.11.19/pipeline.svg)](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-aws-tgw-snode) |
| AWS VPC SNode SNIC | **[f5-xc-aws-vpc-snode-snic](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-aws-vpc-snode-snic)** | [![f5-xc-aws-vpc-snode-snic](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-aws-vpc-snode-snic/badges/0.11.19/pipeline.svg)](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-aws-vpc-snode-snic) |
| AWS TGW Multinode | **[f5-xc-aws-tgw-multinode](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-aws-tgw-multinode)** | [![f5-xc-aws-tgw-multinode](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-aws-tgw-multinode/badges/0.11.19/pipeline.svg)](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-aws-tgw-multinode) |
| AWS VPC Multinode | **[f5-xc-aws-vpc-multinode](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-aws-vpc-multinode)** | [![f5-xc-aws-vpc-multinode](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-aws-vpc-multinode/badges/0.11.18/pipeline.svg)](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-aws-vpc-multinode) |
| Azure VNET SNode SNIC | **[f5-xc-azure-vnet-snode-snic](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-azure-vnet-snode-snic)** | [![f5-xc-azure-vnet-snode-snic](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-azure-vnet-snode-snic/badges/0.11.18/pipeline.svg)](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-azure-vnet-snode-snic) |
| Azure VNET Multinode | **[f5-xc-azure-vnet-multinode](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-azure-vnet-multinode)** | [![f5-xc-azure-vnet-multinode](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-azure-vnet-multinode/badges/0.11.19/pipeline.svg)](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-azure-vnet-multinode) |
| GCP VPC SNode SNIC | **[f5-xc-gcp-vpc-snode-snic](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-gcp-vpc-snode-snic)** | [![f5-xc-gcp-vpc-snode-snic](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-gcp-vpc-snode-snic/badges/0.11.19/pipeline.svg)](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-gcp-vpc-snode-snic) |
| GCP VPC Multinode | **[f5-xc-gcp-vpc-multinode](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-gcp-vpc-multinode)** | [![f5-xc-gcp-vpc-multinode](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-gcp-vpc-multinode/badges/0.11.18/pipeline.svg)](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-gcp-vpc-multinode) |
| BGP | **[f5-xc-bgp](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-bgp)** | [![f5-xc-bgp](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-bgp/badges/0.11.19/pipeline.svg)](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-bgp) |
| Blindfold | **[f5-xc-blindfold](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-blindfold)** | [![f5-xc-blindfold](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-blindfold/badges/0.11.19/pipeline.svg)](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-blindfold) |
| DC Cluster Group | **[f5-xc-dc-cluster-group](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-dc-cluster-group)** | [![f5-xc-dc-cluster-group](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-dc-cluster-group/badges/0.11.19/pipeline.svg)](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-dc-cluster-group) |
| Fleet | **[f5-xc-fleet](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-fleet)** | [![f5-xc-fleet](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-fleet/badges/0.11.19/pipeline.svg)](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-fleet) |
| HealthCheck | **[f5-xc-healthcheck](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-healthcheck)** | [![f5-xc-healthcheck](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-healthcheck/badges/0.11.19/pipeline.svg)](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-healthcheck) |
| Interface | **[f5-xc-interface](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-interface)** | [![f5-xc-interface](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-interface/badges/0.11.19/pipeline.svg)](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-interface) |
| IPSec | **[f5-xc-ipsec](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-ipsec)** | [![f5-xc-ipsec](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-ipsec/badges/0.11.19/pipeline.svg)](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-ipsec) |
| Namespace | **[f5-xc-namespace](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-namespace)** | [![f5-xc-namespace](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-namespace/badges/0.11.19/pipeline.svg)](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-namespace) |
| NFV | **[f5-xc-nfv](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-nfv)** | [![f5-xc-nfv](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-nfv/badges/0.11.18/pipeline.svg)](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-nfv) |
| Site Mesh Group | **[f5-xc-site-mesh-group](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-site-mesh-group)** | [![f5-xc-site-mesh-group](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-site-mesh-group/badges/0.11.19/pipeline.svg)](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-site-mesh-group) |
| Virtual k8s | **[f5-xc-virtual-k8s](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-virtual-k8s)** | [![f5-xc-virtual-k8s](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-virtual-k8s/badges/0.11.19/pipeline.svg)](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-virtual-k8s) |
| Virtual Network | **[f5-xc-virtual-network](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-virtual-network)** | [![f5-xc-virtual-network](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-virtual-network/badges/0.11.19/pipeline.svg)](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-virtual-network) |
| Virtual Site | **[f5-xc-virtual-site](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-virtual-site)** | [![f5-xc-virtual-site](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-virtual-site/badges/0.11.19/pipeline.svg)](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-virtual-site) |
| F5XC Regression Environment | **[f5-xc-regression-environment](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-regression-environment)** | [![f5-xc-regression-environment](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-regression-environment/badges/0.11.18/pipeline.svg)](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-regression-environment) |
| GCP Cloud CE | **[f5-xc-gcp-ce](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-gcp-ce)** | [![f5-xc-gcp-ce](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-gcp-ce/badges/None/pipeline.svg)](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-gcp-ce) |
| AWS Cloud CE | **[f5-xc-aws-ce](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-aws-ce)** | [![f5-xc-aws-ce](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-aws-ce/badges/None/pipeline.svg)](https://gitlab.com/volterra/solution/f5-xc-terraform/f5-xc-aws-ce) |

# AWS Modules

| Module | Documentation                                           | Status                                                                                                                                                                                          |
|--------|---------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EC2    | **[aws_ec2](https://github.com/cklewar/aws-ec2)**       | [![F5 XC AWS EC2 module](https://github.com/cklewar/aws-ec2/actions/workflows/module_test.yml/badge.svg?release=0.11.16)](https://github.com/cklewar/aws-ec2/actions/workflows/module_test.yml)  |
| VPC    | **[aws_vpc](https://github.com/cklewar/aws-vpc)**       | [![AWS VPC module](https://github.com/cklewar/aws-vpc/actions/workflows/module_test.yml/badge.svg)](https://github.com/cklewar/aws-vpc/actions/workflows/module_test.yml)                       |
| Subnet | **[aws_subnet](https://github.com/cklewar/aws-subnet)** | [![AWS Subnet module](https://github.com/cklewar/aws-subnets/actions/workflows/module_test.yml/badge.svg)](https://github.com/cklewar/aws-subnets/actions/workflows/module_test.yml)            |
| EKS    | **[aws_eks](https://github.com/cklewar/aws-eks)**       | [![AWS EKS module](https://github.com/cklewar/aws-eks/actions/workflows/module_test.yml/badge.svg?release=main)](https://github.com/cklewar/aws-eks/actions/workflows/module_test.yml)           |

# GCP Modules

| Module  | Documentation                                              | Status                                                                                                                                                                                             |
|---------|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Compute | **[gcp_compute](https://github.com/cklewar/gcp-compute/)** | [![GCP Compute module](https://github.com/cklewar/gcp-compute/actions/workflows/module_test.yml/badge.svg?release=main)](https://github.com/cklewar/gcp-compute/actions/workflows/module_test.yml)  |
|         |                                                            |                                                                                                                                                                                                    |

# Azure Modules

| Module                | Documentation                                                                              | Status                                                                                                                                                                                                                                            |
|-----------------------|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Linux Virtual Machine | **[azure_linux_virtual_machine](https://github.com/cklewar/azure-linux-virtual-machine/)** | [![Azure linux virtual machine module](https://github.com/cklewar/azure-linux-virtual-machine/actions/workflows/module_test.yml/badge.svg?release=main)](https://github.com/cklewar/azure-linux-virtual-machine/actions/workflows/module_test.yml) |
| Resource Group        | **[azure_resource_group](https://github.com/cklewar/azure-resource-group )**               | [![Azure resource group module](https://github.com/cklewar/azure-resource-group/actions/workflows/module_test.yml/badge.svg?release=main)](https://github.com/cklewar/azure-resource-group/actions/workflows/module_test.yml)                      |
| Virtual Network       | **[azure_virtual_network](https://github.com/cklewar/azure-virtual-network/)**             | [![Azure virtual network module](https://github.com/cklewar/azure-virtual-network/actions/workflows/module_test.yml/badge.svg?release=main)](https://github.com/cklewar/azure-virtual-network/actions/workflows/module_test.yml)                   |
| Subnet                | **[azure_subnet](https://github.com/cklewar/azure-subnet )**                               | [![Azure subnet module](https://github.com/cklewar/azure-subnet/actions/workflows/module_test.yml/badge.svg?release=main)](https://github.com/cklewar/azure-subnet/actions/workflows/module_test.yml)                                              |
| Marketplace Agreement | **[azure_marketplace_agreement](https://github.com/cklewar/azure-marketplace-agreement/)** | [![Azure marketplace agreement module](https://github.com/cklewar/azure-marketplace-agreement/actions/workflows/module_test.yml/badge.svg)](https://github.com/cklewar/azure-marketplace-agreement/actions/workflows/module_test.yml)             |