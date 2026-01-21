# AWS Diagrams Draw.io Generator - Claude Project

A comprehensive Claude Desktop project that enables AI-assisted generation of professional AWS and Kubernetes architecture diagrams in draw.io XML format. This project provides Claude with detailed references, instructions, and examples to architecture diagrams from natural language descriptions or images.

## Overview

This project transforms Claude Desktop into a specialized AWS architecture diagram generator. By providing Claude with comprehensive reference materials and structured instructions, you can:

- **Generate diagrams from text descriptions**: Describe your AWS architecture in natural language, and Claude will create a complete draw.io XML file
- **Generate diagrams from images**: Upload an existing architecture diagram, and Claude can recreate or improve it using official AWS icons
- **Use official AWS 4.0 icons**: All diagrams use the official AWS icon set with correct colors and styles
- **Support Kubernetes components**: Generate EKS architectures with proper Kubernetes icons (Pods, Services, Deployments, Ingress, etc.)
- **Proper grouping and connections**: Automatically creates VPCs, subnets, availability zones, and appropriate connection styles

## Project Structure

```
AWS-Diagrams-Draw.io-Claude-Project/
├── README.md                          # This documentation
├── INSTRUCTIONS.md                    # Main instructions for Claude
├── hello-world.drawio                 # Example diagram for quick testing
├── aws-icons-reference.md            # Complete AWS icon catalog with XML snippets
├── aws-groups-reference.md            # Container/group definitions (VPC, Subnets, etc.)
├── aws-connections-reference.md      # Connection style patterns
└── kubernetes-icons-reference.md      # Kubernetes icon catalog
```

### File Descriptions

- **`INSTRUCTIONS.md`**: Core instructions that guide Claude on how to generate diagrams, including icon conventions, color palettes, grouping rules, and best practices
- **`hello-world.drawio`**: Example diagram demonstrating a simple web application architecture (ALB, EC2 instances, VPC structure)
- **`aws-icons-reference.md`**: Comprehensive catalog of all AWS 4.0 service icons with XML code snippets for each service category
- **`aws-groups-reference.md`**: Reference for creating proper container groups (AWS Cloud, Regions, VPCs, Subnets, Availability Zones)
- **`aws-connections-reference.md`**: Patterns for creating connections between services with appropriate colors and line styles
- **`kubernetes-icons-reference.md`**: Complete reference for Kubernetes components (Pods, Deployments, Services, Ingress, Namespaces, etc.)

## Features

### Supported AWS Services

- **Compute**: EC2, Lambda, ECS, EKS, Fargate, Elastic Beanstalk, Batch
- **Database**: RDS, Aurora, DynamoDB, ElastiCache, DocumentDB, Neptune, Redshift
- **Networking**: VPC, Subnets, ALB, NLB, CloudFront, API Gateway, Route 53, Direct Connect
- **Storage**: S3, EBS, EFS, FSx, Storage Gateway
- **Security**: IAM, Secrets Manager, KMS, WAF, Shield, GuardDuty
- **Management**: CloudWatch, CloudFormation, Systems Manager, CloudTrail
- **Analytics**: Kinesis, EMR, Glue, Athena, QuickSight, Data Pipeline
- **And many more...**

### Supported Kubernetes Components

- Pods, Deployments, Services, Ingress
- Namespaces, ConfigMaps, Secrets
- StatefulSets, DaemonSets, Jobs
- PersistentVolumes, PersistentVolumeClaims


## Setup Instructions for Claude Desktop

Follow these steps to configure this project in Claude Desktop:

### Install Claude Desktop

