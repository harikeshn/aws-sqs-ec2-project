# AWS SQS Asynchronous Message Processing using EC2 & IAM

## Overview
This project demonstrates an asynchronous, decoupled cloud architecture using Amazon SQS, EC2, and IAM.
A Node.js application sends and receives messages through an SQS queue.

## AWS Services Used
- Amazon SQS (Message Queue)
- Amazon EC2 (Compute)
- AWS IAM (Role-based access)
- Amazon Linux

## Architecture
Producer (Web App) → Amazon SQS → Consumer (EC2 Node.js App)

## What This Project Solves
Traditional systems fail when components are tightly coupled.
Using SQS, the producer and consumer work independently, improving reliability and scalability.

## Application Features
- Send messages to SQS
- Retrieve messages from SQS
- IAM Role based secure access (no access keys stored)

## Technologies Used
- Node.js
- Express.js
- AWS SDK
- EJS Templates

## Result
Messages are successfully sent to and retrieved from Amazon SQS using an EC2-hosted Node.js application.




SETUP AND RUN STEPS

1. Launch an EC2 instance (Amazon Linux)
2. Attach an IAM Role with SQS Full Access

3. Install Node.js
Run these commands:
curl -sL https://rpm.nodesource.com/setup_16.x | sudo bash -
sudo yum install -y nodejs

4. Install required packages
Run:
npm init -y
npm install express aws-sdk body-parser ejs

5. Start the application
Run:
node app.js

6. Open the application in browser
http://EC2-PUBLIC-IP:3000


SECURITY

- IAM Role is used instead of saving AWS keys in code
- Security Group allows port 3000

