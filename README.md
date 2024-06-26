
#  Portfolio Hosting on AWS EC2 instance with CI/CD setup using Github Actions.

Established a infrastructure for a CI/CD pipeline and hosting a resume website. Beginning with an IAM user createion from the AWS root account, applied EC2 policies for operational control. This IAM user was configured on an Ubuntu 20.04 LTS server, equipped with Git secret keys for secure operations, including `EC2_SSH_KEY`, `HOST-DNS`, `USERNAME`, and `TARGET-DIR`. 

Additionally, implemented a GitHub Actions workflow with a bash-scripted YML file, facilitating automated deployment and updates. Concurrently, hosted a resume website powered by HTML, CSS, and JavaScript, ensuring seamless accessibility and functionality.

## FeaturesTechnologies used-

- Aws EC2 instance - hosting server.
- Github Actions - CI/CD pipelining.
- Github repository - files storage.
- Bash Scripting - for user login and deployment of code with instance.

## Running Tests

Following steps were used for the Deployment of the website:


### 1.IAM User Creation:

Created an IAM user in AWS from the root account. This user is typically used for programmatic access (like APIs and tools) rather than direct console access.

### 2.Applied Policies for EC2:

Attached policies to this IAM user that allow it to interact with AWS services, specifically EC2 (Elastic Compute Cloud). These policies define what actions the IAM user can perform, such as launching instances or managing security groups.

### 3.Configured User on Ubuntu 20.04 LTS Server:

Configured the IAM user credentials on an Ubuntu 20.04 LTS server. This likely involves setting up the AWS CLI (Command Line Interface) with the IAM user's access keys so that commands can be executed from this server to interact with AWS services.

### 4.Configured Git Secret Keys:

Setting up secret keys necessary for Git operations. 
These include:

### EC2_SSH_KEY:
 SSH private key used to authenticate with EC2 instances.
### HOST-DNS: 
DNS or IP address of the host where your application runs.
### USERNAME: 
Username for SSH authentication or application deployment.
### TARGET-DIR: 
Directory on the target server where your application will be deployed.

### 5.Pushed .github/workflows Directory:

Created and pushed a .github/workflows directory to your Git repository. This directory contains YAML files that define your GitHub Actions workflows.

### 6.Bash Scripted YML File:
Within .github/workflows, created a YML file that defines your CI/CD pipeline using GitHub Actions. 

This file contains:

Environment Variables: Including those you configured (like EC2_SSH_KEY, HOST-DNS, etc.) securely as GitHub secrets.

## GitHub Actions for CI/CD AWS Project:



#### (Workflow Definition): .github/workflows file defines how CI/CD pipeline behaves.
Host: Pushed the html,css,js file from github repository to the public ipv4 dns.



## CD (Continuous Deployment):
Deployment to AWS: Use the AWS CLI (configured with IAM user credentials) to deploy your application to EC2 instances or other AWS services.

## Conclusion:
This setup allows for automated deployment of the login to iam user as well as pushment of the code on ipv4 dns using GitHub Actions and AWS services, ensuring efficiency and reliability in CI/CD processes.
