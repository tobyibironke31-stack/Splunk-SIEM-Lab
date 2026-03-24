# Splunk-SIEM-Lab
Deployment of Splunk Enterprise on Windows 11 Pro VM for data analytics and SIEM operations.

Splunk Enterprise SIEM & Virtualization Lab
Project Overview
This lab demonstrates the end-to-end deployment of a Splunk Enterprise instance within a virtualized infrastructure. The project focuses on setting up a Security Information and Event Management (SIEM) environment to ingest, index, and analyze large-scale log data using Search Processing Language (SPL).

Technical Stack
SIEM: Splunk Enterprise (Latest Version)

Virtualization: VMware Workstation

Operating Systems: Windows 11 Pro (Primary Host), Windows Server 2022

Tools: Microsoft Edge (Management Console), VS Code (Scripting/Documentation)
Technical Implementation Details
1. Infrastructure Provisioning
Virtual Environment: Configured a Windows 11 Pro VM specifically to host the Splunk indexer, ensuring proper resource allocation within the VMware hypervisor.

Service Configuration: Successfully installed Splunk Enterprise and verified local web server connectivity via Port 8000, reaching the Administrator home dashboard.

2. Data Engineering & Ingestion
Dataset: Ingested tutorialdata.zip, consisting of web access logs and vendor sales data.

Pipeline: Navigated the Splunk "Add Data" wizard to define source types and ensure the successful indexing of 219,728 raw events.

Verification: Validated that data was searchable and correctly parsed into fields such as clientip, action, and status.

3. Advanced Analytics with SPL
Used Search Processing Language (SPL) to perform complex data correlations and statistical analysis:

Event Filtering: Utilized custom time ranges and boolean logic to isolate specific forensic windows.

Statistical Aggregation: Executed commands like stats count and distinct_count(productId) to transform raw logs into business intelligence.

Relational Correlation: Developed queries to identify successful purchases (status=200) and map them to unique user IP addresses.

Lab screen shots :

![Splunk Dashboard](images/01-Splunk-Login.png)

![Data Upload Success](images/02-Data-Upload-Success.png)

![Event Search](images/03-Event-Search.png)

![SPL Analytics Results](images/04-SPL-Analytics.png)

Key Takeaways
Virtualization: Gained hands-on experience managing enterprise software within a hypervisor-controlled Windows environment.

SIEM Proficiency: Mastered the basics of the Splunk pipeline: Ingest, Index, and Search.

Analytical Thinking: Developed the ability to write complex search queries to extract meaningful insights from over 200,000 log entries.