If you haven't already, download and install Claude Desktop from [Anthropic's website](https://claude.com/download).

### Configure Claude Desktop to Use the Project

1. Open Claude Desktop
2. Click on the **Projects** icon in the sidebar
3. Click on the **New Project** button
4. Give a name to the project and describe the project in the description field.
5. Copy the INSTRUCTIONS.md content to the project instructions field.
6. Copy the reference files content to the project reference files field.

## Usage Guide

### Quick Start: Test with Example Diagram

To quickly verify that everything is set up correctly:

1. Open the included `hello-world.drawio` file in [app.diagrams.net](https://app.diagrams.net) or draw.io desktop
2. This example demonstrates:
   - AWS Cloud → Region → VPC hierarchy
   - Two Availability Zones (us-east-1a and us-east-1b)
   - Public and Private Subnets with proper CIDR notation
   - Application Load Balancer and EC2 instances
   - Internet Gateway and proper connections
   - Official AWS 4.0 icons with correct colors

This file serves as a reference for the expected output format and can help you verify that your draw.io installation supports AWS 4.0 icons correctly.

### Basic Usage: Text Description

Simply describe your architecture in natural language:

```
Create a diagram for a simple web application with an Application Load Balancer, 
EC2 instances in an Auto Scaling Group, and an RDS database in two availability zones.
```

Claude will generate a complete `.drawio` XML file that you can:
- Save with a `.drawio` extension
- Open directly in [app.diagrams.net](https://app.diagrams.net)
- Import into draw.io desktop application
- Edit and customize as needed

### Advanced Usage: Image Input

1. Upload an existing architecture diagram image
2. Ask Claude to recreate it using official AWS icons:
   ```
   Recreate this architecture diagram using official AWS 4.0 icons and proper 
   grouping (VPC, subnets, availability zones).
   ```

### Example Requests

#### Simple Web Application
```
Create a diagram for a simple web application with an Application Load Balancer, 
EC2 instances in an Auto Scaling Group, and an RDS database in two availability zones.
```

#### Microservices on EKS
```
Design an EKS architecture with 3 microservices (frontend, backend, payment), 
each in their own namespace, with an ALB Ingress, ElastiCache for caching, 
and Aurora Serverless database.
```

#### Event-Driven Architecture
```
Create an event-driven architecture with API Gateway, Lambda functions, SQS queues, 
SNS topics, and DynamoDB tables.
```

#### Data Pipeline
```
Show a data pipeline that ingests data from S3 through Kinesis, processes with 
Lambda and Glue, stores in Redshift, and visualizes with QuickSight.
```

## Output Format

All generated diagrams are complete draw.io XML files that include:

- ✅ Proper XML structure with `<mxfile>` root element
- ✅ Official AWS 4.0 icons with correct colors
- ✅ Proper container hierarchy (Cloud → Region → VPC → Subnet)
- ✅ Appropriate connection styles (solid, dashed, dotted)
- ✅ Color-coded connections by service category
- ✅ Proper spacing and layout
- ✅ Readable labels and annotations

## Key Features Explained

### Official AWS Color Palette

The project uses the official AWS color scheme:

| Category | Fill Color | Gradient Color |
|----------|------------|----------------|
| Compute (Orange) | #D05C17 | #F78E04 |
| Database (Blue) | #3334B9 | #4D72F3 |
| Networking (Purple) | #5A30B5 | #945DF2 |
| Security (Red) | #DD3522 | #FF5757 |
| Storage (Green) | #277116 | #60A337 |
| Management (Pink) | #BC1356 | #F34482 |
| Analytics (Purple) | #4D27AA | #A166FF |

### Connection Styles

- **Primary Data Flow**: Solid lines, strokeWidth=2
- **Secondary/Optional Flow**: Dashed lines (dashPattern=5 5)
- **Async/Event Flow**: Dotted lines (dashPattern=2 2) in pink
- **Color Coding**: Connections use service category colors

### Group Containers

Properly nested containers:
- AWS Cloud boundary
- Region containers
- VPC with CIDR notation
- Availability Zones
- Public/Private Subnets
- EKS/ECS Clusters
- Kubernetes Namespaces

## Troubleshooting

### Claude Doesn't Recognize the Project

1. Ensure all files are in the project directory
2. Restart Claude Desktop
3. Verify the project is selected in the Projects sidebar

### Generated Diagrams Have Errors

1. Check that Claude has access to all reference files
2. Verify the request is clear and specific
3. Ask Claude to review the reference files if needed

### Icons Not Displaying Correctly

1. Ensure you're using draw.io version that supports AWS 4.0 icons
2. Open diagrams in [app.diagrams.net](https://app.diagrams.net) for best compatibility
3. Verify the XML structure is valid

## Best Practices

1. **Be Specific**: Provide clear descriptions of your architecture
2. **Mention Requirements**: Specify multi-AZ, high availability, or specific AWS services
3. **Request Revisions**: Ask Claude to adjust spacing, colors, or layout as needed
4. **Iterate**: Start with a simple diagram and add complexity incrementally

## License

This project is provided as-is for use with Claude Desktop. The AWS icons and draw.io are property of their respective owners.

## Resources

- [Draw.io / Diagrams.net](https://app.diagrams.net)
- [AWS Architecture Icons](https://aws.amazon.com/architecture/icons/)
- [Claude Desktop Documentation](https://claude.ai/docs)

## Support

For issues or questions:
1. Check the reference files for icon names and patterns
2. Review the examples in `INSTRUCTIONS.md`
3. Verify your Claude Desktop configuration

---

**Happy Diagramming! 🎨**
