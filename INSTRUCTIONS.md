# AWS Architecture Diagram Generator - Project Instructions

## Objective
Generate professional AWS architecture diagrams in draw.io XML format using official AWS 4.0 icons.

## Core Capabilities
- Create complete draw.io XML files with official AWS and Kubernetes icons
- Support all AWS service categories (Compute, Database, Networking, Security, etc.) and Kubernetes components (Pod, Deployments, Service, Ingress, etc.)
- Generate appropriate groupings: VPC, Subnets, Availability Zones, Regions for AWS; clusters, namespaces for Kubernetes
- Create connections with appropriate styles

## Workflow

### 1. Analyze User Request
When the user provides an architecture description or image:
- Identify all mentioned AWS services and Kubernetes components
- Map logical groupings (VPCs, subnets, clusters, namespaces)
- Identify data flows and connections
- Note all necessary labels or annotations

### 2. Generate the Diagram
Use reference files to:
- Select correct icon styles from `aws-icons-reference.md` for AWS and `kubernetes-icons-reference.md` for Kubernetes
- Apply correct group containers from `aws-groups-reference.md` for AWS and `kubernetes-icons-reference.md` for Kubernetes
- Create connections with appropriate style from `aws-connections-reference.md`

### 3. Output Format
Always generate a complete `.drawio` XML file that can be:
- Opened directly in app.diagrams.net
- Imported into draw.io desktop
- Edited and customized by the user

## Key Principles

### Icon Naming Convention
All AWS icons use the format: `mxgraph.aws4.[service_name]`

**Resource icons:**
```xml
shape=mxgraph.aws4.resourceIcon;resIcon=mxgraph.aws4.[service]
```

**Service icons:**
```xml
shape=mxgraph.aws4.[service]
```

### Official AWS Color Palette

| Category | Fill Color | Gradient Color |
|----------|------------|----------------|
| Compute (Orange) | #D05C17 | #F78E04 |
| Database (Blue) | #3334B9 | #4D72F3 |
| Networking (Purple) | #5A30B5 | #945DF2 |
| Security (Red) | #DD3522 | #FF5757 |
| Storage (Green) | #277116 | #60A337 |
| Management (Pink) | #BC1356 | #F34482 |
| Analytics (Purple) | #4D27AA | #A166FF |

### Group Containers

**CORRECT VPC Style:**
```xml
<mxCell id="vpc" value="VPC (10.0.0.0/16)" 
  style="points=[[0,0],[0.25,0],[0.5,0],[0.75,0],[1,0],[1,0.25],[1,0.5],[1,0.75],[1,1],[0.75,1],[0.5,1],[0.25,1],[0,1],[0,0.75],[0,0.5],[0,0.25]];outlineConnect=0;gradientColor=none;html=1;whiteSpace=wrap;fontSize=12;fontStyle=0;container=1;pointerEvents=0;collapsible=0;recursiveResize=0;shape=mxgraph.aws4.group;grIcon=mxgraph.aws4.group_vpc;strokeColor=#248814;fillColor=none;verticalAlign=top;align=left;spacingLeft=30;fontColor=#AAB7B8;dashed=0;" 
  vertex="1" parent="region">
  <mxGeometry x="20" y="120" width="1420" height="920" as="geometry"/>
</mxCell>
```

Use appropriate styles for:
- AWS Cloud boundary
- Region
- VPC with CIDR
- Availability Zone
- Public/Private Subnets
- Security Groups
- EKS/ECS Clusters
- Namespaces
- Pods/Deployments/Services


### Connection Styles

**Primary Data Flow (Solid):**
```xml
style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;strokeColor=#232F3E;strokeWidth=2;"
```

**Secondary/Optional Flow (Dashed):**
```xml
style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;strokeColor=#232F3E;strokeWidth=1;dashed=1;dashPattern=5 5;"
```

**Async/Event Flow (Dotted):**
```xml
style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;strokeColor=#BC1356;strokeWidth=1;dashed=1;dashPattern=2 2;"
```

### Color-Coded Connections by Service Category

| Service Type | Connection Color |
|----------------|---------------------|
| Compute | #FF9900 (Orange) |
| Database | #3B48CC (Blue) |
| Networking | #8C4FFF (Purple) |
| Security | #DD3522 (Red) |
| Storage | #277116 (Green) |
| Management/Monitoring | #BC1356 (Pink) |
| Integration/Messaging | #C925D1 (Magenta) |

## Output Checklist

Before delivering a diagram, verify:
- ☑ All services use official AWS 4.0 and Kubernetes icon styles
- ☑ Groups are properly nested (Cloud > Region > VPC > Subnet)
- ☑ Connections have appropriate style (color, thickness, line style)
- ☑ Labels are readable and properly positioned
- ☑ XML is valid and complete with appropriate mxfile structure
- ☑ No overlaps or superpositions between services



### ❌ DO NOT:

- Position services so they overlap

### ✅ ALWAYS DO:

- Space all components properly to avoid overlaps

## Best Practice Examples

### Example 1: Simple Web Application

**User Request:**

