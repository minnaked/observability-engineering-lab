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

## Install Logs from Powershell
PS C:\WINDOWS\system32> [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072;
PS C:\WINDOWS\system32> $env:DD_API_KEY = '5cf67c99d55c0a18ab249f9ebe3bfbb6';
PS C:\WINDOWS\system32> $env:DD_APP_KEY = 'ddapp_8A5t6TJhtG1aCSbikyak7AneYyCw3INw1Q';
PS C:\WINDOWS\system32> $env:DD_SITE = 'datadoghq.com';
PS C:\WINDOWS\system32> $env:DD_APM_INSTRUMENTATION_ENABLED = 'iis';
PS C:\WINDOWS\system32> $env:DD_APM_INSTRUMENTATION_LIBRARIES = 'dotnet:3';
PS C:\WINDOWS\system32> $env:DD_OTELCOLLECTOR_ENABLED = 'true';
PS C:\WINDOWS\system32> $env:DD_PRIVATE_ACTION_RUNNER_ENABLED = 'true';
PS C:\WINDOWS\system32> $env:DD_PRIVATE_ACTION_RUNNER_ACTIONS_ALLOWLIST = 'com.datadoghq.script.runPredefinedPowershellScript';
PS C:\WINDOWS\system32> (New-Object System.Net.WebClient).DownloadFile('https://install.datadoghq.com/datadog-installer-x86_64.exe', 'C:\Windows\SystemTemp\datadog-installer-x86_64.exe');
PS C:\WINDOWS\system32> C:\Windows\SystemTemp\datadog-installer-x86_64.exe
Datadog Installer 7.79.1 - https://www.datadoghq.com
Running the default installation script (https://github.com/DataDog/datadog-agent/tree/672032c98c/pkg/fleet/installer/setup/defaultscript/default_script.go) - 2026-06-02T21:12:03+05:30
The following packages will be installed:
  - datadog-agent / 7.79.1-1
  - datadog-apm-library-dotnet / 3
Stopping Datadog Agent services...
Applying configurations...
Installing datadog-agent...
Successfully installed datadog-agent
Installing datadog-apm-library-dotnet...
INFO:  Installing .NET tracer
INFO:  Ensuring log directory 'C:\ProgramData\Datadog .NET Tracer\logs' exists
INFO:  Successfully installed assembly 'C:\ProgramData\Datadog\Installer\packages\datadog-apm-library-dotnet\3.45.0\library\net461\Datadog.Trace.dll' into the GAC.
INFO:  Successfully installed assembly 'C:\ProgramData\Datadog\Installer\packages\datadog-apm-library-dotnet\3.45.0\library\net461\Datadog.Trace.MSBuild.dll' into the GAC.
INFO:  Adding crash tracking key to registry: 'Software\Microsoft\Windows\Windows Error Reporting\RuntimeExceptionHelperModules'
INFO:  Crash tracking handler path 'C:\ProgramData\Datadog\Installer\packages\datadog-apm-library-dotnet\3.45.0\library\win-x64\Datadog.Trace.ClrProfiler.Native.dll' added to 'Software\Microsoft\Windows\Windows Error Reporting\RuntimeExceptionHelperModules'
INFO:  Enabling IIS instrumentation for .NET tracer
INFO:  Reading IIS information from registry key: 'Software\Microsoft\InetStp'
INFO:  IIS registry key not found
WARNING:  This installer requires IIS 10.0 or later. Could not determine the IIS version; is the IIS feature enabled?
Successfully installed datadog-apm-library-dotnet
Successfully ran the default install script in 2m7s!

## Common Issues
##Powershell Logs

PS C:\WINDOWS\system32> [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072;
PS C:\WINDOWS\system32> $env:DD_API_KEY = 'XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX';
PS C:\WINDOWS\system32> $env:DD_APP_KEY = 'ddapp_nDoZGpkPASIBPstiuMnQeoJKCPiw1junjF';
PS C:\WINDOWS\system32> $env:DD_SITE = 'datadoghq.com';
PS C:\WINDOWS\system32> $env:DD_APM_INSTRUMENTATION_ENABLED = 'iis';
PS C:\WINDOWS\system32> $env:DD_APM_INSTRUMENTATION_LIBRARIES = 'dotnet:3';
PS C:\WINDOWS\system32> $env:DD_OTELCOLLECTOR_ENABLED = 'true';
PS C:\WINDOWS\system32> $env:DD_PRIVATE_ACTION_RUNNER_ENABLED = 'true';
PS C:\WINDOWS\system32> $env:DD_PRIVATE_ACTION_RUNNER_ACTIONS_ALLOWLIST = 'com.datadoghq.script.runPredefinedPowershellScript';
PS C:\WINDOWS\system32> (New-Object System.Net.WebClient).DownloadFile('https://install.datadoghq.com/datadog-installer-x86_64.exe', 'C:\Windows\SystemTemp\datadog-installer-x86_64.exe');
PS C:\WINDOWS\system32> C:\Windows\SystemTemp\datadog-installer-x86_64.exe
Datadog Installer 7.79.1 - https://www.datadoghq.com
Running the default installation script (https://github.com/DataDog/datadog-agent/tree/672032c98c/pkg/fleet/installer/setup/defaultscript/default_script.go) - 2026-06-02T21:58:41+05:30
The following packages will be installed:
  - datadog-agent / 7.79.1-1
  - datadog-apm-library-dotnet / 3
Stopping Datadog Agent services...
Applying configurations...
Installing datadog-agent...
failed to send telemetry payload to endpoint https://instrumentation-telemetry-intake.datadoghq.com/api/v2/apmtelemetry: 403 Forbidden
failed to send telemetry payload to endpoint https://instrumentation-telemetry-intake.datadoghq.com/api/v2/apmtelemetry: 403 Forbidden
failed to send telemetry payload to endpoint https://instrumentation-telemetry-intake.datadoghq.com/api/v2/apmtelemetry: 403 Forbidden
failed to send telemetry payload to endpoint https://instrumentation-telemetry-intake.datadoghq.com/api/v2/apmtelemetry: 403 Forbidden
failed to send telemetry payload to endpoint https://instrumentation-telemetry-intake.datadoghq.com/api/v2/apmtelemetry: 403 Forbidden
failed to send telemetry payload to endpoint https://instrumentation-telemetry-intake.datadoghq.com/api/v2/apmtelemetry: 403 Forbidden
Successfully installed datadog-agent
Installing datadog-apm-library-dotnet...
failed to send telemetry payload to endpoint https://instrumentation-telemetry-intake.datadoghq.com/api/v2/apmtelemetry: 403 Forbidden
INFO:  Installing .NET tracer
INFO:  Ensuring log directory 'C:\ProgramData\Datadog .NET Tracer\logs' exists
INFO:  Successfully installed assembly 'C:\ProgramData\Datadog\Installer\packages\datadog-apm-library-dotnet\3.45.0\library\net461\Datadog.Trace.dll' into the GAC.
INFO:  Successfully installed assembly 'C:\ProgramData\Datadog\Installer\packages\datadog-apm-library-dotnet\3.45.0\library\net461\Datadog.Trace.MSBuild.dll' into the GAC.
INFO:  Adding crash tracking key to registry: 'Software\Microsoft\Windows\Windows Error Reporting\RuntimeExceptionHelperModules'
INFO:  Crash tracking handler path 'C:\ProgramData\Datadog\Installer\packages\datadog-apm-library-dotnet\3.45.0\library\win-x64\Datadog.Trace.ClrProfiler.Native.dll' added to 'Software\Microsoft\Windows\Windows Error Reporting\RuntimeExceptionHelperModules'
INFO:  Enabling IIS instrumentation for .NET tracer
INFO:  Reading IIS information from registry key: 'Software\Microsoft\InetStp'
INFO:  IIS registry key not found
WARNING:  This installer requires IIS 10.0 or later. Could not determine the IIS version; is the IIS feature enabled?
failed to send telemetry payload to endpoint https://instrumentation-telemetry-intake.datadoghq.com/api/v2/apmtelemetry: 403 Forbidden
Successfully installed datadog-apm-library-dotnet
Successfully ran the default install script in 1m46s!
failed to send telemetry payload to endpoint https://instrumentation-telemetry-intake.datadoghq.com/api/v2/apmtelemetry: 403 Forbidden
PS C:\WINDOWS\system32>
PS C:\WINDOWS\system32>
PS C:\WINDOWS\system32> C:\Windows\SystemTemp\datadog-installer-x86_64.exe
Datadog Installer 7.79.1 - https://www.datadoghq.com
Running the default installation script (https://github.com/DataDog/datadog-agent/tree/672032c98c/pkg/fleet/installer/setup/defaultscript/default_script.go) - 2026-06-02T22:00:59+05:30
The following packages will be installed:
  - datadog-agent / 7.79.1-1
  - datadog-apm-library-dotnet / 3
Stopping Datadog Agent services...
Applying configurations...
Installing datadog-agent...
package datadog-agent version 7.79.1-1 is already installed, updating it anyway
failed to send telemetry payload to endpoint https://instrumentation-telemetry-intake.datadoghq.com/api/v2/apmtelemetry: 403 Forbidden
failed to send telemetry payload to endpoint https://instrumentation-telemetry-intake.datadoghq.com/api/v2/apmtelemetry: 403 Forbidden
failed to send telemetry payload to endpoint https://instrumentation-telemetry-intake.datadoghq.com/api/v2/apmtelemetry: 403 Forbidden
failed to send telemetry payload to endpoint https://instrumentation-telemetry-intake.datadoghq.com/api/v2/apmtelemetry: 403 Forbidden
Successfully installed datadog-agent
Installing datadog-apm-library-dotnet...
package datadog-apm-library-dotnet version 3.45.0 is already installed
Successfully installed datadog-apm-library-dotnet
Successfully ran the default install script in 2m7s!
failed to send telemetry payload to endpoint https://instrumentation-telemetry-intake.datadoghq.com/api/v2/apmtelemetry: 403 Forbidden
PS C:\WINDOWS\system32> [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072;
PS C:\WINDOWS\system32> $env:DD_API_KEY = 'XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX';
PS C:\WINDOWS\system32> $env:DD_SITE = 'datadoghq.com';
PS C:\WINDOWS\system32> (New-Object System.Net.WebClient).DownloadFile('https://install.datadoghq.com/datadog-installer-x86_64.exe', 'C:\Windows\SystemTemp\datadog-installer-x86_64.exe');
PS C:\WINDOWS\system32> C:\Windows\SystemTemp\datadog-installer-x86_64.exe
Datadog Installer 7.79.1 - https://www.datadoghq.com
Running the default installation script (https://github.com/DataDog/datadog-agent/tree/672032c98c/pkg/fleet/installer/setup/defaultscript/default_script.go) - 2026-06-02T22:11:16+05:30
The following packages will be installed:
  - datadog-agent / 7.79.1-1
  - datadog-apm-library-dotnet / 3
Stopping Datadog Agent services...
Applying configurations...
Installing datadog-agent...
package datadog-agent version 7.79.1-1 is already installed, updating it anyway
failed to send telemetry payload to endpoint https://instrumentation-telemetry-intake.datadoghq.com/api/v2/apmtelemetry: 403 Forbidden
failed to send telemetry payload to endpoint https://instrumentation-telemetry-intake.datadoghq.com/api/v2/apmtelemetry: 403 Forbidden
failed to send telemetry payload to endpoint https://instrumentation-telemetry-intake.datadoghq.com/api/v2/apmtelemetry: 403 Forbidden
failed to send telemetry payload to endpoint https://instrumentation-telemetry-intake.datadoghq.com/api/v2/apmtelemetry: 403 Forbidden
Successfully installed datadog-agent
Installing datadog-apm-library-dotnet...
package datadog-apm-library-dotnet version 3.45.0 is already installed
Successfully installed datadog-apm-library-dotnet
Successfully ran the default install script in 1m50s!
failed to send telemetry payload to endpoint https://instrumentation-telemetry-intake.datadoghq.com/api/v2/apmtelemetry: 403 Forbidden

### Host Not Appearing

Checks:

* API key validity - Encountered and resolved
* Internet connectivity
* Windows firewall
* Datadog Agent service status - Running

### Missing Metrics

Checks:

* Agent restart
* Host tags
* Agent health status

## Outcome

Datadog Agent successfully installed and collecting infrastructure telemetry from Windows 11 VM.

