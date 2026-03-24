# Splunk-SIEM-Lab
Deployment of Splunk Enterprise on Windows 11 Pro VM for data analytics and SIEM operations.
1. Infrastructure & Environment
Hypervisor Layer: Utilized VMware Workstation to manage multiple concurrent virtual instances, including Windows 11 Pro and Windows Server 2022.

Guest OS Configuration: Provisioned a Windows 11 Pro environment (Oibironke-Win11) specifically for Splunk Enterprise deployment.

Network Connectivity: Configured and verified local service hosting via Port 8000, ensuring successful communication between the Splunk indexer and the web management interface.

2. Data Engineering & Ingestion
Dataset Management: Ingested the tutorialdata.zip dataset, successfully processing and indexing over 219,728 raw events.

Pipeline Verification: Monitored the ingestion wizard to ensure "File has been uploaded successfully" and validated data integrity across multiple source types, including vendor_sales and access_combined.

Host Identification: Standardized event tagging to a local loopback (127.0.0.1) to simulate a centralized logging environment.

3. Search Processing Language (SPL) Analytics
Statistical Aggregation: Developed advanced SPL queries to transform raw logs into actionable metrics using the stats command.

User Behavior Analysis: Correlated successful purchases (status=200, action=purchase) with unique clientip addresses to identify high-volume users.

Cardinality & Values: Leveraged distinct_count(productId) and values(productId) functions to analyze the diversity of products purchased per unique session.

Time-Series Forensics: Applied Custom Time Ranges to isolate and investigate specific security or operational windows within the indexed metadata.
