# AWS Groups Reference for Draw.io

## Group Structure Overview

Groups in AWS diagrams are container elements that represent logical boundaries. They must be properly nested following AWS architecture conventions.

### Nesting Hierarchy (Outside â†’ Inside)
```
AWS Cloud
  â””â”€â”€ Region
        â””â”€â”€ VPC
              â”œâ”€â”€ Availability Zone
              â”‚     â”œâ”€â”€ Public Subnet
              â”‚     â””â”€â”€ Private Subnet
              â””â”€â”€ Security Group
                    â””â”€â”€ Auto Scaling Group / EKS Cluster / ECS Cluster
```

---

## AWS Cloud Container

The outermost boundary representing the AWS environment.

```xml
<mxCell id="aws-cloud" value="AWS Cloud" 
  style="points=[[0,0],[0.25,0],[0.5,0],[0.75,0],[1,0],[1,0.25],[1,0.5],[1,0.75],[1,1],[0.75,1],[0.5,1],[0.25,1],[0,1],[0,0.75],[0,0.5],[0,0.25]];outlineConnect=0;gradientColor=none;html=1;whiteSpace=wrap;fontSize=12;fontStyle=1;container=1;pointerEvents=0;collapsible=0;recursiveResize=0;shape=mxgraph.aws4.group;grIcon=mxgraph.aws4.group_aws_cloud;strokeColor=#232F3E;fillColor=none;verticalAlign=top;align=left;spacingLeft=30;fontColor=#232F3E;dashed=0;" 
  vertex="1" parent="1">
  <mxGeometry x="40" y="40" width="1200" height="800" as="geometry"/>
</mxCell>
```

---

## Region Container

```xml
<mxCell id="region" value="Region" 
  style="points=[[0,0],[0.25,0],[0.5,0],[0.75,0],[1,0],[1,0.25],[1,0.5],[1,0.75],[1,1],[0.75,1],[0.5,1],[0.25,1],[0,1],[0,0.75],[0,0.5],[0,0.25]];outlineConnect=0;gradientColor=none;html=1;whiteSpace=wrap;fontSize=12;fontStyle=1;container=1;pointerEvents=0;collapsible=0;recursiveResize=0;shape=mxgraph.aws4.group;grIcon=mxgraph.aws4.group_region;strokeColor=#00A4A6;fillColor=none;verticalAlign=top;align=left;spacingLeft=30;fontColor=#147EBA;dashed=1;" 
  vertex="1" parent="aws-cloud">
  <mxGeometry x="20" y="40" width="1160" height="740" as="geometry"/>
</mxCell>
```

---

## VPC Container

```xml
<mxCell id="vpc" value="VPC (10.0.0.0/16)" 
  style="points=[[0,0],[0.25,0],[0.5,0],[0.75,0],[1,0],[1,0.25],[1,0.5],[1,0.75],[1,1],[0.75,1],[0.5,1],[0.25,1],[0,1],[0,0.75],[0,0.5],[0,0.25]];outlineConnect=0;gradientColor=none;html=1;whiteSpace=wrap;fontSize=12;fontStyle=1;container=1;pointerEvents=0;collapsible=0;recursiveResize=0;shape=mxgraph.aws4.group;grIcon=mxgraph.aws4.group_vpc2;strokeColor=#8C4FFF;fillColor=none;verticalAlign=top;align=left;spacingLeft=30;fontColor=#8C4FFF;dashed=0;" 
  vertex="1" parent="region">
  <mxGeometry x="20" y="40" width="1100" height="680" as="geometry"/>
</mxCell>
```

---

## Availability Zone

```xml
<mxCell id="az-1" value="Availability Zone 1" 
  style="fillColor=none;strokeColor=#147EBA;dashed=1;verticalAlign=top;fontStyle=1;fontColor=#147EBA;whiteSpace=wrap;html=1;fontSize=12;container=1;pointerEvents=0;collapsible=0;recursiveResize=0;" 
  vertex="1" parent="vpc">
  <mxGeometry x="20" y="40" width="520" height="600" as="geometry"/>
</mxCell>
```

---

## Public Subnet

