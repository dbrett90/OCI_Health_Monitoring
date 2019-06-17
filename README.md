# OCI Health & Monitoring Demo
This repository is built specifically for creating a customer-facing demo for OCI Health &amp; Monitoring Tools

## Overview
The OCI Health and Monitoring Demo will cover 5 specific tools native to the OCI Console. These include:
* [Service Metrics](https://github.com/dbrett90/OCI_Health_Monitoring#oci-service-metrics)
* [Metrics Explorer](https://github.com/dbrett90/OCI_Health_Monitoring#oci-metrics-explorer)
* Alarm Status
* Alarm Definitions
* Health Checks

Upon completion of the demo, users should have a deeper understanding of how they can leverage these Tools
to monitor their cloud infrastructure at a high level. For information regarding deeper & more expansive monitoring see the links for [Oracle CASB](https://docs.oracle.com/en/cloud/paas/casb-cloud/palug/toc.htm) & [Oracle Management Cloud](https://docs.oracle.com/en/cloud/paas/management-cloud/index.html).

## Prerequisites
In this module we'll explore how you can leverage Oracle's out-of-the-box Service Metrics & Metric
explorer to increase your insight into the health of your underlying cloud infrastructure. In order to complete this lab you must have:
* An active Oracle Cloud Account (Trial is fine)
* [An active compute node](https://oracle.github.io/learning-library/oci-library/)
* IAM Policy in place that allows users to manage monitoring resources

## OCI Service Metrics

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
Note that each of these metrics can be accessed within the [Metrics Explorer](https://github.com/dbrett90/OCI_Health_Monitoring#oci-metric-explorer) or can be used to create a corresponding alarm should a metric reach a defined threshold.

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

## OCI Metrics Explorer
1.) Refer back to the section ```View Metric Charts``` Step 3 and select ```Metrics Explorer```
![1.)](/imgs/m2.png?raw=true)

2.) In the Metrics Explorer tab, write and edit queries by filling in the fields:
* <b>Compartment</b>: The compartment containing the resources that you want to monitor. By default, the first accessible compartment is selected.
* <b>Metric Namespace</b>: The service or application emitting metrics for the resources that you want to monitor.
* <b>Metric Name</b>: The name of the metric. Only one metric can be specified. Metric selections depend on the selected compartment and metric namespace. Example: <b>CpuUtilization</b>
* <b>Interval</b>: The aggregation window.
* <b>Statistic</b>: The aggregation function.
* <b>Metric Dimensions</b>: Optional filters to narrow the metric data evaluated.
* <b>Aggregate Metric Streams</b>: Aggregates all results to plot a single aggregated average for all metric sstreams. This average is plotted as a single line on the metric chart. This operation is helpful when you want to plot a metric as one line for all resources.

![1.)](/imgs/m5.png?raw=true)
Then click on <b>Update Chart</b>.


3.) To customize the Y-Axis Label or range, type the label you want into <b>Y-Axis Label</b> or type the minimum and maximum values you want into <b>Y-Axis Min Value</b> and <b>Y-Axis Max Value</b>.
![1.)](/imgs/m6.png?raw=true)

4.) To view the query as a Monitoring Query Language (MQL) expression, click <b>Advanced Mode</b>.
![1.)](/imgs/ADV_mode_in_metric_exp.png?raw=true)
Use Advanced Mode to edit your query using MQL syntax to aggregate results by group. The MQL syntax also supports additional parameter values.

5.) To share the query you can click on <b>Advanced Mode</b> and copy the text in the <b>Query Code Editor</b> box.
![1.)](/imgs/share_query.png?raw=true)

6.) To hide a query from the chart we can click on the <b>Toggle query on chart</b> icon.
![1.)](/imgs/toggle_query.png?raw=true)
