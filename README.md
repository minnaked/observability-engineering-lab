# Observability Engineering Lab

## Overview

This repository documents my hands on journey learning modern observability
concepts using Datadog, Linux, Windows, OpenSearch, and home lab environments.

The focus of this repository is not infrastructure deployment or platform
engineering, but understanding how telemetry can be used to monitor systems,
analyze performance, establish operational baselines, identify anomalies, and
improve troubleshooting.

The lab is inspired by real world experience supporting enterprise observability
and monitoring platforms including Riverbed SteelCentral, ExtraHop NDR, Datadog,
OpenSearch, and related monitoring technologies.

## Status

This lab is actively developing. Each section is added as the work behind it is
built and validated, so the structure below is the roadmap being filled in rather
than a finished product.

## Learning Objectives

This repository explores:

- Metrics fundamentals
- Time series analysis
- Dashboard design
- Capacity planning
- Service monitoring
- Application monitoring concepts
- Alerting and threshold design
- Performance analysis
- Root cause investigation

## Lab Environment

### Monitoring Platform

- Datadog

### Monitored Systems

- Windows 11 endpoint
- Ubuntu Linux virtual machines
- Wazuh security monitoring platform
- OpenSearch components

### Tools

- Datadog Agent
- OpenSearch
- Wazuh
- Linux
- Windows
- Python

## Repository Structure

```
observability-engineering-lab/
├── datadog/
│   ├── host-onboarding.md
│   ├── windows-agent-install.md
│   ├── host-metrics-dashboard.md
│   └── screenshots/
│
├── metrics-fundamentals/
│   ├── gauges.md
│   ├── counters.md
│   ├── rates.md
│   └── percentiles.md
│
├── dashboards/
│   ├── infrastructure-health.md
│   ├── service-health.md
│   └── capacity-dashboard.md
│
├── service-monitoring/
│   ├── wazuh-manager.md
│   ├── opensearch.md
│   └── datadog-agent.md
│
├── application-monitoring/
│   ├── latency.md
│   ├── throughput.md
│   ├── availability.md
│   └── errors.md
│
└── screenshots/
```

## Key Topics Covered

### Metrics Fundamentals

Understanding gauges, counters, rates, percentiles, and aggregations.

### Time Series Analysis

Learning how to interpret trends, spikes, baselines, seasonality, and anomalies.

### Dashboard Design

Building dashboards that answer operational questions such as:

- Is the system healthy?
- Which resource is saturated?
- Is performance degrading?
- Is capacity sufficient?

### Service Monitoring

Monitoring application services and supporting processes including the Wazuh
manager, OpenSearch, and the Datadog Agent.

### Application Monitoring Concepts

Understanding latency, throughput, error rates, availability, and user experience
metrics, including application performance monitoring and distributed tracing
concepts.

### Capacity Planning

Using telemetry to establish baselines, track growth trends, and forecast future
resource requirements.

## Screenshots

This repository contains screenshots and explanations of dashboards built in
Datadog using telemetry collected from the Windows and Linux lab environments.

Each dashboard includes:

- Purpose
- Metrics used
- Interpretation
- Operational use cases
- Troubleshooting examples

## Author

Mahesh Inna Kedage

Senior Observability, Security, and Customer Engineering Professional

CISSP | NUS Master of Technology, Software Engineering

GitHub: https://github.com/minnaked

