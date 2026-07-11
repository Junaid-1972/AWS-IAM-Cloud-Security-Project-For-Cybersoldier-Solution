# AWS-IAM-Cloud-Security-Project

 This repository showcases a cloud console hardening project For Cybersoldier Solution in AWS, mapped to NIST CSF Protect/Detect functions and ISO 27001 Annex A.5 (Organizational Controls) plus Annex A.8 (Technological Controls). It demonstrates how secure configuration and monitoring strengthen cloud governance and compliance with international standards.

# AWS IAM Cloud Security Project

**Implementing Least Privilege Access Controls in Amazon Web Services (AWS)**

**Project Focus:** Identity and Access Management (IAM)  
**Date:** [Insert Date]

---

## Table of Contents

- [Project Overview]
- [Tools & Concepts]
- [IAM Users]
- [IAM Groups]
- [Logging in as IAM User]
- [EC2 Instance Creation]
- [Tagging Strategy]
- [S3 Bucket Creation]
- [S3 Bucket Policy]
- [Policy Testing]
- [Screenshots / Evidence]
- [Conclusion]

---

## Project Overview

This project focused on implementing cloud security best practices in **Amazon Web Services (AWS)**, with a strong emphasis on **Identity and Access Management (IAM)**.  

The main objective was to demonstrate the **Principle of Least Privilege** by:
- Creating IAM users and groups
- Developing a custom IAM/S3 policy
- Attaching the policy to restrict user actions on an S3 bucket
- Verifying that unauthorized actions (such as deleting the bucket or bucket policy) are properly denied

---

## Tools & Concepts

- **AWS IAM** – Users, Groups, and Policies
- **Amazon EC2** – Instance creation and resource tagging
- **Amazon S3** – Bucket creation and object management
- **JSON Policy Language** – Effect, Action, Resource elements
- **Principle of Least Privilege**
- **Policy Testing & Validation**

---

## IAM Users

Two IAM users were created:

- `cybersoldier-security-alabi`
- `cybersoldier-developer-tunji`

---

## IAM Groups

1. Created two IAM groups:
   - `cybersoldier-security`
   - `cybersoldier-developer`

2. Assigned users to appropriate groups:
   - `cybersoldier-security-alabi` → Security Group
   - `cybersoldier-developer-tunji` → Developer Group

---

## Logging in as IAM User

IAM users can authenticate via:
- **AWS Management Console** (using account alias URL)
- **AWS CLI** (using programmatic access keys)

---

## EC2 Instance Creation

- **Instance Name:** `Cybersoldier-Windows-Server`
- Launched using the EC2 service for workload simulation.

---

## Tagging Strategy

Applied the following tags to the EC2 instance:

| Key     | Value                  |
|---------|------------------------|
| Name    | Cybersoldier-Windows-Server |
| Design  | Webapp                 |

---

## S3 Bucket Creation

- **Bucket Name:** `cybersoldierbucket`
- Created a General Purpose S3 bucket
- Uploaded a sample object for testing

---

## S3 Bucket Policy

A custom JSON bucket policy was created to explicitly **deny** the following actions for IAM users:
- Delete the bucket
- Delete or modify the bucket policy

This provides an additional layer of protection at the resource level.

---

## Policy Testing

| Test Action                          | Expected Result | Actual Result                          |
|--------------------------------------|-----------------|----------------------------------------|
| Delete Bucket / Delete Bucket Policy | Denied          | Access Denied – No permission granted  |

The policy successfully blocked destructive actions.

---

## Screenshots / Evidence

**Key screenshots captured during the project:**

- IAM Users successfully created (`cybersoldier-security-alabi` & `cybersoldier-developer-tunji`)
- ![image alt](https://github.com/Junaid-1972/AWS-IAM-Cloud-Security-Project-For-Cybersoldier-Solution/blob/main/IAM%20user.png?raw=true)
- IAM Groups (`cybersoldier-security` and `cybersoldier-developer`) with users attached
- ![image alt](https://github.com/Junaid-1972/AWS-IAM-Cloud-Security-Project-For-Cybersoldier-Solution/blob/main/IAM%20usergroup.png?raw=true)
- EC2 Instance (`Cybersoldier-Windows-Server`) running with proper tags applied
- ![image alt]()
- S3 Bucket (`cybersoldierbucket`) created and object uploaded
- ![image alt](https://github.com/Junaid-1972/AWS-IAM-Cloud-Security-Project-For-Cybersoldier-Solution/blob/main/Bucket.png?raw=true)
- Custom S3 Bucket Policy in JSON format
- ![image alt](https://github.com/Junaid-1972/AWS-IAM-Cloud-Security-Project-For-Cybersoldier-Solution/blob/main/S3%20bucket%20policy.png?raw=true)
- Policy enforcement test showing "Access Denied" when attempting to delete the bucket or bucket policy
- ![image alt](https://github.com/Junaid-1972/AWS-IAM-Cloud-Security-Project-For-Cybersoldier-Solution/blob/main/Bucket%20policy%20enforced.png?raw=true)
- AWS Management Console views for IAM, EC2, and S3 services
- ![image alt](https://github.com/Junaid-1972/AWS-IAM-Cloud-Security-Project-For-Cybersoldier-Solution/blob/main/Login%20as%20IAM%20user.png?raw=true)

*(All major steps were documented with screenshots in the original report for verification and portfolio purposes)*

---

## Conclusion

This project successfully demonstrated the implementation of robust cloud security measures using **AWS IAM** and **S3 Bucket Policies**.  

By applying the **Principle of Least Privilege** and using proper resource tagging and bucket policies, the project effectively protects cloud infrastructure and sensitive data.  

The hands-on experience provided valuable insights into cloud security governance and serves as a strong foundation for future cloud security initiatives — ensuring the **Confidentiality, Integrity, and Availability** of data in AWS environments.

---

**Project Author:** JUNAID ABDULRAHMAN A  
**Role:** Cybersecurity Analyst
