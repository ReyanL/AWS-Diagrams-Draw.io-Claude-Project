# AWS Connections Reference for Draw.io

## Connection Structure

All connections use `mxCell` with `edge="1"` attribute.

### Basic Connection Template

```xml
<mxCell id="conn-[source]-[target]" 
  style="[STYLE_STRING]" 
  edge="1" parent="1" source="[source-id]" target="[target-id]">
  <mxGeometry relative="1" as="geometry"/>
</mxCell>
```

---

## Connection Styles by Data Flow Type

### Primary Data Flow (Solid)

```xml
style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;strokeColor=#232F3E;strokeWidth=2;"
```

### Secondary/Optional Flow (Dashed)

```xml
style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;strokeColor=#232F3E;strokeWidth=1;dashed=1;dashPattern=5 5;"
```

### Async/Event Flow (Dotted)

```xml
style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;strokeColor=#BC1356;strokeWidth=1;dashed=1;dashPattern=2 2;"
```

---

## Color-Coded Connections by Service Category

### Compute (Orange)
```xml
strokeColor=#FF9900
```

### Database (Blue)
```xml
strokeColor=#3B48CC
```

### Networking (Purple)
```xml
strokeColor=#8C4FFF
```

### Security (Red)
```xml
strokeColor=#DD3522
```

### Storage (Green)
```xml
strokeColor=#277116
```

### Management/Monitoring (Pink)
```xml
strokeColor=#BC1356
```

### Integration/Messaging (Pink/Magenta)
```xml
strokeColor=#C925D1
```

---

## Edge Styles

### Orthogonal (Right Angles)
```xml
edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;
```

### Curved
```xml
edgeStyle=elbowEdgeStyle;elbow=horizontal;
```

### Straight Line
```xml
edgeStyle=none;
```

### Entity Relation (for database diagrams)
```xml
edgeStyle=entityRelationEdgeStyle;
```

---

## Arrow Styles

### Standard Arrow (Default)
```xml
endArrow=classic;
```

### Open Arrow
```xml
endArrow=open;
```

### Block Arrow
```xml
endArrow=block;
```

### No Arrow (Line Only)
```xml
endArrow=none;
```

### Bidirectional
```xml
startArrow=classic;endArrow=classic;
```

### Diamond (for aggregation)
```xml
startArrow=diamond;endArrow=none;
```

---

## Connection Width

| Width | Usage |
|-------|-------|
| 1 | Secondary connections, internal flows |
| 2 | Primary data flows, main paths |
| 3 | Critical paths, highlighted flows |

---

## Complete Connection Examples

### User to Load Balancer
```xml
<mxCell id="conn-user-alb" 
  style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;strokeColor=#232F3E;strokeWidth=2;endArrow=classic;" 
  edge="1" parent="1" source="end-users" target="alb">
  <mxGeometry relative="1" as="geometry"/>
</mxCell>
```

### Service to Database
```xml
<mxCell id="conn-service-db" 
  style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;strokeColor=#3B48CC;strokeWidth=1;dashed=1;dashPattern=5 5;endArrow=classic;" 
  edge="1" parent="1" source="app-service" target="rds-instance">
  <mxGeometry relative="1" as="geometry"/>
</mxCell>
```

### Microservice to Microservice
```xml
<mxCell id="conn-svc1-svc2" 
  style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;strokeColor=#FF9900;strokeWidth=1;dashed=1;dashPattern=5 5;endArrow=classic;" 
  edge="1" parent="1" source="service-1" target="service-2">
  <mxGeometry relative="1" as="geometry"/>
</mxCell>
```

### Async Event (SNS/SQS)
```xml
<mxCell id="conn-sns-sqs" 
  style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;strokeColor=#BC1356;strokeWidth=1;dashed=1;dashPattern=2 2;endArrow=classic;" 
  edge="1" parent="1" source="sns-topic" target="sqs-queue">
  <mxGeometry relative="1" as="geometry"/>
</mxCell>
```

### VPN/Direct Connect
```xml
<mxCell id="conn-vpn" 
  style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;strokeColor=#5A30B5;strokeWidth=2;dashed=1;dashPattern=8 4;endArrow=classic;startArrow=classic;" 
  edge="1" parent="1" source="on-prem" target="vpn-gw">
  <mxGeometry relative="1" as="geometry"/>
</mxCell>
```

### Monitoring Flow
```xml
<mxCell id="conn-monitoring" 
  style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;strokeColor=#BC1356;strokeWidth=1;dashed=1;dashPattern=3 3;endArrow=open;" 
  edge="1" parent="1" source="eks-cluster" target="cloudwatch">
  <mxGeometry relative="1" as="geometry"/>
</mxCell>
```

---

## Connection Labels

Add labels to connections by setting the `value` attribute:

```xml
<mxCell id="conn-with-label" value="HTTPS" 
  style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;strokeColor=#232F3E;strokeWidth=2;fontColor=#232F3E;fontSize=10;" 
  edge="1" parent="1" source="alb" target="service">
  <mxGeometry relative="1" as="geometry"/>
</mxCell>
```

---

## Waypoints (Custom Routing)

For complex routing, add waypoints:

```xml
<mxCell id="conn-with-waypoints" 
  style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;strokeColor=#232F3E;strokeWidth=2;" 
  edge="1" parent="1" source="source" target="target">
  <mxGeometry relative="1" as="geometry">
    <Array as="points">
      <mxPoint x="300" y="200"/>
      <mxPoint x="300" y="400"/>
    </Array>
  </mxGeometry>
</mxCell>
```

---

## Best Practices

1. **Consistency**: Use the same style for similar connection types
2. **Color Coding**: Match connection colors to the service category they represent
3. **Width Hierarchy**: Use thicker lines for primary flows
4. **Dashed vs Solid**: Solid for synchronous, dashed for async/optional
5. **Arrow Direction**: Always point arrows in the direction of data flow
6. **Labels**: Add labels for protocol/port when relevant (HTTPS, gRPC, etc.)