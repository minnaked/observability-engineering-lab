# Observability Engineering Lab

## Overview

This repository documents my hands on journey learning modern observability
concepts using Datadog, the OpenTelemetry Collector, Linux, Windows, and a home
lab environment.

The focus of this repository is not infrastructure deployment or platform
engineering, but understanding how telemetry can be used to monitor systems,
analyze performance, establish operational baselines, identify anomalies, and
improve troubleshooting.

The lab is inspired by real world experience supporting enterprise observability
and monitoring platforms including Riverbed SteelCentral, ExtraHop NDR, Datadog,
and OpenSearch.

## Status

This lab is actively developing. The sections below separate what is in place
today from what is planned next, so the structure is a roadmap being filled in
rather than a finished product.

## Lab Environment

### Monitoring Platform

- Datadog
- OpenTelemetry Collector

### Monitored Hosts

Five hosts run the Datadog Agent and report into Datadog, across Windows and
Linux:

- A Windows 11 detection lab host
- Two additional Windows hosts
- A Wazuh server on Linux
- A Kali Linux host

### Tools

- Datadog Agent
- OpenTelemetry Collector
- Wazuh
- OpenSearch
- Linux
- Windows
- Python

## Current State

What is collected and visible today:

- The Datadog Agent deployed on all five hosts, all reporting and up to date
- Host and infrastructure metrics: CPU, memory, disk, load, and IO
- Log collection enabled
- The OpenTelemetry Collector running on one host
- The built in Host Metrics dashboard, showing CPU, load averages, and memory
  across the fleet
- Baseline host monitors for CPU, disk, and memory

## Planned and In Progress

- Custom dashboards built to answer specific operational questions
- Custom Datadog Agent instrumentation for the Wazuh manager, which has no native
  integration, to expose engine metrics such as events processed, events dropped,
  and queue usage
- Application performance monitoring and distributed tracing, not yet active, a
  learning goal once a suitable application is instrumented

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

## Repository Structure

Current:

```
observability-engineering-lab/
├── README.md
└── datadog/
    ├── host-onboarding.md
    ├── windows-agent-install.md
    ├── host-metrics-dashboard.md
    └── screenshots/
```

Planned, added as each piece is built:

```
├── metrics-fundamentals/
├── dashboards/
├── service-monitoring/
└── application-monitoring/
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

Monitoring application services and supporting processes, with the Wazuh manager
and OpenSearch as the worked example.

### Application Monitoring Concepts

Understanding latency, throughput, error rates, and availability, including
application performance monitoring and distributed tracing as a planned learning
area, not yet implemented in this lab.

### Capacity Planning

Using telemetry to establish baselines, track growth trends, and forecast future
resource requirements.

## Screenshots

The datadog/screenshots folder documents the lab as it stands:

- Fleet Automation overview, all agents healthy across the five hosts
- Infrastructure host list
- The Host Metrics dashboard, CPU, load averages, and memory
- Agent onboarding and the first host live view

Each entry includes purpose, metrics used, interpretation, and operational use.

## Author

Mahesh Inna Kedage

Senior Observability, Security, and Customer Engineering Professional

CISSP | NUS Master of Technology, Software Engineering

GitHub: https://github.com/minnaked
