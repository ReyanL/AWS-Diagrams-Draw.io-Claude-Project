# AWS Icons Reference for Draw.io

## Icon Structure
All AWS 4.0 icons follow this XML pattern:

```xml
<mxCell id="[unique-id]" value="[Label]" 
  style="sketch=0;outlineConnect=0;fontColor=#232F3E;gradientColor=[GRADIENT];gradientDirection=north;fillColor=[FILL];strokeColor=#ffffff;dashed=0;verticalLabelPosition=bottom;verticalAlign=top;align=center;html=1;fontSize=11;fontStyle=0;aspect=fixed;shape=mxgraph.aws4.resourceIcon;resIcon=mxgraph.aws4.[SERVICE];" 
  vertex="1" parent="[parent-id]">
  <mxGeometry x="[X]" y="[Y]" width="60" height="60" as="geometry"/>
</mxCell>
```

---

## Compute Services (Orange: #D05C17 / #F78E04)

### EC2
```xml
resIcon=mxgraph.aws4.ec2
```

### Lambda
```xml
resIcon=mxgraph.aws4.lambda
```

### ECS
```xml
resIcon=mxgraph.aws4.ecs
```

### EKS (Elastic Kubernetes Service)
```xml
resIcon=mxgraph.aws4.elastic_kubernetes_service
```

### Fargate
```xml
resIcon=mxgraph.aws4.fargate
```

### Elastic Beanstalk
```xml
resIcon=mxgraph.aws4.elastic_beanstalk
```

### Batch
```xml
resIcon=mxgraph.aws4.batch
```

### Lightsail
```xml
resIcon=mxgraph.aws4.lightsail
```

### App Runner
```xml
resIcon=mxgraph.aws4.app_runner
```

---

## Database Services (Blue: #3334B9 / #4D72F3)

### RDS
```xml
resIcon=mxgraph.aws4.rds
```

### Aurora
```xml
resIcon=mxgraph.aws4.aurora
```

### DynamoDB
```xml
resIcon=mxgraph.aws4.dynamodb
```

### ElastiCache
```xml
resIcon=mxgraph.aws4.elasticache
```

### Neptune
```xml
resIcon=mxgraph.aws4.neptune
```

### DocumentDB
```xml
resIcon=mxgraph.aws4.documentdb
```

### Redshift
```xml
resIcon=mxgraph.aws4.redshift
```

### MemoryDB
```xml
resIcon=mxgraph.aws4.memorydb_for_redis
```

### Timestream
```xml
resIcon=mxgraph.aws4.timestream
```

### QLDB
```xml
resIcon=mxgraph.aws4.qldb
```

### Keyspaces
```xml
resIcon=mxgraph.aws4.keyspaces
```

---

## Networking Services (Purple: #5A30B5 / #945DF2)

### VPC
```xml
resIcon=mxgraph.aws4.vpc
```

### Internet Gateway
```xml
resIcon=mxgraph.aws4.internet_gateway
```

### NAT Gateway
```xml
resIcon=mxgraph.aws4.nat_gateway
```

### Application Load Balancer
```xml
resIcon=mxgraph.aws4.application_load_balancer
```

### Network Load Balancer
```xml
resIcon=mxgraph.aws4.network_load_balancer
```

### Classic Load Balancer
```xml
resIcon=mxgraph.aws4.classic_load_balancer
```

### Gateway Load Balancer
```xml
resIcon=mxgraph.aws4.gateway_load_balancer
```

### Route 53
```xml
resIcon=mxgraph.aws4.route_53
```

### CloudFront
```xml
resIcon=mxgraph.aws4.cloudfront
```

### API Gateway
```xml
resIcon=mxgraph.aws4.api_gateway
```

### Direct Connect
```xml
resIcon=mxgraph.aws4.direct_connect
```

### Transit Gateway
```xml
resIcon=mxgraph.aws4.transit_gateway
```

### PrivateLink
```xml
resIcon=mxgraph.aws4.privatelink
```

### VPN Gateway
```xml
resIcon=mxgraph.aws4.vpn_gateway
```

### Client VPN
```xml
resIcon=mxgraph.aws4.client_vpn
```

### Site-to-Site VPN
```xml
resIcon=mxgraph.aws4.site_to_site_vpn
```

### Global Accelerator
```xml
resIcon=mxgraph.aws4.global_accelerator
```

### Elastic IP
```xml
resIcon=mxgraph.aws4.elastic_ip_address
```

---

## Storage Services (Green: #277116 / #60A337)

