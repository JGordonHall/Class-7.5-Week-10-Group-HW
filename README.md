Class 7.5 Week 10 Group HW
```markdown

# Anti-Drunk Engineer VM Recovery Assignment

## Overview

This assignment has two main parts:

1. Create a troubleshooting runbook and support ticket for a broken GCP VM environment.
2. Build supporting GCP infrastructure with Terraform.

The broken environment is created by running the provided setup command. Do not inspect the script. The goal is to troubleshoot the deployed environment like a real-world outage, document the investigation, repair the issue, and create reusable documentation for future engineers.

---

## Broken Environment Setup

Run the following command to create the broken VM environment:

```bash
curl -s https://storage.googleapis.com/static-site-bucket-522479235074/broken-env-with-prechecks-v2.sh | bash
```

You will need:

* A properly configured GCP account
* `gcloud` configured
* Bash, Git Bash, or GCP Cloud Shell

The script includes preflight checks to confirm that `gcloud` is configured and that the environment is not already provisioned.

---

## Part 1: Runbook

Create a section called **Runbook**.

The runbook should document how to troubleshoot and repair a GCP VM that is no longer accessible as a public web server and cannot be reached through SSH.

The runbook should include:

* Initial symptoms
* Expected behavior
* Actual behavior
* Troubleshooting steps used
* Commands used
* GCP Console checks performed
* Methods that helped identify the issue
* Methods that were useful but did not directly solve the issue
* Root cause
* Repair steps
* Validation steps
* Notes for future engineers

The runbook should follow a typical runbook format and be written clearly enough that another engineer can use it to complete the same recovery.

---

## Part 2: Support Ticket

Create a support ticket that documents the outage.

The support ticket should include:

* What was happening when the VM was first observed
* What the VM was expected to do
* What was broken
* What troubleshooting was performed
* What the root cause was
* What repair was completed
* A reference to the runbook

The runbook can be referenced as the **Anti-Drunk Engineer Runbook**.

---

## Part 3: Runbook Testing

The runbook must be tested by at least one group member.

The tester should:

1. Create the broken environment in their own GCP account.
2. Follow the runbook without extra help.
3. Confirm whether the runbook worked.
4. Provide feedback.
5. Update the runbook if anything was unclear or missing.

Document who tested the runbook and what feedback was received.

---

## Part 4: Terraform Infrastructure

In a subdirectory called `terraform`, create GCP infrastructure using Terraform.

The Terraform portion should include:

* VPC
* Firewall rules
* VM template
* Health check
* Managed Instance Group
* Global Application Load Balancer using HTTP only, if completed

Terraform requirements:

* Follow normal Terraform best practices
* Include a `.gitignore`
* Use class settings
* Use variables where appropriate
* Use locals
* Use a `terraform.tfvars` file
* Use outputs

AI may not be used for the Terraform code. Using AI for the Terraform portion results in automatic failure.

---

## Documentation Expectations

The final repository should clearly document:

* The runbook
* The support ticket
* The troubleshooting process
* The root cause and fix
* The runbook testing results
* The Terraform infrastructure work
* Any issues encountered
* Any resources or documentation used

---

## Final Status Checklist

```text
Runbook completed:
Support ticket completed:
Runbook tested by group member:
Terraform directory created:
VPC created with Terraform:
Firewall rules created with Terraform:
VM template created with Terraform:
Health check created with Terraform:
MIG created with Terraform:
HTTP Load Balancer created with Terraform:
Outputs included:
tfvars file included:
Locals included:
.gitignore included:
```

```
```
