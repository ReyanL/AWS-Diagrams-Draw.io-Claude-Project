# Kubernetes Icons Reference for Draw.io

## Icon Structure
All Kubernetes icons follow this XML pattern:

```xml
<mxCell id="[unique-id]" value="[Label]" 
  style="sketch=0;outlineConnect=0;fontColor=#232F3E;fillColor=[FILL_COLOR];strokeColor=[STROKE_COLOR];dashed=0;verticalLabelPosition=bottom;verticalAlign=top;align=center;html=1;fontSize=11;fontStyle=0;aspect=fixed;shape=mxgraph.kubernetes.icon;prIcon=[K8S_ICON]" 
  vertex="1" parent="[parent-id]">
  <mxGeometry x="[X]" y="[Y]" width="[WIDTH]" height="[HEIGHT]" as="geometry"/>
</mxCell>
```

---

## Core Kubernetes Resources

### Pod
```xml
prIcon=pod
fillColor=#326CE5
strokeColor=#ffffff
```

**Complete Example:**
```xml
<mxCell id="pod-1" value="Frontend Pod" 
  style="sketch=0;outlineConnect=0;fontColor=#232F3E;fillColor=#326CE5;strokeColor=#ffffff;dashed=0;verticalLabelPosition=bottom;verticalAlign=top;align=center;html=1;fontSize=11;fontStyle=0;aspect=fixed;shape=mxgraph.kubernetes.icon;prIcon=pod" 
  vertex="1" parent="1">
  <mxGeometry x="100" y="100" width="50" height="48" as="geometry"/>
</mxCell>
```

### Deployment
```xml
prIcon=deploy
fillColor=#326CE5
strokeColor=#ffffff
```

### ReplicaSet
```xml
prIcon=rs
fillColor=#326CE5
strokeColor=#ffffff
```

### StatefulSet
```xml
prIcon=sts
fillColor=#326CE5
strokeColor=#ffffff
```

### DaemonSet
```xml
prIcon=ds
fillColor=#326CE5
strokeColor=#ffffff
```

### Job
```xml
prIcon=job
fillColor=#326CE5
strokeColor=#ffffff
```

### CronJob
```xml
prIcon=cronjob
fillColor=#326CE5
strokeColor=#ffffff
```

---

## Networking Resources

### Service
```xml
prIcon=svc
fillColor=#326CE5
strokeColor=#ffffff
```

### Ingress
```xml
prIcon=ing
fillColor=#326CE5
strokeColor=#ffffff
```

### NetworkPolicy
```xml
prIcon=netpol
fillColor=#326CE5
strokeColor=#ffffff
```

### Endpoint
```xml
prIcon=ep
fillColor=#326CE5
strokeColor=#ffffff
```

---

## Configuration & Storage

### ConfigMap
```xml
prIcon=cm
fillColor=#326CE5
strokeColor=#ffffff
```

### Secret
```xml
prIcon=secret
fillColor=#326CE5
strokeColor=#ffffff
```

### PersistentVolume
```xml
prIcon=pv
fillColor=#326CE5
strokeColor=#ffffff
```

### PersistentVolumeClaim
```xml
prIcon=pvc
fillColor=#326CE5
strokeColor=#ffffff
```

### StorageClass
```xml
prIcon=sc
fillColor=#326CE5
strokeColor=#ffffff
```

### Volume
```xml
prIcon=vol
fillColor=#326CE5
strokeColor=#ffffff
```

---

## Cluster Management

### Namespace
```xml
prIcon=ns
fillColor=#326CE5
strokeColor=#ffffff
```

### Node
```xml
prIcon=node
fillColor=#326CE5
strokeColor=#ffffff
```

### Cluster
```xml
prIcon=c-
fillColor=#326CE5
strokeColor=#ffffff
```

### ServiceAccount
```xml
prIcon=sa
fillColor=#326CE5
strokeColor=#ffffff
```

### Role
```xml
prIcon=role
fillColor=#326CE5
strokeColor=#ffffff
```

### RoleBinding
```xml
prIcon=rb
fillColor=#326CE5
strokeColor=#ffffff
```

### ClusterRole
```xml
prIcon=c-role
fillColor=#326CE5
strokeColor=#ffffff
```

### ClusterRoleBinding
```xml
prIcon=crb
fillColor=#326CE5
strokeColor=#ffffff
```

---

## Scaling & Autoscaling

### HorizontalPodAutoscaler
```xml
prIcon=hpa
fillColor=#326CE5
strokeColor=#ffffff
```

### VerticalPodAutoscaler
```xml
prIcon=vpa
fillColor=#326CE5
strokeColor=#ffffff
```

---

## Controllers

### Controller
```xml
prIcon=c-c-m
fillColor=#326CE5
strokeColor=#ffffff
```

### Scheduler
```xml
prIcon=sched
fillColor=#326CE5
strokeColor=#ffffff
```

### Kubelet
```xml
prIcon=kubelet
fillColor=#326CE5
strokeColor=#ffffff
```

