# ContentSphere Monitoring Requirements

## Components
- ContentSphere application and Ubuntu EC2 server
- Prometheus and Node Exporter
- Grafana dashboards
- AWS CloudWatch metrics and alarms
- Amazon SNS notifications
- Fluent Bit or Fluentd, Elasticsearch, and Kibana

## KPI Matrix

| KPI | Initial Warning | Initial Critical | Source |
|---|---|---|---|
| CPU utilization | >70% | >80% | Prometheus / CloudWatch |
| Memory utilization | >75% | >90% | Node Exporter / CloudWatch Agent |
| Disk utilization | >75% | >90% | Node Exporter / CloudWatch Agent |
| Host availability | Investigate brief failures | Persistent target down | Prometheus |
| EC2 status | Investigate warning | Status check failed | CloudWatch |
| HTTP errors | Rising 4xx rate | Rising 5xx rate | Application metrics / logs |
| Request latency | Above baseline | Above agreed limit | Application instrumentation |
| Log errors | Increasing trend | Sustained spike | Elasticsearch / Kibana |

Thresholds are initial examples and must be tuned to the workload. Application metrics, memory, and filesystem metrics require suitable instrumentation where they are not available by default.

## Troubleshooting
1. Check the alert and timestamp.
2. Review Prometheus and Grafana metrics.
3. Check CloudWatch metrics and EC2 status checks.
4. Search application and system logs.
5. Apply corrective action and verify recovery.
