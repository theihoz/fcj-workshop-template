---
title: "Week 3 Worklog"
date: 2026-10-05
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Week 3 Objectives

Use EC2 to study data management, application permissions, and load balancing. Focus on EBS snapshots, AMIs, IAM roles, and the Application Load Balancer, building on Week 1's server introduction to configure a simple web application.

### Weekly Tasks

| Session | Task | Start Date | Completion Date | Primary Material |
| --- | --- | --- | --- | --- |
| 1 | Compare EBS and instance store; mount an attached volume, inspect its data, and create an EBS snapshot for backup. | 05/10/2026 | 05/10/2026 | [Amazon EC2](https://000004.awsstudygroup.com/) |
| 2 | Study IAM users, roles, policies, and least privilege; read Effect, Action, and Resource in a policy, and distinguish trust policies from permissions policies. | 06/10/2026 | 06/10/2026 | [Access Management with IAM](https://000002.awsstudygroup.com/) |
| 3 | Create an EC2 IAM role with S3 read access, attach it to an instance, and test access through the server's CLI without storing separate access keys on the instance. | 07/10/2026 | 07/10/2026 | [Application Access through an IAM Role](https://000048.awsstudygroup.com/) |
| 4 | Deploy a sample web application on EC2, check service ports and security groups, and study AMI creation to preserve the configured environment. | 08/10/2026 | 08/10/2026 | [Amazon EC2](https://000004.awsstudygroup.com/) |
| 5 | Study basic ALB and NLB use cases; create an ALB, listener, and target group for web servers, configure health checks, and test request distribution. | 09/10/2026 | 10/10/2026 | [Load Balancer Section of the FCJ Workshop](https://000006.awsstudygroup.com/) |

### Learning and Practical Outcomes

#### EC2 Storage and Backup

Understand that EBS volumes are managed separately from instances, while instance store is associated with the physical server hosting the instance. Know to inspect storage type and deletion settings to determine which data remains after instance termination.

Practiced mounting an EBS volume and creating a snapshot. Can distinguish attaching a volume in the Console from making it usable by the operating system. Understand a snapshot as a backup point from which a volume can be created for recovery.

#### IAM and Permission Scope

Can distinguish IAM users and roles for a guided lab. Understand that policies describe allowed or denied actions on resources. A trust policy identifies who can assume a role, while a permissions policy defines what the role can do.

Can read the main elements of a sample policy and explain why a read-only application does not need write or delete access. This supports choosing permissions for a simple lab and reviewing them when access is denied.

#### IAM Roles for EC2

Created a role with S3 read access, attached it to an EC2 instance, and tested access through the server's CLI. Understand the instance profile's role in associating an IAM role with EC2 and the use of temporary credentials by applications.

Can distinguish the local access configuration from Week 1 from permissions received through an EC2 role. Know to inspect the attached role and its policies when a service request does not work as expected.

#### Web Application and AMI

Practiced deploying a sample web application, checking service status, and reviewing its access port. Know to compare the application's listening port with security group rules when browser access fails.

Understand that an AMI can preserve a configured server environment for later launches. Can distinguish data backup through an EBS snapshot from creating a server image through an AMI.

#### ALB Load Balancing

Understand ALB's role for HTTP/HTTPS traffic and NLB's role for connection-level traffic such as TCP. Can identify the listener receiving requests, the target group containing servers, and the health check assessing a target's ability to serve requests.

Practiced configuring an ALB with EC2 instances, inspecting target health, and accessing the application through the load balancer address. Can follow the user → ALB → target group → EC2 flow and review ports, health check paths, and security groups when a target is unhealthy.

Can use these storage, permission, and load balancing settings in a guided lab and explain how each supports the application.

### Supplementary Material

* [IAM Roles for Amazon EC2](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/iam-roles-for-amazon-ec2.html): reference for instance profiles and temporary credentials.
* [ALB Target Groups](https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-target-groups.html): reference for targets, listeners, and health checks.
