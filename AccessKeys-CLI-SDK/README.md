# Access Keys, CLI, SDK and CloudShell

## Accessing AWS

1. AWS Management Console (website): protected by password and MFA
2. AWS Command Line Interface (CLI): Protected by access keys
3. AWS Software Developer Kit (SDK) - for code: protected by access keys

## AWS CLI

- A tool that allows you to interact with AWS using commands in your command-line shell.

## AWS SDK

- Enables you to access and manage AWS services programmatically
- Embedded within your application.
- Supports many programming languages e.g. Java, Python

## Generating Access Keys

Users manage their own access keys

1. AWS
2. IAM
3. Click on the user you want to add the key to
4. Security Credentials
5. Create Access Key
6. Choose the type you want e.g. Command Line Interface
7. Create Access key

8. Within the terminal...
9. ```aws configure``` 
10. enter the access key details and region (you can skip the 'default outfut format').
11. ```aws iam list-users``` to check users (if you don't have admin permissions you will not see them)

## AWS CloudShell

![](../Images/cloudshell.png)

- Alternative to using a terminal.
- On the aws site.
- Only availible in some regions
- Can use aws commands
