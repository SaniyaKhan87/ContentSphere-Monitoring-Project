# ContentSphere Monitoring Architecture

## Metrics Flow
ContentSphere EC2 -> Node Exporter (9100) -> Prometheus (9090) -> Grafana

## AWS Monitoring Flow
AWS Resources -> CloudWatch Metrics -> CloudWatch Dashboard and Alarms -> SNS Notifications

## Logging Flow
Application/System Logs -> Fluent Bit or Fluentd -> Elasticsearch -> Kibana

## Component Roles
- Node Exporter exposes Linux host metrics.
- Prometheus scrapes and stores metrics.
- Grafana visualizes metrics.
- CloudWatch monitors supported AWS resource metrics.
- SNS delivers configured notifications.
- Fluent Bit or Fluentd forwards logs to Elasticsearch.
- Kibana searches and visualizes indexed logs.

Restrict access to monitoring services and do not publish credentials, tokens, or private keys. This file describes the target architecture; verify actual deployments before marking every component as implemented.
