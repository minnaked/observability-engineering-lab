# Observability Engineering Lab

Security-focused observability
configurations and detection pipelines
built on ELK, OpenSearch, and Logstash.

## Contents

### Logstash Security Parsers
Parsing configurations for Windows
security events, Apache logs, firewall
logs, and VPN logs.

### OpenSearch Detections
Alert configurations for failed logins,
port scanning, and suspicious PowerShell
execution mapped to MITRE ATT&CK.

### Azure EventHub Pipeline
Log ingestion pipeline architecture
from Azure EventHub to Logstash
to OpenSearch.

## Based on Production Experience
These configurations reflect real
observability work delivered at
Louis Vuitton Singapore using ELK,
OpenSearch, GKE, Helm, and ArgoCD.