### API Server
```xml
prIcon=api
fillColor=#326CE5
strokeColor=#ffffff
```

### etcd
```xml
prIcon=etcd
fillColor=#326CE5
strokeColor=#ffffff
```

---

## Custom Resources & Operators

### Custom Resource Definition (CRD)
```xml
prIcon=crd
fillColor=#326CE5
strokeColor=#ffffff
```

### User (for RBAC diagrams)
```xml
prIcon=user
fillColor=#326CE5
strokeColor=#ffffff
```

### Group (for RBAC diagrams)
```xml
prIcon=group
fillColor=#326CE5
strokeColor=#ffffff
```

---

## Alternative Container Icon for Kubernetes

For representing containers within pods, you can use the AWS container icon which is commonly used:

```xml
<mxCell id="container-1" value="nginx" 
  style="sketch=0;outlineConnect=0;fontColor=#232F3E;gradientColor=none;fillColor=#ED7100;strokeColor=none;dashed=0;verticalLabelPosition=bottom;verticalAlign=top;align=center;html=1;fontSize=12;fontStyle=0;aspect=fixed;pointerEvents=1;shape=mxgraph.aws4.container_1;" 
  vertex="1" parent="pod-1">
  <mxGeometry x="10" y="10" width="48" height="31" as="geometry"/>
</mxCell>
```

---

## Kubernetes Group Containers

### Namespace Container
```xml
<mxCell id="namespace-1" value="default" 
  style="fillColor=#E1F5FE;strokeColor=#01579B;dashed=1;verticalAlign=top;fontStyle=1;fontColor=#01579B;whiteSpace=wrap;html=1;fontSize=12;container=1;pointerEvents=0;collapsible=0;recursiveResize=0;" 
  vertex="1" parent="1">
  <mxGeometry x="100" y="100" width="600" height="400" as="geometry"/>
</mxCell>
```

### Pod Group (for multiple containers)
```xml
<mxCell id="pod-group" value="Pod: frontend" 
  style="fillColor=#BBDEFB;strokeColor=#1976D2;dashed=0;verticalAlign=top;fontStyle=1;fontColor=#1976D2;whiteSpace=wrap;html=1;fontSize=11;container=1;pointerEvents=0;collapsible=0;recursiveResize=0;rounded=1;" 
  vertex="1" parent="namespace-1">
  <mxGeometry x="50" y="50" width="200" height="120" as="geometry"/>
</mxCell>
```

---

## Color Scheme

### Official Kubernetes Blue
```
Fill Color: #326CE5
Stroke Color: #ffffff
Font Color: #232F3E
```

### Alternative Colors for Different States

| State | Fill Color | Use Case |
|-------|------------|----------|
| Running | #4CAF50 (Green) | Healthy pods/services |
| Pending | #FFC107 (Amber) | Starting/Waiting resources |
| Failed | #F44336 (Red) | Failed pods/jobs |
| Warning | #FF9800 (Orange) | Issues or degraded state |
| Terminating | #9E9E9E (Grey) | Shutting down |

---

## Connection Styles for Kubernetes

### Pod to Service
```xml
style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;strokeColor=#326CE5;strokeWidth=2;endArrow=classic;"
```

### Service to Ingress
```xml
style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;strokeColor=#1976D2;strokeWidth=2;dashed=1;dashPattern=5 5;endArrow=classic;"
```

### Pod to ConfigMap/Secret (Configuration)
```xml
style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;strokeColor=#00897B;strokeWidth=1;dashed=1;dashPattern=3 3;endArrow=open;"
```

### Pod to PVC (Storage)
```xml
style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;strokeColor=#6A1B9A;strokeWidth=2;endArrow=classic;"
```

### Network Policy Enforcement
```xml
style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;strokeColor=#D32F2F;strokeWidth=1;dashed=1;dashPattern=2 2;endArrow=block;"
```

---

## Complete Example: Multi-Container Pod

