### Identity and Access Managment

- IAM policies can be attached at different levels: groups, users (inline policies), and multiple groups.

- Users inherit policies from all groups they belong to, combining permissions.

- IAM policy structure includes version, ID, and statements with key elements: Sid, Effect, Principal, Action,Resource, and optional Condition.

- Understanding Effect, Principal, Action, and Resource is essential for managing AWS permissions effectively.

# How to acces AWS?

There are three ways to access AWS. The first one is AWS Managment Console. The second one is AWS CLI(Command Line Interface). The third and the last one is AWS SDK(Software Development Kit).

## What is CLI?

- A tool enables AWS on command line.

- Direct access to public API's on AWS.

## What is SDK?

- AWS Software Development kit.

- Supports languages such as; JavaScript, GO, .NET, Python, Node.js, PHP.

# Security on AWS

To make AWS secure and protected, the best way is to protect the root with the multifactor. There are three ways to use multifactor. 

1. AuthApp
2. Security Key
3. Hard ttop token

Note: It is important to have access to the whichever multifactor you have because if you cannot get access to the multifactor, you cannot get access to the AWS.

## AWS CloudShell
- AWS CloudShell provides a browser-based terminal for issuing commands against AWS.
- CloudShell is only available in certain regions, so users must check availability.
- Files created in CloudShell persist across sessions, and users can upload or download files as needed.
- CloudShell supports multiple tabs and split views for enhanced productivity.

## IAM Roles for Services
- IAM Roles allow AWS services to perform actions on your behalf by assigning permissions.
- IAM Roles function like users but are intended for AWS services, not physical people.
- EC2 Instances and other AWS services like Lambda Functions use IAM Roles to access AWS resources securely.
- Creating and assigning IAM Roles is essential for managing permissions for AWS services.