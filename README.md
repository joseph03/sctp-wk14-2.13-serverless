![License](https://img.shields.io/badge/license-MIT-blue.svg)  
![Version](https://img.shields.io/badge/version-1.0.0-green.svg)  

# wk14 2.13 serverless vs terraform

<!-- 2x2 table using html tags -->
<table>
  <!-- Header Row -->
  <tr>
    <th style="background-color: #007bff; color: #ffffff;">Serverless</th>
    <th style="background-color: #007bff; color: #ffffff;">Terraform</th>
  </tr>
  <!-- Data Rows -->
  <tr>
    <td style="background-color: #e6f7ff; color: #333333;">to focus on applicatoin development</td>
    <td style="background-color: #e6f7ff; color: #333333;">declarative infrastructure management for both static and dynamic resources</td>
  </tr>
</table>

## Table of Contents
- [What type of infrastructure and application deployments are each tool best suited for?](#suit)
- [How do their primary objectives differ?](#obj)
- [How do they differ in terms of learning curve and ease of use for developers or DevOps teams?](#learn)
- [What are the differences in how each tool handles state tracking and deployment changes?](#diff)
- [In what scenarios would you recommend using Serverless Framework over Terraform, and vice versa?](#recommend)
- [Are there scenarios where using both together might be beneficial?](#together)

<a id="suit"></a>
## What type of infrastructure and application deployments are each tool best suited for?
| Serverless Framework  | Terraform |
|------|-----------|
| Optimized for rapid deployment and iteration of serverless applications without the need to provision for infrastructure    | Designed for managing a wide range of virtual infrastructure for multi-cloud environments or hybrid setup where consistent infrastructure management across providers is required. Good for large-scale, complex infrastructure setups requiring fine-grained control and modularity.

<a id="obj"></a>
## How do their primary objectives differ?
| Serverless framework	| Terraform | 
|------|-----------|
| The purpose is to focus on the deployment of application without the need to provision on infrastructure. | Aims to provide a cloud-agnostic, declarative way to provision and manage infrastructure with full control over resource configurations and dependencies. |

<a id="learn"></a>
## How do they differ in terms of learning curve and ease of use for developers or DevOps teams?
| Serverless framework	| Terraform | 
|------|-----------|
| Easier to learn for developers already familiar with serverless concepts and the specific cloud provider’s services due to its straightforward YAML syntax and pre-built templates | Steeper, as it requires understanding of infrastructure concepts, cloud provider-specific resources, and Terraform’s own syntax (HCL - HashiCorp Configuration Language). |

<a id="diff"></a>
## What are the differences in how each tool handles state tracking and deployment changes?
| Serverless framework	| Terraform | 
|------|-----------|
| Does not include built-in state tracking. Deployment changes are managed through the underlying cloud provider's stack | Maintains a state file (terraform.tfstate) that tracks the current state of the infrastructure. This state file is crucial for planning and applying changes. |

<a id="recommend"></a>
## In what scenarios would you recommend using Serverless Framework over Terraform, and vice versa?
| Serverless framework	| Terraform | 
|------|-----------|
| For situation where the focus is on the development of application in single cloud provider’s ecosystem rather than infrastructure management | In situation where there is a need to manage complex, multi-cloud, or hybrid infrastructure. |

<a id="together"></a>
## Are there scenarios where using both together might be beneficial?
```bash
In situation where there is a need for the mix of serverless and traditional infrastructure. Terraform can manage the traditional infrastructure, while Serverless Framework handles the serverless components.
```

