# Pre-Interview Assignment – DevOps Engineer Task

**Candidate:** Anniq Suha 
**Date:** Jan 28 2026  
**Company:** PacerPro, Inc.

---

## Repository Structure

This repository contains all parts of the pre-interview assignment:

- `sumo_logic_query.txt` – Sumo Logic query for monitoring API response times.
- `lambda_function/` – Python AWS Lambda function triggered by the Sumo Logic alert.
- `terraform/` – Terraform scripts to deploy EC2 instance, Lambda function, and SNS topic.
- `recordings/` – Screen and audio recordings for each part.
- `README.md` – This documentation file.

## Important Note to Reviewer

To make reviewing this submission easier and organized, I have separated the work into multiple recordings, each demonstrating a specific part of the assignment:

1. **Recording 1** – Creating the Sumo Logic query and setting up the alert/monitor.  
2. **Recording 2** – Setting up the AWS environment: creating an EC2 instance, IAM roles, and policies.  
3. **Recording 3** – Developing, deploying, and testing the AWS Lambda function.  
4. **Recording 4** – Deploying and verifying infrastructure using Terraform.  

Each recording includes a narration of my thought process, the steps I took, and verification of functionality. This structure is intended to clearly show the implementation and reasoning for each part of the assignment.

---

## Part 1: Sumo Logic Query and Alert

**Objective:** Identify slow responses from the `/api/data` endpoint and trigger an alert.

**Implementation:**

- Filter logs for `/api/data`.
- Parse `responseTime`.
- Identify entries where `responseTime > 3000 ms`.
- Aggregate over 10-minute windows.
- Trigger alert if more than 5 slow responses are detected.

**Notes:** Replace `_sourceCategory` with your log source.  

**Recording:** `recordings/part1_sumo_logic.mp4`

---

## Part 2: AWS Lambda Function

**Objective:** Automate EC2 instance restart when Sumo Logic alert is triggered.

**Implementation:**

- Triggered by Sumo Logic alert.
- Restarts specified EC2 instance.
- Logs action.
- Sends notification to SNS topic.

**Deployment and Testing:** Lambda deployed via AWS Console / CLI and tested successfully.  

**Recording:** 'part3_lambda.mp4`

---

## Part 3: Infrastructure as Code (Terraform)

**Objective:** Deploy required infrastructure using Terraform.

**Implementation:**

- Deploy EC2 instance, Lambda function, and SNS topic.
- Optional: Configured with least privilege access.
- Verified deployment and Lambda functionality.

**Recording:** `part4_terraform.mp4`

---

## Submission Notes

- All files and recordings are publicly accessible in this repository.
- Each part demonstrates implementation, thought process, and verification.
- Solution follows best practices for monitoring, automation, and Infrastructure as Code.

