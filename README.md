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

### Prerequisites
In this module we'll explore how to create, update, suppress, and delete alarms , as well as how to retrieve alarm history. In order to complete this lab you must have:
* An active Oracle Cloud Account (Trial is fine)
* An active compute node

### Guide

## To create an example threshold alarm

This procedure walks through creation of an example threshold alarm to detect Compute instances operating at non-optimal thresholds. A **Threshold Alarm** is an alarm that checks for metric values outside a given range or value. The procedure uses options as displayed in Basic Mode.  

1). Open the navigation menu. Under **Solutions, Platform and Edge**, go to **Monitoring** and click **Alarm Definitions.**
![1.)](/imgs/p1.png?raw=true)

2). Click **Create Alarm**
![1.)](/imgs/p2.png?raw=true)

3). On the **Create Alarm** page, under **Define alarm**, fill in or update the alarm settings:
* **Alarm Name**: Non-Optimal Alarm
* **Alarm Severity**: Warning
* **Alarm Body**: Non-optimal utilization detected. An application or process may be consuming more CPU than usual.
![1.)](/imgs/p3.png?raw=true)

* **Metric description**: 
  * **Compartment**: (select your compartment)
  * **Metric Namespace: oci_computeagent**
  * **Metric Name: CpuUtilization**
  * **Interval: 1m**
  * **Statistic: Count**
![1.)](/imgs/p4.png?raw=true)
  
* **Trigger rule:**
  * **Operator: between**
  * **Value**: 5
  * **Value**: 60
  * **Trigger Delay Minutes**: 10
![1.)](/imgs/p5.png?raw=true)
  
4). Set up an email notification under **Notifications, Destinations:**
* **Destination Service**: Notifications Service
* **Compartment**: (select your compartment)
* **Topic**: Click **Create a topic**
![1.)](/imgs/p6.png?raw=true)

  * **Topic Name**: Operations Team
  * **Topic Description**: Resource Monitoring Channel
  * **Subscription Protocol: Email**
  * **Email Addresses**: (type an email address for the operations team here)
![1.)](/imgs/p7.png?raw=true)
  
5). Repeat notification every day:
* **Repeat Notification?**: (select this option)
* **Notification Interval**: 24 hours

6). Click **Save alarm**.

![1.)](/imgs/p8.png?raw=true)

### Example Results: 
![1.)](/imgs/p17.png?raw=true)


## To create an example absence alarm

This procedure walks through creation of an example absence alarm to detect resources that may be down or unreachable. An **Absence Alarm** is an alarm that checks for absent metrics (using the absent operator). The procedure uses options as displayed in Basic Mode.

1). Open the navigation menu. Under **Solutions, Platform and Edge**, go to **Monitoring** and click **Alarm Definitions.**
![1.)](/imgs/p1.png?raw=true)

2). Click **Create Alarm**
![1.)](/imgs/p2.png?raw=true)

3). On the **Create Alarm** page, under **Define alarm**, fill in or update the alarm settings:
* **Alarm Name**: Up/Down Resource Alarm
* **Alarm Severity**: Critical
* **Alarm Body**: Resource may be down. Please investigate. Move workloads to another available resource.
![1.)](/imgs/p9.png?raw=true)

* **Metric description**: 
  * **Compartment**: (select your compartment)
  * **Metric Namespace: oci_computeagent**
  * **Metric Name: CpuUtilization**
  * **Interval: 1m**
  * **Statistic: Count**
![1.)](/imgs/p10.png?raw=true)
  
* **Trigger rule:**
  * **Operator: absent**
  * **Trigger Delay Minutes**: 5
![1.)](/imgs/p11.png?raw=true)
  
4). Set up an email notification under **Notifications, Destinations:**
* **Destination Service**: Notifications Service
* **Compartment**: (select your compartment)
* **Topic**: Click **Create a topic**
![1.)](/imgs/p6.png?raw=true)

  * **Topic Name**: Operations Team
  * **Topic Description**: Resource Up/Down Channel
  * **Subscription Protocol: Email**
  * **Email Addresses**: (type an email address for the operations team here)
![1.)](/imgs/p12.png?raw=true)
  
5). Repeat notification every day:
* **Repeat Notification?**: (select this option)
* **Notification Interval**: 1 minute

6). Click **Save alarm**.

![1.)](/imgs/p13.png?raw=true)

### Example Results: 
![1.)](/imgs/p16.png?raw=true)
