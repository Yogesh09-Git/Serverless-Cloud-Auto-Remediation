# Serverless Cloud Auto-Remediation Platform

## Project Overview

This project is a serverless cloud auto-remediation platform that
monitors AWS resources and automatically performs predefined
remediation actions when an issue is detected.

## Infrastructure as Code

AWS CloudFormation is used to provision the required AWS resources.

## AWS Services Used

- Amazon EC2
- AWS Lambda
- Amazon CloudWatch
- Amazon EventBridge
- Amazon DynamoDB
- Amazon API Gateway
- Amazon S3
- AWS IAM

## Architecture

CloudFormation provisions the AWS infrastructure.

EC2 resource metrics are monitored using CloudWatch.
When a high CPU condition is detected, CloudWatch triggers
EventBridge, which invokes the remediation Lambda function.

The Lambda function performs the remediation action and stores
the incident information in DynamoDB.

API Gateway provides access to incident data for the dashboard,
which is hosted using Amazon S3.

## IaC Deployment

The infrastructure was deployed using AWS CloudFormation
in the `ap-southeast-1` (Singapore) AWS Region.

CloudFormation Stack:

`Auto-Remediation-IaC-Stack`

## Deployment Status

All resources in the CloudFormation stack successfully reached
`CREATE_COMPLETE` status.

## Repository Contents

- CloudFormation YAML template
- Architecture diagram
- AWS deployment screenshots
- Project documentation
