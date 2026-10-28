# ContentSphere Monitoring Project

**Course:** DevOps with AWS  
**Batch:** DR501  
**Submitted by:** Saniya Maulavi  
**Submitted to:** Akhilesh Dubey  
**Submission date:** 29 October 2026  
**AWS Region:** Sydney (`ap-southeast-2`)

## 1. Project Overview

ContentSphere is a cloud monitoring and centralized logging project created as part of DevOps with AWS practical training. It focuses on infrastructure monitoring, metrics visualization, cloud alarms, log collection, and log analysis.

## 2. Objectives

- Monitor Linux infrastructure metrics.
- Visualize metrics using Grafana.
- Monitor AWS resources using Amazon CloudWatch.
- Document CloudWatch alarms and SNS notifications.
- Explore log collection and forwarding using Fluent Bit.
- Search and analyze logs using Elasticsearch and Kibana.
- Document monitoring tasks and practical results.

## 3. Technologies

- AWS EC2 and Ubuntu Linux
- Prometheus and Node Exporter
- Grafana
- Amazon CloudWatch and Amazon SNS
- Fluent Bit
- Elasticsearch and Kibana

## 4. Current Repository Structure

- `README.md` — project overview and repository guide
- `monitoring-project-report.docx` — project report
- `cloudwatch/` — CloudWatch dashboard and alarm notes
- `logging/` — Elasticsearch notes
- `kibana/` — Kibana dashboard notes
- `screenshots/` — 35 practical screenshots (`1.png` to `35.png`)

## 5. Monitoring Workflow

1. Collect infrastructure metrics using Prometheus and Node Exporter.
2. Visualize metrics through Grafana.
3. Monitor AWS resources and alarms through CloudWatch.
4. Document notification configuration using SNS.
5. Collect and forward logs using a log collection agent.
6. Search and analyze log events using Elasticsearch and Kibana.
7. Review screenshots and project documentation.

## 6. Security and Cost Considerations

- Never commit AWS credentials, passwords, access tokens, or private SSH keys.
- Review screenshots and configuration files before publishing.
- Restrict access to monitoring and logging services.
- Review AWS resource usage and stop or delete lab resources when no longer required.

## 7. Author

**Saniya Maulavi**  
DevOps with AWS — Batch DR501