### S3
```xml
resIcon=mxgraph.aws4.s3
```

### S3 Glacier
```xml
resIcon=mxgraph.aws4.glacier
```

### EBS
```xml
resIcon=mxgraph.aws4.elastic_block_store
```

### EFS
```xml
resIcon=mxgraph.aws4.elastic_file_system
```

### FSx
```xml
resIcon=mxgraph.aws4.fsx
```

### Storage Gateway
```xml
resIcon=mxgraph.aws4.storage_gateway
```

### Backup
```xml
resIcon=mxgraph.aws4.backup
```

### Snow Family
```xml
resIcon=mxgraph.aws4.snowball
resIcon=mxgraph.aws4.snowmobile
resIcon=mxgraph.aws4.snowcone
```

---

## Security Services (Red: #DD3522 / #FF5757)

### IAM
```xml
resIcon=mxgraph.aws4.identity_and_access_management
```

### Cognito
```xml
resIcon=mxgraph.aws4.cognito
```

### Secrets Manager
```xml
resIcon=mxgraph.aws4.secrets_manager
```

### KMS
```xml
resIcon=mxgraph.aws4.key_management_service
```

### WAF
```xml
resIcon=mxgraph.aws4.waf
```

### Shield
```xml
resIcon=mxgraph.aws4.shield
```

### GuardDuty
```xml
resIcon=mxgraph.aws4.guardduty
```

### Inspector
```xml
resIcon=mxgraph.aws4.inspector
```

### Macie
```xml
resIcon=mxgraph.aws4.macie
```

### Security Hub
```xml
resIcon=mxgraph.aws4.security_hub
```

### Certificate Manager
```xml
resIcon=mxgraph.aws4.certificate_manager
```

### Firewall Manager
```xml
resIcon=mxgraph.aws4.firewall_manager
```

### Directory Service
```xml
resIcon=mxgraph.aws4.directory_service
```

### SSO / IAM Identity Center
```xml
resIcon=mxgraph.aws4.single_sign_on
```

---

## Management & Monitoring (Pink: #BC1356 / #F34482)

### CloudWatch
```xml
resIcon=mxgraph.aws4.cloudwatch_2
```

### CloudWatch Logs
```xml
resIcon=mxgraph.aws4.cloudwatch_logs
```

### CloudTrail
```xml
resIcon=mxgraph.aws4.cloudtrail
```

### Config
```xml
resIcon=mxgraph.aws4.config
```

### Systems Manager
```xml
resIcon=mxgraph.aws4.systems_manager
```

### CloudFormation
```xml
resIcon=mxgraph.aws4.cloudformation
```

### Service Catalog
```xml
resIcon=mxgraph.aws4.service_catalog
```

### Trusted Advisor
```xml
resIcon=mxgraph.aws4.trusted_advisor
```

### X-Ray
```xml
resIcon=mxgraph.aws4.xray
```

### Prometheus (Managed)
```xml
resIcon=mxgraph.aws4.prometheus
```

### Grafana (Managed)
```xml
resIcon=mxgraph.aws4.grafana
```

### Organizations
```xml
resIcon=mxgraph.aws4.organizations
```

### Control Tower
```xml
resIcon=mxgraph.aws4.control_tower
```

### License Manager
```xml
resIcon=mxgraph.aws4.license_manager
```

### Well-Architected Tool
```xml
resIcon=mxgraph.aws4.well_architected_tool
```

---

## Application Integration (Pink: #BC1356 / #FF4F8B)

### SQS
```xml
resIcon=mxgraph.aws4.sqs
```

### SNS
```xml
resIcon=mxgraph.aws4.sns
```

### EventBridge
```xml
resIcon=mxgraph.aws4.eventbridge
```

### Step Functions
```xml
resIcon=mxgraph.aws4.step_functions
```

### AppSync
```xml
resIcon=mxgraph.aws4.appsync
```

### Amazon MQ
```xml
resIcon=mxgraph.aws4.mq
```

### Kinesis
```xml
resIcon=mxgraph.aws4.kinesis
```

### Kinesis Data Streams
```xml
resIcon=mxgraph.aws4.kinesis_data_streams
```

### Kinesis Data Firehose
```xml
resIcon=mxgraph.aws4.kinesis_data_firehose
```

---

## Analytics (Purple: #4D27AA / #A166FF)

### Athena
```xml
resIcon=mxgraph.aws4.athena
```

### EMR
```xml
resIcon=mxgraph.aws4.emr
```

