# Forward Lacework Logs and Events to Datadog

## Overview

Use the Datadog-Lacework integration to forward your Lacework logs and events to Datadog.

## Setup

All configuration happens on Lacework Dashboard. Find details on how to set it up in the Lacework Documentation. Datadog automatically enables the right logs processing pipeline when it detects Lacework logs.

**Installation**

1. In Lacework, go to Settings and select Integrations.
2. In the Outgoing section (on the left panel) select Datadog.
3. Fill in the following details:

Name: Enter a name for the integration. For example, Datadog-Lacework.
Datadog Type: Select the type of logs sent to Datadog:

- Type: Logs Detail - Sends Lacework detailed logs to the Datadog logs platform.
- Type: Logs Summary - Sends a Lacework summary to the Datadog logs platform.
- Type: Events Summary - Sends a Lacework summary to the Datadog Events platform.

**Datadog Site:**

- Select `com` if you use the Datadog US region.
- Select `eu` if you use the Datadog EU region.

**API KEY:** Enter your Datadog API key.

**Alert Security Level:** Select the minimum log severity level of forwarded logs

## Data Collected

**Metrics**
This Lacework integration does not not collect metrics

**Service Checks**
This Lacework intgeration does not include any service checks.

**Logs**
Lacework can be configured to send Logs.

**Events**
Lacework can be configured to send Events.
