---
title: "Week 4 Worklog"
date: 2026-10-12
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Week 4 Objectives

Study Amazon RDS, Amazon Lightsail, Amazon EC2 Auto Scaling, and Amazon CloudWatch through First Cloud Journey workshops. Apply the EC2, IAM role, and load balancer work to database connectivity, application scaling, and system monitoring.

### Learning and Practice Plan

| Session | Task | Planned Start Date | Planned Completion Date | Primary Material |
| --- | --- | --- | --- | --- |
| 1 | Study RDS, database engines, DB instances, and endpoints; prepare a DB subnet group, configure EC2 connectivity, create a database, and test backup and restore following the workshop. | 12/10/2026 | 12/10/2026 | [Create a Database with Amazon RDS](https://000005.awsstudygroup.com/) |
| 2 | Explore Lightsail plans and blueprints; deploy one sample application from the workshop, configure networking, test access, create a snapshot, and read the instance upgrade workflow. | 13/10/2026 | 13/10/2026 | [Optimize Costs with Amazon Lightsail](https://000045.awsstudygroup.com/) |
| 3 | Create a launch template and Auto Scaling Group; integrate the load balancer and set minimum, desired, and maximum capacity; test manual, scheduled, and dynamic scaling, and read about predictive scaling. | 14/10/2026 | 14/10/2026 | [Application Scaling with EC2 Auto Scaling](https://000006.awsstudygroup.com/) |
| 4 | View metrics and study log groups and streams; practice Logs Insights, metric filters, alarms, and dashboards; observe data during application and scaling tests. | 15/10/2026 | 15/10/2026 | [System Monitoring with CloudWatch](https://000008.awsstudygroup.com/) |
| 5 | Summarize configurations, checks, and observations; explain the four services' roles, clean up resources following the guides, and inspect remaining resources. | 16/10/2026 | 16/10/2026 | [Explore AWS Services](https://cloudjourney.awsstudygroup.com/1-explore/) |

### Expected Knowledge and Practical Skills

#### Amazon RDS

Understand managed relational databases and distinguish the database engine, DB instance, endpoint, and connection port. Identify the network settings, security groups, and login details required for an application on EC2 to connect.

Practice creating a DB instance, obtaining its endpoint, and testing the application connection. Learn to check database status, endpoint, port, and network rules in sequence when a connection fails. Explore backup, snapshots, and restore procedures within the lab.

#### Amazon Lightsail

Understand Lightsail plans and blueprints for deploying servers or applications. Learn to review the resources included in a plan, usage allowances, and potentially billable components before choosing one.

Practice deploying a sample application, inspecting network settings, and testing browser access. Study snapshots and the workflow for creating a larger instance from a snapshot. Be able to explain when Lightsail's simple deployment approach suits a small website or application.

#### Amazon EC2 Auto Scaling

Understand launch templates as stored launch settings and Auto Scaling Groups as capacity management within minimum, desired, and maximum limits. Distinguish request distribution by a load balancer from changing server numbers through Auto Scaling.

Practice integrating the group with a load balancer, changing desired capacity, and checking that new instances join the target group. Test scheduled and dynamic scaling following the workshop and inspect activity history for capacity changes. Predictive scaling study focuses on the mechanism and metrics introduced in the material.

#### Amazon CloudWatch

Distinguish metrics for measurements, logs for events, alarms for evaluating alert conditions, and dashboards for a combined view. Learn to select the appropriate time range and resource when reading data.

Practice log queries with Logs Insights, explore converting log patterns into metrics with metric filters, configure an alarm, and create a dashboard. Compare metrics with scaling activity to explain workload and instance count changes during the lab.

#### Practice Review and Checks

Record key settings, successful checks, and troubleshooting steps. Clean up after each workshop and inspect remaining components such as snapshots or storage resources. The goal is to perform basic guided configurations and explain the observations.

### Supplementary Material

* [Amazon RDS — Getting Started](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_GettingStarted.html): reference for creating and connecting to DB instances.
* [Amazon Lightsail — Overview](https://docs.aws.amazon.com/lightsail/latest/userguide/what-is-amazon-lightsail.html): reference for service plans and components.
* [EC2 Auto Scaling — Capacity Limits](https://docs.aws.amazon.com/autoscaling/ec2/userguide/asg-capacity-limits.html): reference for minimum, desired, and maximum capacity.
* [Amazon CloudWatch — Overview](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/WhatIsCloudWatch.html): reference for basic monitoring capabilities.
