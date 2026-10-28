# ContentSphere CloudWatch Alarms

Previously recorded CPU alarm:
- Name: ContentSphere-High-CPU-Alarm
- Metric: CPUUtilization
- Threshold: Greater than 80%
- Evaluation: 1 datapoint within 5 minutes
- Last recorded state: Insufficient data

Previously recorded SNS topic: ContentSphere-CPU-Alerts
The subscription was previously reported as confirmed.

Verify the current alarm state, SNS subscription, and alarm actions in AWS. Notification delivery has not been confirmed in the available record.

Recommended additional alarm: EC2 StatusCheckFailed.

Thresholds are initial values and should be tuned to the workload.
