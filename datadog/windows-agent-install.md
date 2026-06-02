# Datadog Windows Agent Installation

## Objective

Deploy and configure Datadog Agent on a Windows 11 virtual machine to collect infrastructure telemetry.

## Prerequisites

* Datadog Account
* Datadog API Key
* Administrative Access
* Internet Connectivity

## Installation Procedure

### Step 1: Obtain Installation Command

From Datadog:

Integrations → Agent → Windows

### Step 2: Install Agent

Executed Datadog installation package with organization API key.

### Step 3: Verify Service

Verified:

Services → Datadog Agent

Status:

Running

### Step 4: Validate Connectivity

Checked:

Infrastructure → Host Map

Confirmed Windows VM appeared as an active monitored host.

## Metrics Collected

* CPU Utilization
* CPU Idle
* Memory Consumption
* Swap Usage
* Disk Usage
* Network Traffic

## Common Issues

### Host Not Appearing

Checks:

* API key validity
* Internet connectivity
* Windows firewall
* Datadog Agent service status

### Missing Metrics

Checks:

* Agent restart
* Host tags
* Agent health status

## Outcome

Datadog Agent successfully installed and collecting infrastructure telemetry from Windows 11 VM.