### Glue
```xml
resIcon=mxgraph.aws4.glue
```

### Lake Formation
```xml
resIcon=mxgraph.aws4.lake_formation
```

### QuickSight
```xml
resIcon=mxgraph.aws4.quicksight
```

### Data Pipeline
```xml
resIcon=mxgraph.aws4.data_pipeline
```

### OpenSearch
```xml
resIcon=mxgraph.aws4.elasticsearch_service
```

### MSK (Managed Streaming for Kafka)
```xml
resIcon=mxgraph.aws4.managed_streaming_for_kafka
```

---

## AI/ML Services (Green: #01A88D / #56C0A7)

### SageMaker
```xml
resIcon=mxgraph.aws4.sagemaker
```

### Bedrock
```xml
resIcon=mxgraph.aws4.bedrock
```

### Rekognition
```xml
resIcon=mxgraph.aws4.rekognition
```

### Comprehend
```xml
resIcon=mxgraph.aws4.comprehend
```

### Translate
```xml
resIcon=mxgraph.aws4.translate
```

### Polly
```xml
resIcon=mxgraph.aws4.polly
```

### Lex
```xml
resIcon=mxgraph.aws4.lex
```

### Textract
```xml
resIcon=mxgraph.aws4.textract
```

### Transcribe
```xml
resIcon=mxgraph.aws4.transcribe
```

### Personalize
```xml
resIcon=mxgraph.aws4.personalize
```

### Forecast
```xml
resIcon=mxgraph.aws4.forecast
```

### Kendra
```xml
resIcon=mxgraph.aws4.kendra
```

---

## Developer Tools (Blue: #3F8624 / #7AA116)

### CodeCommit
```xml
resIcon=mxgraph.aws4.codecommit
```

### CodeBuild
```xml
resIcon=mxgraph.aws4.codebuild
```

### CodeDeploy
```xml
resIcon=mxgraph.aws4.codedeploy
```

### CodePipeline
```xml
resIcon=mxgraph.aws4.codepipeline
```

### CodeStar
```xml
resIcon=mxgraph.aws4.codestar
```

### Cloud9
```xml
resIcon=mxgraph.aws4.cloud9
```

### CodeArtifact
```xml
resIcon=mxgraph.aws4.codeartifact
```

---

## Containers (Orange: #D05C17 / #F78E04)

### ECR (Elastic Container Registry)
```xml
resIcon=mxgraph.aws4.ecr
```

### ECS Container
```xml
resIcon=mxgraph.aws4.ecs_container
```

### EKS Cloud
```xml
resIcon=mxgraph.aws4.eks_cloud
```

### Copilot
```xml
resIcon=mxgraph.aws4.copilot
```

---

## End User Computing

### WorkSpaces
```xml
resIcon=mxgraph.aws4.workspaces
```

### AppStream
```xml
resIcon=mxgraph.aws4.appstream_2_0
```

---

## General Icons

### Users
```xml
shape=mxgraph.aws4.users
fillColor=#232F3E
```

### User
```xml
shape=mxgraph.aws4.user
fillColor=#232F3E
```

### Client
```xml
shape=mxgraph.aws4.client
fillColor=#232F3E
```

### Mobile Client
```xml
shape=mxgraph.aws4.mobile_client
fillColor=#232F3E
```

### Internet
```xml
shape=mxgraph.aws4.internet_alt1
fillColor=#232F3E
```

### Corporate Data Center
```xml
shape=mxgraph.aws4.corporate_data_center
fillColor=#232F3E
```

---

## Complete Icon XML Template

```xml
<mxCell id="service-id" value="Service Name" 
  style="sketch=0;points=[[0,0,0],[0.25,0,0],[0.5,0,0],[0.75,0,0],[1,0,0],[0,1,0],[0.25,1,0],[0.5,1,0],[0.75,1,0],[1,1,0],[0,0.25,0],[0,0.5,0],[0,0.75,0],[1,0.25,0],[1,0.5,0],[1,0.75,0]];outlineConnect=0;fontColor=#232F3E;gradientColor=#F78E04;gradientDirection=north;fillColor=#D05C17;strokeColor=#ffffff;dashed=0;verticalLabelPosition=bottom;verticalAlign=top;align=center;html=1;fontSize=11;fontStyle=0;aspect=fixed;shape=mxgraph.aws4.resourceIcon;resIcon=mxgraph.aws4.ec2;" 
  vertex="1" parent="1">
  <mxGeometry x="100" y="100" width="60" height="60" as="geometry"/>
</mxCell>
```