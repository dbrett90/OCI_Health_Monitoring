# OCI Health & Monitoring Demo
This repository is built specifically for creating a customer-facing demo for OCI Health &amp; Monitoring Tools

## Overview
The OCI Health and Monitoring Demo will cover 5 specific tools native to the OCI Console. These include:
* [Service Metrics & Metrics Explorer](https://github.com/dbrett90/OCI_Health_Monitoring#oci-service-metrics--metrics-explorer)
* Alarm Status
* Alarm Definitions
* Health Checks

Upon completion of the demo, users should have a deeper understanding of how they can leverage these Tools
to monitor their cloud infrastructure at a high level. For information regarding deeper & more expansive monitoring see the links for [Oracle CASB](https://docs.oracle.com/en/cloud/paas/casb-cloud/palug/toc.htm) & [Oracle Management Cloud](https://docs.oracle.com/en/cloud/paas/management-cloud/index.html).

### Prerequisites
In this module we'll explore how you can leverage Oracle's out-of-the-box Service Metrics & Metric
explorer to increase your insight into the health of your underlying cloud infrastructure. In order to complete this lab you must have:
* An active Oracle Cloud Account (Trial is fine)
* An active compute node

## OCI Service Metrics & Metrics Explorer

### View Metric Charts
1.) Navigate to the following [link](https://cloud.oracle.com/home) & log in with your credentials.

2.) Using the navigation menu in the upper-left hand corner, select ```Compute```.
![1.)](/imgs/m1.png?raw=true)  

3.) Using the navigation menu in the upper-left hand corner, select ```Monitoring``` and then ```Service Metrics```
![1.)](/imgs/m2.png?raw=true)  

4.) With the Service Metrics console open, we need to make sure that we're looking at the appropriate metrics (either Compute, VCN, Storage, etc) for the instances within a given compartment. Set these accordingly.
![1.)](/imgs/m3.png?raw=true)  
![1.)](/imgs/m4.png?raw=true)  

5.) Make sure the start & end date are configured for the period you'd like to monitor. You will now have access to a high level overview for the following fields:
* CPU Utilization
* Memory Utilization
* Disk Read I/O
* Disk Write I/O
* Disk Ready Bytes
* Disk Write Bytes
* Network Receive Bytes
* Network Transmit Bytes
![1.)](/imgs/m5a.png?raw=true)
Note that each of these metrics can be accessed within the [Metrics Explorer](https://github.com/dbrett90/OCI_Health_Monitoring#building-metric-queries) or can be used to create a corresponding alarm should a metric reach a defined threshold.

6.) Service Metrics are also highly customizable. Users can adjust the interval for each metric along with the statistic being shown. Users can see the following statistics for each metric outlined in the previous step:
* Rate
* Sum
* Mean
* Min
* Max
* Count
* 50th Percentile
* 90th Percentile
* 99th Percentile
* 99.9 Percentile
![1.)](/imgs/m6a.png?raw=true)

### Building Metric Queries
1.) Refer back to the section ```View Metric Charts``` Step 3 and select ```Metrics Explorer```
![1.)](/imgs/m2.png?raw=true)

2.) In the Metrics Explorer tab, write and edit queries in Monitoring Query Language (MQL). Fill in the fields for a new query (Compartment, Metric Namespace, Metric Name, Interval, Statistic, Metric Dimensions, Aggregate Metric Streams) and click on <b>Update Chart</b>.
![1.)](/imgs/m5.png?raw=true)

3.) To customize the Y-Axis Label or range, type the label you want into <b>Y-Axis Label</b> or type the minimum and maximum values you want into <b>Y-Axis Min Value</b> and <b>Y-Axis Max Value</b>.
![1.)](/imgs/m6.png?raw=true)
