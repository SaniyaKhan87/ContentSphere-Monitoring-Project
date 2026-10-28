# ContentSphere Kibana Log Analysis

Purpose: search and visualize application, web-server, and operating-system logs stored in Elasticsearch.

## Basic Workflow
1. Confirm Elasticsearch is receiving log events.
2. Create a Kibana data view for the actual index or data stream.
3. Use Discover to search logs by time, host, service, and severity.
4. Create a dashboard named ContentSphere Log Analysis.
5. Review error events and correlate their timestamps with Grafana metrics and CloudWatch alarms.

## Example KQL Queries

Error logs, if the field exists:
log.level : "error"

HTTP 5xx responses, if the field exists:
http.response.status_code >= 500

ContentSphere error logs, if these fields exist:
service.name : "contentsphere" and log.level : "error"

The queries depend on the actual indexed field names and mappings. Verify the results in Kibana.