```xml
<mxCell id="public-subnet" value="Public Subnet" 
  style="points=[[0,0],[0.25,0],[0.5,0],[0.75,0],[1,0],[1,0.25],[1,0.5],[1,0.75],[1,1],[0.75,1],[0.5,1],[0.25,1],[0,1],[0,0.75],[0,0.5],[0,0.25]];outlineConnect=0;gradientColor=none;html=1;whiteSpace=wrap;fontSize=12;fontStyle=1;container=1;pointerEvents=0;collapsible=0;recursiveResize=0;shape=mxgraph.aws4.group;grIcon=mxgraph.aws4.group_security_group;strokeColor=#7AA116;fillColor=#F2F6E8;verticalAlign=top;align=left;spacingLeft=30;fontColor=#248814;dashed=0;" 
  vertex="1" parent="az-1">
  <mxGeometry x="20" y="40" width="480" height="200" as="geometry"/>
</mxCell>
```

---

## Private Subnet

```xml
<mxCell id="private-subnet" value="Private Subnet" 
  style="points=[[0,0],[0.25,0],[0.5,0],[0.75,0],[1,0],[1,0.25],[1,0.5],[1,0.75],[1,1],[0.75,1],[0.5,1],[0.25,1],[0,1],[0,0.75],[0,0.5],[0,0.25]];outlineConnect=0;gradientColor=none;html=1;whiteSpace=wrap;fontSize=12;fontStyle=1;container=1;pointerEvents=0;collapsible=0;recursiveResize=0;shape=mxgraph.aws4.group;grIcon=mxgraph.aws4.group_security_group;strokeColor=#147EBA;fillColor=#E6F2F8;verticalAlign=top;align=left;spacingLeft=30;fontColor=#147EBA;dashed=0;" 
  vertex="1" parent="az-1">
  <mxGeometry x="20" y="260" width="480" height="320" as="geometry"/>
</mxCell>
```

---

## Security Group

```xml
<mxCell id="security-group" value="Security Group" 
  style="fillColor=none;strokeColor=#DD3522;verticalAlign=top;fontStyle=1;fontColor=#DD3522;whiteSpace=wrap;html=1;fontSize=12;container=1;pointerEvents=0;collapsible=0;recursiveResize=0;dashed=1;" 
  vertex="1" parent="private-subnet">
  <mxGeometry x="20" y="40" width="440" height="260" as="geometry"/>
</mxCell>
```

---

## EKS Cluster

```xml
<mxCell id="eks-cluster" value="EKS Cluster" 
  style="points=[[0,0],[0.25,0],[0.5,0],[0.75,0],[1,0],[1,0.25],[1,0.5],[1,0.75],[1,1],[0.75,1],[0.5,1],[0.25,1],[0,1],[0,0.75],[0,0.5],[0,0.25]];outlineConnect=0;gradientColor=none;html=1;whiteSpace=wrap;fontSize=12;fontStyle=1;container=1;pointerEvents=0;collapsible=0;recursiveResize=0;shape=mxgraph.aws4.group;grIcon=mxgraph.aws4.group_eks_cluster;strokeColor=#FF9900;fillColor=#FFF7E8;verticalAlign=top;align=left;spacingLeft=30;fontColor=#FF9900;dashed=0;" 
  vertex="1" parent="private-subnet">
  <mxGeometry x="20" y="40" width="440" height="260" as="geometry"/>
</mxCell>
```

---

## ECS Cluster

```xml
<mxCell id="ecs-cluster" value="ECS Cluster" 
  style="points=[[0,0],[0.25,0],[0.5,0],[0.75,0],[1,0],[1,0.25],[1,0.5],[1,0.75],[1,1],[0.75,1],[0.5,1],[0.25,1],[0,1],[0,0.75],[0,0.5],[0,0.25]];outlineConnect=0;gradientColor=none;html=1;whiteSpace=wrap;fontSize=12;fontStyle=1;container=1;pointerEvents=0;collapsible=0;recursiveResize=0;shape=mxgraph.aws4.group;grIcon=mxgraph.aws4.group_ecs_cluster;strokeColor=#D05C17;fillColor=#FFF2E8;verticalAlign=top;align=left;spacingLeft=30;fontColor=#D05C17;dashed=0;" 
  vertex="1" parent="1">
  <mxGeometry x="100" y="100" width="400" height="300" as="geometry"/>
</mxCell>
```

---

## Auto Scaling Group