```xml
<!-- Pod Container -->
<mxCell id="pod-frontend" value="frontend-pod" 
  style="fillColor=#BBDEFB;strokeColor=#1976D2;dashed=0;verticalAlign=top;fontStyle=1;fontColor=#1976D2;whiteSpace=wrap;html=1;fontSize=11;container=1;pointerEvents=0;collapsible=0;recursiveResize=0;rounded=1;" 
  vertex="1" parent="namespace-default">
  <mxGeometry x="50" y="50" width="250" height="150" as="geometry"/>
</mxCell>

<!-- Pod Icon -->
<mxCell id="pod-icon" value="" 
  style="sketch=0;outlineConnect=0;fontColor=#232F3E;fillColor=#326CE5;strokeColor=#ffffff;dashed=0;verticalLabelPosition=bottom;verticalAlign=top;align=center;html=1;fontSize=11;fontStyle=0;aspect=fixed;shape=mxgraph.kubernetes.icon;prIcon=pod" 
  vertex="1" parent="pod-frontend">
  <mxGeometry x="10" y="10" width="30" height="29" as="geometry"/>
</mxCell>

<!-- Container 1: nginx -->
<mxCell id="container-nginx" value="nginx" 
  style="sketch=0;outlineConnect=0;fontColor=#232F3E;gradientColor=none;fillColor=#ED7100;strokeColor=none;dashed=0;verticalLabelPosition=bottom;verticalAlign=top;align=center;html=1;fontSize=11;fontStyle=0;aspect=fixed;pointerEvents=1;shape=mxgraph.aws4.container_1;" 
  vertex="1" parent="pod-frontend">
  <mxGeometry x="50" y="50" width="48" height="31" as="geometry"/>
</mxCell>

<!-- Container 2: sidecar -->
<mxCell id="container-sidecar" value="fluent-bit" 
  style="sketch=0;outlineConnect=0;fontColor=#232F3E;gradientColor=none;fillColor=#ED7100;strokeColor=none;dashed=0;verticalLabelPosition=bottom;verticalAlign=top;align=center;html=1;fontSize=11;fontStyle=0;aspect=fixed;pointerEvents=1;shape=mxgraph.aws4.container_1;" 
  vertex="1" parent="pod-frontend">
  <mxGeometry x="150" y="50" width="48" height="31" as="geometry"/>
</mxCell>
```

---

## Best Practices

1. **Consistency**: Use official Kubernetes blue (#326CE5) for standard resources
2. **Color Coding**: Use state colors (green/amber/red) to indicate resource health
3. **Grouping**: Always group related resources (pods in namespaces, containers in pods)
4. **Labels**: Use clear, descriptive labels matching actual Kubernetes resource names
5. **Connections**: 
   - Solid lines for data flow
   - Dashed lines for configuration/policy
   - Color-code by relationship type
6. **Hierarchy**: Maintain proper nesting (Cluster > Namespace > Workload > Pod > Container)

---

## Integration with AWS Services

When combining Kubernetes (EKS) with AWS services:

```xml
<!-- EKS Cluster Container -->
<mxCell id="eks-cluster" value="EKS Cluster" 
  style="points=[[0,0],[0.25,0],[0.5,0],[0.75,0],[1,0],[1,0.25],[1,0.5],[1,0.75],[1,1],[0.75,1],[0.5,1],[0.25,1],[0,1],[0,0.75],[0,0.5],[0,0.25]];outlineConnect=0;gradientColor=none;html=1;whiteSpace=wrap;fontSize=12;fontStyle=1;container=1;pointerEvents=0;collapsible=0;recursiveResize=0;shape=mxgraph.aws4.group;grIcon=mxgraph.aws4.group_eks_cluster;strokeColor=#FF9900;fillColor=#FFF7E8;verticalAlign=top;align=left;spacingLeft=30;fontColor=#FF9900;dashed=0;" 
  vertex="1" parent="private-subnet">
  <mxGeometry x="20" y="40" width="600" height="400" as="geometry"/>
</mxCell>

<!-- K8s Namespace inside EKS -->
<mxCell id="k8s-namespace" value="production" 
  style="fillColor=#E1F5FE;strokeColor=#01579B;dashed=1;verticalAlign=top;fontStyle=1;fontColor=#01579B;whiteSpace=wrap;html=1;fontSize=12;container=1;pointerEvents=0;collapsible=0;recursiveResize=0;" 
  vertex="1" parent="eks-cluster">
  <mxGeometry x="40" y="40" width="520" height="320" as="geometry"/>
</mxCell>

<!-- K8s Pods with containers -->
<!-- Use Kubernetes icons for pods and AWS container icons for containers -->
```

---

## Common Architecture Patterns

### Microservices Pattern
- Use Deployment icons for each microservice
- Connect to Service icons
- Show Ingress at the entry point
- Include ConfigMaps and Secrets

### Stateful Application Pattern
- Use StatefulSet icon
- Connect to PersistentVolumeClaim
- Show headless Service
- Include StorageClass

### Batch Processing Pattern
- Use Job or CronJob icons
- Connect to ConfigMaps for configuration
- Show completed pods in different color

### Monitoring Stack Pattern
- DaemonSet for node monitoring
- Deployment for central collector
- Service for metrics exposure
- PersistentVolume for data retention

---

## Icon Size Recommendations

| Icon Type | Width | Height | Use Case |
|-----------|-------|--------|----------|
| Standard Resource | 50px | 48px | Pods, Services, Deployments |
| Small Resource | 30px | 29px | ConfigMaps, Secrets (in groups) |
| Container | 48px | 31px | Containers within pods |
| Large Component | 78px | 78px | Cluster-level components |

---

## Notes

- All Kubernetes icons use `shape=mxgraph.kubernetes.icon` with appropriate `prIcon` values
- The standard Kubernetes blue (#326CE5) should be used for most resources
- For containers within pods, use the AWS container icon (`shape=mxgraph.aws4.container_1`)
- Always maintain proper parent-child relationships in XML structure
- Group containers must have `container=1` attribute
- Use consistent sizing across similar resource types