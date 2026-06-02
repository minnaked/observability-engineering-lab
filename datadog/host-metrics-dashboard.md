# Datadog Host Onboarding Lab

## Objective

The objective of this lab was to onboard infrastructure hosts into Datadog and validate telemetry collection for observability and monitoring purposes.

## Environment

| Component           | Details                    |
| ------------------- | -------------------------- |
| Host OS             | Windows 11                 |
| Monitoring Platform | Datadog                    |
| Agent Version       | Latest Available           |
| Lab Type            | Personal Observability Lab |

## Architecture

Host
↓
Datadog Agent
↓
Datadog SaaS Platform
↓
Host Metrics Dashboard

## Implementation Steps

1. Created Datadog trial account.
2. Generated API key from Datadog Integrations page.
3. Installed Datadog Agent on Windows 11 VM.
4. Registered host using Datadog API key.
5. Verified agent service status.
6. Confirmed host registration within Datadog Infrastructure view.

## Validation

Successfully verified:

* CPU Metrics
* Memory Metrics
* Disk Metrics
* Network Metrics
* Host Availability

## Troubleshooting Performed

* Verified outbound HTTPS connectivity.
* Confirmed API key configuration.
* Restarted Datadog Agent service after configuration updates.
* Validated host registration in Infrastructure Inventory.

## Outcome

Successfully onboarded Windows host into Datadog and established baseline observability metrics for future dashboarding and alerting use cases.

## Skills Demonstrated

* Datadog Agent Deployment
* Host Onboarding
* Infrastructure Monitoring
* Observability Fundamentals
* Troubleshooting

