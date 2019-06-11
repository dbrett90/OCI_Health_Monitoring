# OCI Monitoring - Alarm Status/Definitions
This repository is built specifically for creating a customer-facing demo for OCI Health &amp; Monitoring Tools

## Overview
The OCI Health and Monitoring Demo will cover 5 specific tools native to the OCI Console. These include:
* Service Metrics
* Metrics Explorer
* Alarm Status
* Alarm Definitions
* Health Checks

Upon completion of the demo, users should have a deeper understanding of how they can leverage these Tools
to monitor their cloud infrastructure at a high level. For information regarding deeper & more expansive monitoring see the links for [Oracle CASB](https://docs.oracle.com/en/cloud/paas/casb-cloud/palug/toc.htm) & [Oracle Management Cloud](https://docs.oracle.com/en/cloud/paas/management-cloud/index.html).

## OCI Service Metrics & Metrics Explorer
### Prerequisites
In this module we'll explore how to create, update, suppress, and delete alarms , as well as how to retrieve alarm history. In order to complete this lab you must have:
* An active Oracle Cloud Account (Trial is fine)
* An active compute node

### Guide

#### To create an example threshold alarm

This procedure walks through creation of an example threshold alarm to detect Compute instances operating at non-optimal thresholds. A **Threshold Alarm** is an alarm that checks for metric values outside a given range or value. The procedure uses options as displayed in Basic Mode.  

1). Open the navigation menu. Under **Solutions, Platform and Edge**, go to **Monitoring** and click **Alarm Definitions.**

2). Click **Create Alarm**

3). On the **Create Alarm** page, under **Define alarm**, fill in or update the alarm settings:
* **Alarm Name**: Non-Optimal Alarm
* **Alarm Severity**: Warning
* **Alarm Body**: Non-optimal utilization detected. An application or process may be consuming more CPU than usual.
* **Metric description**: 
  * **Compartment**: (select your compartment)
  * **Metric Namespace: oci_computeagent**
  * **Metric Name: CpuUtilization**
  * **Interval: 1m**
  * **Statistic: Count**
* **Trigger rule:**
  * **Operator: between**
  * **Value**: 60
  * **Value**: 80
  * **Trigger Delay Minutes**: 10
4). Set up an email notification under **Notifications, Destinations:**
* **Destination Service**: Notifications Service
* **Compartment**: (select your compartment)
* **Topic**: Click **Create a topic**
  * **Topic Name**: Operations Team
  * **Topic Description**: Resource Monitoring Channel
  * **Subscription Protocol: Email**
  * **Email Addresses**: (type an email address for the operations team here)
5). Repeat notification every day:
* **Repeat Notification?**: (select this option)
* **Notification Interval**: 24 hours
6). Click **Save alarm**.

