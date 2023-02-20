# F5-XC-MODULES v0.11.19

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
- Clone module library with: `git clone -b 0.11.19 github.com/cklewar/f5-xc-modules` into the new created project folder
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
| GCP Egress NAT Ingress LB | **[f5-xc-uc-gcp-smg-nat-lb](https://github.com/cklewar/f5-xc-uc-gcp-smg-nat-lb)** | [![GCP Egress NAT Ingress LB](https://github.com/cklewar/f5-xc-uc-gcp-smg-nat-lb/actions/workflows/module_v0_11_18.yml/badge.svg?branch=0.11.18)](https://github.com/cklewar/f5-xc-uc-gcp-smg-nat-lb/actions/workflows/module_v0_11_18.yml) |
| Regression Env | **[f5-xc-regression-environment](https://github.com/cklewar/f5-xc-regression-environment)** | [![Regression Env](https://github.com/cklewar/f5-xc-regression-environment/actions/workflows/module_v0_11_18.yml/badge.svg?branch=0.11.18)](https://github.com/cklewar/f5-xc-regression-environment/actions/workflows/module_v0_11_18.yml) |

# F5XC Modules

| Module                             | Documentation         | Status                                                                                                                                         |
|------------------------------------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| API Credential | **[f5-xc-api-credential](https://github.com/cklewar/f5-xc-api-credential)** | [![API Credential](https://github.com/cklewar/f5-xc-api-credential/actions/workflows/module_v0_11_19.yml/badge.svg?branch=0.11.19)](https://github.com/cklewar/f5-xc-api-credential/actions/workflows/module_v0_11_19.yml) |
| AWS TGW Multinode | **[f5-xc-aws-tgw-multinode](https://github.com/cklewar/f5-xc-aws-tgw-multinode)** | [![AWS TGW Multinode](https://github.com/cklewar/f5-xc-aws-tgw-multinode/actions/workflows/module_v0_11_18.yml/badge.svg?branch=0.11.18)](https://github.com/cklewar/f5-xc-aws-tgw-multinode/actions/workflows/module_v0_11_18.yml) |
| AWS TGW SNode | **[f5-xc-aws-tgw-snode](https://github.com/cklewar/f5-xc-aws-tgw-snode)** | [![AWS TGW SNode](https://github.com/cklewar/f5-xc-aws-tgw-snode/actions/workflows/module_v0_11_19.yml/badge.svg?branch=0.11.19)](https://github.com/cklewar/f5-xc-aws-tgw-snode/actions/workflows/module_v0_11_19.yml) |
| AWS VPC Multinode | **[f5-xc-aws-vpc-multinode](https://github.com/cklewar/f5-xc-aws-vpc-multinode)** | [![AWS VPC Multinode](https://github.com/cklewar/f5-xc-aws-vpc-multinode/actions/workflows/module_v0_11_18.yml/badge.svg?branch=0.11.18)](https://github.com/cklewar/f5-xc-aws-vpc-multinode/actions/workflows/module_v0_11_18.yml) |
| AWS VPC SNode SNIC | **[f5-xc-aws-vpc-snode-snic](https://github.com/cklewar/f5-xc-aws-vpc-snode-snic)** | [![AWS VPC SNode SNIC](https://github.com/cklewar/f5-xc-aws-vpc-snode-snic/actions/workflows/module_v0_11_19.yml/badge.svg?branch=0.11.19)](https://github.com/cklewar/f5-xc-aws-vpc-snode-snic/actions/workflows/module_v0_11_19.yml) |
| AWS Cloud CE | **[f5-xc-aws-ce](https://github.com/cklewar/f5-xc-aws-ce)** | [![AWS Cloud CE](https://github.com/cklewar/f5-xc-aws-ce/actions/workflows/module_v0_11_18.yml/badge.svg?branch=0.11.18)](https://github.com/cklewar/f5-xc-aws-ce/actions/workflows/module_v0_11_18.yml) |
| Azure VNET Multinode | **[f5-xc-azure-vnet-multinode](https://github.com/cklewar/f5-xc-azure-vnet-multinode)** | [![Azure VNET Multinode](https://github.com/cklewar/f5-xc-azure-vnet-multinode/actions/workflows/module_v0_11_18.yml/badge.svg?branch=0.11.18)](https://github.com/cklewar/f5-xc-azure-vnet-multinode/actions/workflows/module_v0_11_18.yml) |
| Azure VNET SNode SNIC | **[f5-xc-azure-vnet-snode-snic](https://github.com/cklewar/f5-xc-azure-vnet-snode-snic)** | [![Azure VNET SNode SNIC](https://github.com/cklewar/f5-xc-azure-vnet-snode-snic/actions/workflows/module_v0_11_18.yml/badge.svg?branch=0.11.18)](https://github.com/cklewar/f5-xc-azure-vnet-snode-snic/actions/workflows/module_v0_11_18.yml) |
| GCP VPC Singlenode | **[f5-xc-gcp-vpc-snode-snic](https://github.com/cklewar/f5-xc-gcp-vpc-snode-snic)** | [![GCP VPC Singlenode](https://github.com/cklewar/f5-xc-gcp-vpc-snode-snic/actions/workflows/module_v0_11_19.yml/badge.svg?branch=0.11.19)](https://github.com/cklewar/f5-xc-gcp-vpc-snode-snic/actions/workflows/module_v0_11_19.yml) |
| GCP VPC Multinode | **[f5-xc-gcp-vpc-multinode](https://github.com/cklewar/f5-xc-gcp-vpc-multinode)** | [![GCP VPC Multinode](https://github.com/cklewar/f5-xc-gcp-vpc-multinode/actions/workflows/module_v0_11_18.yml/badge.svg?branch=0.11.18)](https://github.com/cklewar/f5-xc-gcp-vpc-multinode/actions/workflows/module_v0_11_18.yml) |
| GCP Cloud CE | **[f5-xc-gcp-ce](https://github.com/cklewar/f5-xc-gcp-ce)** | [![GCP Cloud CE](https://github.com/cklewar/f5-xc-gcp-ce/actions/workflows/module_v0_11_19.yml/badge.svg?branch=0.11.19)](https://github.com/cklewar/f5-xc-gcp-ce/actions/workflows/module_v0_11_19.yml) |
| BGP | **[f5-xc-bgp](https://github.com/cklewar/f5-xc-bgp)** | [![BGP](https://github.com/cklewar/f5-xc-bgp/actions/workflows/module_v0_11_19.yml/badge.svg?branch=0.11.19)](https://github.com/cklewar/f5-xc-bgp/actions/workflows/module_v0_11_19.yml) |
| Blindfold | **[f5-xc-blindfold](https://github.com/cklewar/f5-xc-blindfold)** | [![Blindfold](https://github.com/cklewar/f5-xc-blindfold/actions/workflows/module_v0_11_19.yml/badge.svg?branch=0.11.19)](https://github.com/cklewar/f5-xc-blindfold/actions/workflows/module_v0_11_19.yml) |
| DC Cluster Group | **[f5-xc-dc-cluster-group](https://github.com/cklewar/f5-xc-dc-cluster-group)** | [![DC Cluster Group](https://github.com/cklewar/f5-xc-dc-cluster-group/actions/workflows/module_v0_11_19.yml/badge.svg?branch=0.11.19)](https://github.com/cklewar/f5-xc-dc-cluster-group/actions/workflows/module_v0_11_19.yml) |
| Fleet | **[f5-xc-fleet](https://github.com/cklewar/f5-xc-fleet)** | [![Fleet](https://github.com/cklewar/f5-xc-fleet/actions/workflows/module_v0_11_19.yml/badge.svg?branch=0.11.19)](https://github.com/cklewar/f5-xc-fleet/actions/workflows/module_v0_11_19.yml) |
| HealthCheck | **[f5-xc-healthcheck](https://github.com/cklewar/f5-xc-healthcheck)** | [![HealthCheck](https://github.com/cklewar/f5-xc-healthcheck/actions/workflows/module_v0_11_18.yml/badge.svg?branch=0.11.18)](https://github.com/cklewar/f5-xc-healthcheck/actions/workflows/module_v0_11_18.yml) |
| Interface | **[f5-xc-interface](https://github.com/cklewar/f5-xc-interface)** | [![Interface](https://github.com/cklewar/f5-xc-interface/actions/workflows/module_v0_11_19.yml/badge.svg?branch=0.11.19)](https://github.com/cklewar/f5-xc-interface/actions/workflows/module_v0_11_19.yml) |
| IPSec | **[f5-xc-ipsec](https://github.com/cklewar/f5-xc-ipsec)** | [![IPSec](https://github.com/cklewar/f5-xc-ipsec/actions/workflows/module_v0_11_19.yml/badge.svg?branch=0.11.19)](https://github.com/cklewar/f5-xc-ipsec/actions/workflows/module_v0_11_19.yml) |
| Namespace | **[f5-xc-namespace](https://github.com/cklewar/f5-xc-namespace)** | [![Namespace](https://github.com/cklewar/f5-xc-namespace/actions/workflows/module_v0_11_19.yml/badge.svg?branch=0.11.19)](https://github.com/cklewar/f5-xc-namespace/actions/workflows/module_v0_11_19.yml) |
| NFV | **[f5-xc-nfv](https://github.com/cklewar/f5-xc-nfv)** | [![NFV](https://github.com/cklewar/f5-xc-nfv/actions/workflows/module_v0_11_19.yml/badge.svg?branch=0.11.19)](https://github.com/cklewar/f5-xc-nfv/actions/workflows/module_v0_11_19.yml) |
| Site Mesh Group | **[f5-xc-site-mesh-group](https://github.com/cklewar/f5-xc-site-mesh-group)** | [![Site Mesh Group](https://github.com/cklewar/f5-xc-site-mesh-group/actions/workflows/module_v0_11_19.yml/badge.svg?branch=0.11.19)](https://github.com/cklewar/f5-xc-site-mesh-group/actions/workflows/module_v0_11_19.yml) |
| Virtual k8s | **[f5-xc-virtual-k8s](https://github.com/cklewar/f5-xc-virtual-k8s)** | [![Virtual k8s](https://github.com/cklewar/f5-xc-virtual-k8s/actions/workflows/module_v0_11_19.yml/badge.svg?branch=0.11.19)](https://github.com/cklewar/f5-xc-virtual-k8s/actions/workflows/module_v0_11_19.yml) |
| Virtual Network | **[f5-xc-virtual-network](https://github.com/cklewar/f5-xc-virtual-network)** | [![Virtual Network](https://github.com/cklewar/f5-xc-virtual-network/actions/workflows/module_v0_11_19.yml/badge.svg?branch=0.11.19)](https://github.com/cklewar/f5-xc-virtual-network/actions/workflows/module_v0_11_19.yml) |
| Virtual Site | **[f5-xc-virtual-site](https://github.com/cklewar/f5-xc-virtual-site)** | [![Virtual Site](https://github.com/cklewar/f5-xc-virtual-site/actions/workflows/module_v0_11_19.yml/badge.svg?branch=0.11.19)](https://github.com/cklewar/f5-xc-virtual-site/actions/workflows/module_v0_11_19.yml) |

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