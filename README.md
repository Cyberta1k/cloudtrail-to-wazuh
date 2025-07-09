# Forwarding AWS CloudTrail Logs to Wazuh SIEM

This repository documents a production-grade configuration to forward **AWS CloudTrail logs** to **Wazuh SIEM** for security monitoring, compliance, and detection engineering.

It includes:
- CloudTrail and S3 configuration
- IAM policies for log access
- Wazuh S3 integration setup
- Sample Wazuh detection rules

---

## Architecture Overview

```mermaid
flowchart LR
    A[AWS CloudTrail] --> B[S3 Bucket: CloudTrail Logs]
    B --> C[Wazuh Manager]
    C --> D[Alerts and Detections]
