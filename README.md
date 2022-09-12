Azure Firewall (AF) is...

AF is integrated with Azure Monitor. This means you can forward AF metrics and logs to:
* Log Analytics Workspace
* Azure Storage
* Event hub

A [Log Analytics workspace](https://docs.microsoft.com/en-us/azure/azure-monitor/logs/log-analytics-workspace-overview) is a unique environment for log data from Azure Monitor and other Azure services. Each workspace has its own data repository and configuration but might combine data from multiple services.

Ingest data in a Log Analytics workspace has a Latency.

Latency refers to the time that data is created on the monitored system and the time that it comes available for analysis in Azure Monitor. 

[The typical latency](https://docs.microsoft.com/en-us/azure/azure-monitor/logs/data-ingestion-time#typical-latency) to ingest log data is between 20 seconds and 3 minutes.

This latency can be frustrating if you want so see in (near) real-time what's happening on AF.

# azure-firewall-mon
Azure-Firewall-Mon is a near-real-time Azure Firewall Monitor log viewer for Azure Firewall. It uses Azure Event Hub to have events from AF as soon as possible on a web UI. Objective of this project is have an experience similar to [Check Point's SmartView](https://community.checkpoint.com/t5/Management/SmartView-Accessing-Check-Point-Logs-from-Web/td-p/3710) web log access
