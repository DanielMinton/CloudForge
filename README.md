# CloudForge

Infrastructure-as-code visual builder with live AWS deployment capabilities.

## Overview

CloudForge is a drag-and-drop infrastructure designer that generates production-ready Terraform and CloudFormation templates. It provides visual feedback on your cloud architecture while handling the complexity of infrastructure configuration.

## Features

- **Visual Designer**: Drag-and-drop interface for building cloud architectures
- **Template Generation**: Auto-generates Terraform/CloudFormation from visual designs
- **Live Preview**: Real-time deployment previews before committing changes
- **Cost Estimation**: Projected monthly costs based on your infrastructure choices
- **Security Scanning**: Built-in checks for common security misconfigurations
- **Multi-Cloud Support**: Design for AWS, with extensible architecture

## Technical Stack

- **React** - Interactive canvas and UI components
- **Node.js** - Backend template generation service
- **AWS SDK** - Direct cloud resource management
- **Terraform** - Infrastructure-as-code output format
- **D3.js** - Network visualization and diagramming

## Architecture

```
┌──────────────────────────────────────────────┐
│              Visual Designer                  │
│  ┌────────┐  ┌────────┐  ┌────────┐         │
│  │ VPC    │──│  EC2   │──│  RDS   │         │
│  └────────┘  └────────┘  └────────┘         │
└──────────────────┬───────────────────────────┘
                   │
           ┌───────▼───────┐
           │   Generator   │
           └───────┬───────┘
                   │
    ┌──────────────┼──────────────┐
    ▼              ▼              ▼
┌────────┐   ┌──────────┐   ┌─────────┐
│Terraform│   │CloudForm │   │ Preview │
└────────┘   └──────────┘   └─────────┘
```

## Supported Resources

- **Compute**: EC2, Lambda, ECS, EKS
- **Storage**: S3, EBS, EFS
- **Database**: RDS, DynamoDB, ElastiCache
- **Networking**: VPC, Subnets, Security Groups, ALB
- **Integration**: API Gateway, SQS, SNS

## Demo

View the live demo at: https://danielminton.github.io/CloudForge/

## Local Development

```bash
npm install
npm run dev
```

## Author

Daniel Minton