---
title: "Week 2 Worklog"
date: 2026-09-30
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Week 2 Objectives

Study Amazon S3 and Amazon CloudFront at an introductory level, focusing on file storage and content delivery. The practical outcome is a sketch of a file delivery flow from S3 through CloudFront, with an explanation of each component.

### Weekly Tasks

| Session | Task | Start Date | Completion Date | Primary Material |
| --- | --- | --- | --- | --- |
| 1 | Explore S3, distinguish buckets from objects, and read examples involving files, images, and website assets. | 30/09/2026 | 30/09/2026 | [Getting Started with Amazon S3](https://000057.awsstudygroup.com/) |
| 2 | Study CloudFront, CDNs, and edge locations; identify the role of a distribution in content delivery. | 01/10/2026 | 01/10/2026 | [CloudFront with an S3 Bucket Origin](https://000094.awsstudygroup.com/) |
| 3 | Read about the connection between S3 and CloudFront; identify the origin and follow a user request to the content in the bucket. | 02/10/2026 | 02/10/2026 | [CloudFront with an S3 Bucket Origin](https://000094.awsstudygroup.com/) |
| 4 | Study caching, distinguish cache hits from cache misses, and examine how cache duration relates to content updates. | 03/10/2026 | 03/10/2026 | [CloudFront with an S3 Bucket Origin](https://000094.awsstudygroup.com/) |
| 5 | Sketch the user → CloudFront → S3 flow, use an HTML file or image as an example, and explain each service's function. | 04/10/2026 | 04/10/2026 | [CloudFront with an S3 Bucket Origin](https://000094.awsstudygroup.com/) |

### Learning and Practical Outcomes

#### Amazon S3 Storage

Understand that a bucket contains objects and that an object includes file data and associated metadata. Know that an object key identifies an object within a bucket and that prefixes can help organize names.

Can identify suitable S3 examples such as images, documents, HTML, CSS, and JavaScript files. Can distinguish file storage in S3 from running an application on EC2, covered in Week 1. The reading also clarified that storing a file and granting access to it are separate configuration concerns.

#### Amazon CloudFront Content Delivery

Understand CloudFront's content delivery role and the origin as the source of the original content. Know that an S3 bucket can serve as an origin and that a distribution defines how CloudFront receives requests and delivers content.

Recognize that edge locations help serve content closer to users. Can explain the general purpose of a CDN for frequently requested website assets such as images and interface files.

#### Caching and Request Flow

Understand a cache hit as a request for suitable content already in the cache, while a cache miss requires CloudFront to fetch content from the origin. Recognize that cache duration affects when users receive updated content.

Can follow the basic request flow: a user accesses CloudFront, which checks its cache and retrieves content from S3 when needed. Can explain the different roles of storage and delivery in this flow.

#### Practical Outcome

Sketched a file delivery diagram and explained the request path using an HTML file or image. Identified the user, distribution, cache, and S3 origin in the diagram.

Can describe this simple model as preparation for configuration practice. This week's work consists of reading and diagramming; it does not record a deployed distribution or a complete website.

### Supplementary Material

* [Amazon S3 — Overview](https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html): reference for buckets, objects, and data access.
* [CloudFront — Content Delivery](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/HowCloudFrontWorks.html): further reading on origins, edge locations, and caching.
