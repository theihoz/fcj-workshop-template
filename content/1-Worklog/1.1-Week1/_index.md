---
title: "Week 1 Worklog"
date: 2026-09-23
weight: 1
chapter: false
pre: " <b> 1.1. </b> "
---

### Week 1 Objectives

Become familiar with the First Cloud AI Journey internship, AWS service categories, and resource management through the AWS Management Console and AWS CLI. Practice focuses on launching an EC2 instance, connecting over SSH, and identifying the components of a basic server.

### Weekly Tasks

| Session | Task | Start Date | Completion Date | Primary Material |
| --- | --- | --- | --- | --- |
| 1 | Meet FCAJ members, read the internship rules, and establish a way to record learning activities. | 23/09/2026 | 23/09/2026 | [First Cloud Journey](https://cloudjourney.awsstudygroup.com/) |
| 2 | Explore cloud computing and the compute, storage, networking, and database categories; identify the basic roles of EC2, S3, VPC, and RDS in an application. | 24/09/2026 | 25/09/2026 | [Explore AWS Services](https://cloudjourney.awsstudygroup.com/1-explore/) |
| 3 | Create an AWS account and explore the Console; install AWS CLI, configure access and Region settings, and check the active account. | 24/09/2026 | 25/09/2026 | [Create an AWS Account](https://000001.awsstudygroup.com/) |
| 4 | Study instances, AMIs, instance types, key pairs, security groups, EBS, and Elastic IP; read the server launch and SSH connection workflow. | 25/09/2026 | 26/09/2026 | [Getting Started with Amazon EC2](https://000004.awsstudygroup.com/) |
| 5 | Launch an EC2 instance following the guide, connect over SSH, and attach an EBS volume; compare instance information in the Console and CLI. | 25/09/2026 | 26/09/2026 | [Getting Started with Amazon EC2](https://000004.awsstudygroup.com/) |

### Learning and Practical Outcomes

#### Internship and Learning Approach

Became familiar with the team and internship rules. Learned to select service workshops from Cloud Journey, read prerequisites before practice, and record configuration steps for use when troubleshooting.

#### AWS Service Categories

Gained a basic understanding of EC2 for virtual servers, S3 for object storage, VPC for networking, and RDS for relational databases. Can identify a suitable service category for simple needs such as running an application, storing files, or keeping structured data.

Recognize that resources are deployed in a selected Region and that the Region must be checked when locating resources in the Console or CLI. This understanding is sufficient to follow an introductory lab and read a simple system diagram.

#### AWS Account and Management Console

Created an AWS account and practiced finding services, opening resource pages, selecting a Region, and reading configuration details. Learned to check resource status after creation rather than relying only on the completion message.

#### AWS CLI

Installed and configured AWS CLI locally. Understand the purpose of credentials, the default Region, and profiles, and can check the active configuration before using resources.

Used basic commands to inspect account information, Regions, EC2 instances, and key pairs. Can compare instance IDs, states, and IP addresses between the Console and CLI. Current practice covers individual commands with reference to the guide.

#### Introductory EC2 Practice

Can distinguish the role of an AMI, instance type, key pair, and security group. Understand that EBS provides attached storage and that an Elastic IP is a separately allocated public IPv4 address.

Practiced launching an instance, connecting over SSH, and attaching an EBS volume. Know to review the IP address, username, key pair, and SSH access rule when checking a connection. Can use an EC2 server for a basic guided lab.

### Supplementary Material

* [AWS CLI — Initial Configuration](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-quickstart.html): reference for profiles, Regions, and authentication methods.
