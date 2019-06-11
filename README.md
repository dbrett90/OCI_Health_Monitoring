# OCI Health & Monitoring Demo
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
1.) Navigate to the following [link](https://cloud.oracle.com/home) & log in with your credentials.

2.) Using the navigation menu in the upper-left hand corner, select ```Compute```.
![1.)](/imgs/m1.png?raw=true)  

3.) Using the navigation menu in the upper-left hand corner, select ```Monitoring``` and then ```Alarm Definitions```
![1.)](/imgs/m2.png?raw=true)  

4.) With the ```Alarm Definitions``` console open, we need to make sure that we're looking at the appropriate metrics (either Compute, VCN, Storage, etc) for the instances within a given compartment. Set these accordingly.
![1.)](/imgs/m3.png?raw=true)  
![1.)](/imgs/m4.png?raw=true)  
