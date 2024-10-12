
# Automate the Deployment of an Application using AWS CDK

## Prerequisites
- **Operating System**: Windows
- **Tools**:
  - [AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)
  - [Git](https://git-scm.com/downloads/win)
  - [Node.js](https://nodejs.org/en/download/prebuilt-installer/current)
  - [Python](https://www.python.org/downloads/)

## Steps

### 1. Install AWS CLI
- Install AWS CLI from the [official AWS documentation](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html).
- After installation, verify it by running:
  ```bash
  aws --version
  ```
- Add the path to the AWS CLI executable (e.g., `C:\Program Files\Amazon\AWSCLI\bin`) to your system's PATH.

### 2. Configure AWS CLI
- Run the following command to configure the CLI with your AWS account access and secret key:
  ```bash
  aws configure
  ```

### 3. Install AWS CDK
- Install the AWS CDK globally using npm:
  ```bash
  npm install -g aws-cdk
  ```
  > **Note**: You may need to install [Node.js](https://nodejs.org/en/download/prebuilt-installer/current) for npm to work.

### 4. Bootstrap Your AWS Environment
- Run the following command to bootstrap your AWS environment:
  ```bash
  cdk bootstrap aws://123456789012/us-east1
  ```

### 5. Create a New Directory for Your Web App
- Since CDK cannot run in a non-empty directory, create a new directory:
  ```bash
  mkdir my-web-app
  cd my-web-app
  ```

- Before continuing, ensure you have Git and Python installed and added to your system’s PATH:
  - [Git](https://git-scm.com/downloads/win)
  - [Python](https://www.python.org/downloads/)
  > **Note**: Both should be added to the PATH (e.g., `C:\Users\username\AppData\Local\Programs\Python\Python312`).

- Set up Git with your email and name:
  ```bash
  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"
  ```

### 6. Initialize the CDK Project with Python
- Initialize the CDK project to use Python:
  ```bash
  cdk init app --language python
  ```

- You'll receive a message saying: 
  > "Please run 'python -m venv .venv'!"

- To activate the virtual environment, run:
  ```bash
  .venv\Scripts\activate
  ```
  > **Note**: You’ll need to activate this virtual environment every time you work on the AWS CDK project.

- Install the required libraries inside the virtual environment:
  ```bash
  pip install -r requirements.txt
  ```

### 7. Deploying the CDK Stack
- Inside the virtual environment, run:
  ```bash
  cdk deploy
  ```
  This will deploy your infrastructure.

### 8. Verify Your Deployment
- Check your AWS account to verify the deployment.

---

This guide walks you through setting up and deploying an application using AWS CDK on a Windows system.
