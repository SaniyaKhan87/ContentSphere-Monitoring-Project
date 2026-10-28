# ContentSphere Grafana Dashboard

Purpose: visualize infrastructure metrics collected by Prometheus.

Recommended panels:
- CPU utilization
- Memory utilization
- Disk utilization
- Network received and transmitted traffic
- Target availability using up
- Server uptime

Configuration:
1. Add Prometheus as the Grafana data source.
2. Test the data source connection.
3. Create panels using the queries in prometheus/prometheus-notes.md.
4. Set a suitable time range and save the dashboard.
5. Capture screenshots of working panels.

Application request volume, HTTP errors, and latency require application instrumentation or suitable log-based metrics.
