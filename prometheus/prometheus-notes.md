# ContentSphere Prometheus Monitoring

Prometheus collects Linux server metrics from configured scrape targets. Node Exporter exposes host metrics on port 9100, and Prometheus commonly runs on port 9090.

## PromQL Queries

Target availability:
up

CPU utilization (%):
100 * (1 - avg by (instance) (rate(node_cpu_seconds_total{mode="idle"}[5m])))

Memory utilization (%):
100 * (1 - node_memory_MemAvailable_bytes / node_memory_MemTotal_bytes)

Disk utilization (%):
100 * (1 - (node_filesystem_avail_bytes{mountpoint="/", fstype!~"tmpfs|overlay"} / node_filesystem_size_bytes{mountpoint="/", fstype!~"tmpfs|overlay"}))

Network received bytes/sec:
rate(node_network_receive_bytes_total[5m])

Network transmitted bytes/sec:
rate(node_network_transmit_bytes_total[5m])

Server uptime in seconds:
time() - node_boot_time_seconds

## Verification Commands

sudo systemctl status prometheus --no-pager
sudo systemctl status node_exporter --no-pager
curl -sS http://localhost:9090/-/healthy
curl -sS http://localhost:9100/metrics | head

Check the Prometheus Targets page and confirm the configured targets are UP. Queries require the corresponding metrics to be available.