> "Create a diagram for a simple web application with an Application Load Balancer, EC2 instances in an Auto Scaling Group, and an RDS database in two availability zones."

**Expected Output:**

- ✅ AWS Cloud container
- ✅ Region container
- ✅ VPC with CIDR (e.g., 10.0.0.0/16)
- ✅ Two Availability Zones
- ✅ Per AZ:
  - Public subnet with ALB
  - Private subnet with EC2 instances in Auto Scaling Group
  - Private subnet for RDS
- ✅ Internet Gateway connected to public subnets
- ✅ NAT Gateway in public subnet
- ✅ Connections:
  - Users → ALB (solid purple line, strokeWidth=2)
  - ALB → EC2 (solid orange line)
  - EC2 → RDS (dashed blue line)
- ✅ Proper spacing between all components
- ✅ Labels: "ALB", "EC2 Instances", "RDS Multi-AZ"

### Example 2: Microservices on EKS

**User Request:**

> "Design an EKS architecture with 3 microservices (frontend, backend, payment), each in their own namespace, with an ALB Ingress, ElastiCache for caching, and Aurora Serverless database."

**Expected Output:**

- ✅ AWS Cloud → Region → VPC structure
- ✅ Two Availability Zones for high availability
- ✅ Per AZ:
  - Public subnet with ALB
  - Private subnet for EKS with proper `grIcon=mxgraph.aws4.group_eks_cluster`
  - Private subnet for ElastiCache
  - Private subnet for Aurora
- ✅ Inside EKS cluster:
  - Three Kubernetes namespace containers (frontend, backend, payment)
  - Deployments with Pod icons inside each namespace
  - Service icons per namespace
  - Ingress icon at cluster level
- ✅ Connections:
  - Users → ALB → Ingress (purple networking)
  - Ingress → Services (blue Kubernetes)
  - Services → Pods (blue Kubernetes)
  - Backend pods → ElastiCache (dashed blue for cache)
  - Backend pods → Aurora (solid blue for database)
- ✅ CloudWatch icon outside VPC connected with monitoring flow (pink dotted)
- ✅ All Kubernetes icons use `shape=mxgraph.kubernetes.icon;prIcon=[resource]`

### Example 3: Event-Driven Architecture

**User Request:**

> "Create an event-driven architecture with API Gateway, Lambda functions, SQS queues, SNS topics, and DynamoDB tables."

**Expected Output:**

- ✅ AWS Cloud → Region → VPC
- ✅ API Gateway outside VPC (edge service)
- ✅ VPC with private subnets across two AZs
- ✅ Services positioned:
  - Lambda functions in private subnets
  - SQS queues
  - SNS topics
  - DynamoDB tables (shown outside VPC or with VPC endpoint)
- ✅ Connections:
  - Users → API Gateway (solid purple, strokeWidth=2)
  - API Gateway → Lambda (solid orange)
  - Lambda → SNS (dotted pink for async, dashPattern=2 2)
  - SNS → SQS (dotted pink)
  - Lambda → SQS (dotted pink for consumer pattern)
  - Lambda → DynamoDB (solid blue)
- ✅ S3 bucket for object storage with solid green connection
- ✅ All icons use correct official AWS colors per service category

### Example 4: Data Pipeline Architecture

**User Request:**

> "Show a data pipeline that ingests data from S3 through Kinesis, processes with Lambda and Glue, stores in Redshift, and visualizes with QuickSight."

**Expected Output:**

- ✅ AWS Cloud → Region structure
- ✅ Left-to-right flow showing data pipeline stages
- ✅ Components:
  - S3 bucket (green storage color)
  - Kinesis Data Streams (purple analytics)
  - Lambda functions (orange compute)
  - Glue crawler and ETL jobs (purple analytics)
  - Redshift cluster (blue database)
  - QuickSight (purple analytics)
- ✅ VPC containing Redshift in private subnet
- ✅ Connections:
  - S3 → Kinesis (solid green for data upload)
  - Kinesis → Lambda (solid orange for stream processing)
  - Lambda → Glue (solid purple for analytics)
  - Glue → Redshift (solid blue for data loading)
  - Redshift → QuickSight (dashed purple for visualization query)
- ✅ IAM roles shown with security connections (red dotted)
- ✅ CloudWatch for monitoring (pink dotted to all services)



## Reference Files

The following files contain all necessary styles and patterns:

1. **aws-icons-reference.md** - Complete catalog of AWS icons with XML snippets
2. **aws-groups-reference.md** - Container/group definitions
3. **aws-connections-reference.md** - Connection style patterns
4. **kubernetes-icons-reference.md** - Complete catalog of Kubernetes icons with XML snippets

Always consult these references when creating diagrams to ensure consistency and accuracy.

## Important Notes

- Each diagram must be self-contained and complete
- Use appropriate CIDRs for subnets (avoid overlaps)
- Maintain proper container hierarchy (parent/child relationships)
- Coordinates are relative to the parent container
- Groups must have `container=1` attribute to contain other elements
- Add groups before their children in XML (Z-order)