```xml
<mxCell id="asg" value="Auto Scaling Group" 
  style="points=[[0,0],[0.25,0],[0.5,0],[0.75,0],[1,0],[1,0.25],[1,0.5],[1,0.75],[1,1],[0.75,1],[0.5,1],[0.25,1],[0,1],[0,0.75],[0,0.5],[0,0.25]];outlineConnect=0;gradientColor=none;html=1;whiteSpace=wrap;fontSize=12;fontStyle=1;container=1;pointerEvents=0;collapsible=0;recursiveResize=0;shape=mxgraph.aws4.group;grIcon=mxgraph.aws4.group_auto_scaling_group;strokeColor=#D05C17;fillColor=#FFF2E8;verticalAlign=top;align=left;spacingLeft=30;fontColor=#D05C17;dashed=1;" 
  vertex="1" parent="1">
  <mxGeometry x="100" y="100" width="300" height="200" as="geometry"/>
</mxCell>
```

---

## Kubernetes Namespace (for EKS)

```xml
<mxCell id="k8s-namespace" value="namespace-name" 
  style="points=[[0,0],[0.25,0],[0.5,0],[0.75,0],[1,0],[1,0.25],[1,0.5],[1,0.75],[1,1],[0.75,1],[0.5,1],[0.25,1],[0,1],[0,0.75],[0,0.5],[0,0.25]];outlineConnect=0;gradientColor=none;html=1;whiteSpace=wrap;fontSize=10;fontStyle=0;container=1;pointerEvents=0;collapsible=0;recursiveResize=0;shape=mxgraph.aws4.group;grIcon=mxgraph.aws4.group_spot_fleet;strokeColor=#FF9900;fillColor=none;verticalAlign=top;align=left;spacingLeft=5;fontColor=#FF9900;dashed=1;" 
  vertex="1" parent="eks-cluster">
  <mxGeometry x="20" y="40" width="140" height="100" as="geometry"/>
</mxCell>
```

---

## Corporate Data Center (On-Premises)

```xml
<mxCell id="on-prem" value="Corporate Data Center" 
  style="points=[[0,0],[0.25,0],[0.5,0],[0.75,0],[1,0],[1,0.25],[1,0.5],[1,0.75],[1,1],[0.75,1],[0.5,1],[0.25,1],[0,1],[0,0.75],[0,0.5],[0,0.25]];outlineConnect=0;gradientColor=none;html=1;whiteSpace=wrap;fontSize=12;fontStyle=1;container=1;pointerEvents=0;collapsible=0;recursiveResize=0;shape=mxgraph.aws4.group;grIcon=mxgraph.aws4.group_corporate_data_center;strokeColor=#5A6C86;fillColor=#E6E7E8;verticalAlign=top;align=left;spacingLeft=30;fontColor=#5A6C86;dashed=0;" 
  vertex="1" parent="1">
  <mxGeometry x="40" y="40" width="300" height="200" as="geometry"/>
</mxCell>
```

---

## Generic Group (Custom Color)

```xml
<mxCell id="custom-group" value="Custom Group Name" 
  style="fillColor=#F2F6E8;strokeColor=#7AA116;verticalAlign=top;fontStyle=1;fontColor=#7AA116;whiteSpace=wrap;html=1;fontSize=12;container=1;pointerEvents=0;collapsible=0;recursiveResize=0;dashed=0;" 
  vertex="1" parent="1">
  <mxGeometry x="100" y="100" width="300" height="200" as="geometry"/>
</mxCell>
```

---

## Group Color Reference

| Group Type | Stroke Color | Fill Color | Font Color |
|------------|--------------|------------|------------|
| AWS Cloud | #232F3E | none | #232F3E |
| Region | #00A4A6 | none | #147EBA |
| VPC | #8C4FFF | none | #8C4FFF |
| Availability Zone | #147EBA | none | #147EBA |
| Public Subnet | #7AA116 | #F2F6E8 | #248814 |
| Private Subnet | #147EBA | #E6F2F8 | #147EBA |
| Security Group | #DD3522 | none | #DD3522 |
| EKS Cluster | #FF9900 | #FFF7E8 | #FF9900 |
| ECS Cluster | #D05C17 | #FFF2E8 | #D05C17 |
| Auto Scaling Group | #D05C17 | #FFF2E8 | #D05C17 |
| On-Premises | #5A6C86 | #E6E7E8 | #5A6C86 |

---

## Important Notes

1. **Parent Attribute**: Always set the `parent` attribute to the ID of the containing group
2. **Geometry**: Coordinates are relative to the parent container
3. **Container Property**: `container=1` must be set for groups to contain other elements
4. **Z-Order**: Groups should be added before their children in the XML
5. **Collapsible**: Set `collapsible=0` to prevent users from accidentally collapsing groups