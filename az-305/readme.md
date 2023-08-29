# Azure AZ-305 

[![Video Name](https://img.youtube.com/vi/SRWMfO-q9dc/maxresdefault.jpg)](https://www.youtube.com/watch?v=SRWMfO-q9dc)

[Study guide for Exam AZ-305: Designing Microsoft Azure Infrastructure Solutions](https://learn.microsoft.com/certifications/resources/study-guides/az-305)


The Azure AZ-305 certification is designed to validate your expertise in designing and implementing solutions on Microsoft's Azure cloud platform, focusing on aspects like identity, governance, data storage, business continuity, and infrastructure. 

# Hands-On Projects Projects

Governify: The Ultimate Identity, Governance, and Monitoring Solution (Design identity, governance, and monitoring solutions)
-----------------------------------------------------------------------------------------------------------------------------

This skill measures your ability to design and recommend solutions for logging, monitoring, authentication, and authorization in Azure. It also assesses your understanding of governance structures, including management groups, subscriptions, and resource groups, as well as compliance and identity governance.

In this project, you'll create a multi-tier web application and implement identity, governance, and monitoring solutions. You'll set up Azure AD for authentication, use Azure Policy and Blueprints for governance, and configure Azure Monitor and Log Analytics for logging and monitoring.

### Diagram Description

The architecture consists of a multi-tier web application deployed on Azure App Service, connected to an Azure SQL Database. Azure AD is used for authentication, Azure Policy and Blueprints enforce governance, and Azure Monitor and Log Analytics are set up for logging and monitoring.

### Programming Required?

✅

### Azure Services Used

-   Azure App Service
-   Azure SQL Database
-   Azure AD
-   Azure Policy
-   Azure Blueprints
-   Azure Monitor
-   Azure Log Analytics

### Steps

1.  Set Up the Multi-Tier Web Application

    -   Create an Azure App Service for the front-end and another for the back-end.
    -   Deploy a sample web application to the front-end App Service.
    -   Deploy a sample API to the back-end App Service.
    -   Create an Azure SQL Database and connect it to the back-end.
2.  Implement Azure AD Authentication

    -   Set up Azure AD and create a few test users.
    -   Integrate Azure AD authentication into the front-end and back-end of your web application.
3.  Set Up Governance with Azure Policy and Blueprints

    -   Create Azure Policies that enforce tagging and other governance rules.
    -   Create an Azure Blueprint and add the policies to it.
    -   Assign the blueprint to your Azure subscription.
4.  Configure Azure Monitor and Log Analytics

    -   Create a Log Analytics workspace.
    -   Enable Azure Monitor and connect it to the Log Analytics workspace.
    -   Configure your App Services and SQL Database to send logs and metrics to Azure Monitor.
5.  Implement Logging in the Application

    -   Add logging code to your front-end and back-end applications.
    -   Use Azure SDKs to send these logs to Azure Monitor.
6.  Set Up Alerts and Monitoring

    -   Create custom queries in Azure Log Analytics to analyze logs.
    -   Set up alerts in Azure Monitor based on metrics or log events.
7.  Test the Complete Setup

    -   Log in to the application using different Azure AD users.
    -   Verify that governance policies are being enforced on resources.
    -   Check Azure Monitor and Log Analytics to ensure logs and metrics are being captured.
    -   Trigger alerts by simulating error conditions or exceeding thresholds.

DataFort: A Comprehensive Data Storage and Integration Solution (Design data storage solutions)
-----------------------------------------------------------------------------------------------

### Skill Description

This skill measures your ability to design data storage solutions for both relational and non-relational data types. You'll need to know how to recommend appropriate Azure data services, storage tiers, and data protection strategies. Additionally, you'll be evaluated on your ability to design data integration and analysis solutions.

### Project Description

In this project, you'll create a comprehensive data storage and integration solution using Azure services. You'll set up an Azure SQL Database for relational data and Azure Blob Storage for semi-structured and unstructured data. You'll also implement data integration using Azure Data Factory and data analysis using Azure Synapse Analytics.

### Diagram Description

The architecture consists of an Azure SQL Database for storing relational data and Azure Blob Storage for semi-structured and unstructured data. Azure Data Factory is used for data integration between these storage solutions, and Azure Synapse Analytics is set up for data analysis.

### Programming Required?

✅

### Azure Services Used

-   Azure SQL Database
-   Azure Blob Storage
-   Azure Data Factory
-   Azure Synapse Analytics

### Steps

1.  Set Up Azure SQL Database

    -   Create an Azure SQL Database.
    -   Choose an appropriate service tier and compute tier based on your needs.
    -   Populate the database with some sample relational data.
2.  Set Up Azure Blob Storage

    -   Create an Azure Blob Storage account.
    -   Upload some sample semi-structured (e.g., JSON files) and unstructured (e.g., images, videos) data.
3.  Implement Data Protection

    -   Enable Geo-Replication for Azure SQL Database for disaster recovery.
    -   Set up Azure Blob Storage with cool and hot access tiers, and enable Azure Blob Versioning for data protection.
4.  Design Data Integration with Azure Data Factory

    -   Create an Azure Data Factory instance.
    -   Create a data pipeline to move data from Azure SQL Database to Azure Blob Storage and vice versa.
5.  Implement Data Analysis with Azure Synapse Analytics

    -   Create an Azure Synapse Analytics workspace.
    -   Import data from Azure SQL Database and Azure Blob Storage.
    -   Run some sample data analysis queries and visualize the results.
6.  Test the Complete Setup

    -   Verify that data can be added, updated, and deleted in Azure SQL Database and Azure Blob Storage.
    -   Run the Azure Data Factory pipeline to ensure data integration is working as expected.
    -   Perform some data analysis tasks in Azure Synapse Analytics and validate the results.

ContinuityCraft: Mastering Business Continuity in Azure (Design business continuity solutions)
----------------------------------------------------------------------------------------------

### Skill Description

This skill assesses your ability to design backup and disaster recovery solutions for Azure and hybrid workloads, including compute resources, databases, and unstructured data. It also evaluates your expertise in recommending high-availability solutions for various types of data and compute resources.

### Project Description

In this project, you'll set up a multi-tier web application with a relational database and blob storage. You'll implement backup and disaster recovery solutions for each component and ensure high availability for the entire system.

### Diagram Description

The architecture includes a multi-tier web application deployed on Azure App Service, connected to an Azure SQL Database and Azure Blob Storage. Azure Backup and Azure Site Recovery are configured for backup and disaster recovery, while Azure Availability Zones are used for high availability.

### Programming Required?

✅

### Azure Services Used

-   Azure App Service
-   Azure SQL Database
-   Azure Blob Storage
-   Azure Backup
-   Azure Site Recovery
-   Azure Availability Zones

### Steps

1.  Set Up the Multi-Tier Web Application

    -   Create an Azure App Service for the front-end and another for the back-end.
    -   Deploy a sample web application to the front-end App Service.
    -   Deploy a sample API to the back-end App Service.
2.  Set Up Azure SQL Database and Blob Storage

    -   Create an Azure SQL Database and populate it with sample data.
    -   Create an Azure Blob Storage account and upload some sample unstructured data.
3.  Implement Backup and Disaster Recovery

    -   Configure Azure Backup to take regular backups of the App Service and Blob Storage.
    -   Use Azure Site Recovery to set up disaster recovery for the Azure SQL Database and App Service.
4.  Implement High Availability

    -   Configure the App Service and SQL Database to use Azure Availability Zones.
    -   Set up Azure Blob Storage with geo-redundant storage (GRS) for high availability.
5.  Test Backup and Recovery

    -   Perform test backups and restores using Azure Backup.
    -   Execute a disaster recovery drill using Azure Site Recovery.
6.  Test High Availability

    -   Simulate failures to ensure that the App Service, SQL Database, and Blob Storage remain available.
    -   Validate that the system automatically recovers and continues to function as expected.

InfraGenius: A Comprehensive Azure Infrastructure Solution (Design infrastructure solutions)
--------------------------------------------------------------------------------------------

### Skill Description

This skill measures your ability to design various types of compute solutions, application architectures, and migration strategies. It also assesses your expertise in designing network solutions that include connectivity, performance optimization, security, and load-balancing.

### Project Description

In this project, you'll design and implement a comprehensive Azure infrastructure solution that includes a virtual machine-based application, containerized microservices, serverless functions, and batch processing tasks. You'll also integrate these components using a messaging architecture and migrate an on-premises database to Azure. Finally, you'll optimize network performance and security.

### Diagram Description

The architecture consists of Azure VMs running a web application, Azure Kubernetes Service (AKS) for containerized microservices, Azure Functions for serverless computing, and Azure Batch for batch processing. Azure Service Bus is used for messaging, and Azure VPN Gateway connects on-premises networks to Azure resources.

### Programming Required?

✅

### Azure Services Used

-   Azure Virtual Machines
-   Azure Kubernetes Service (AKS)
-   Azure Functions
-   Azure Batch
-   Azure Service Bus
-   Azure SQL Database
-   Azure VPN Gateway
-   Azure Network Security Groups
-   Azure Load Balancer

### Steps

1.  Set Up Azure Virtual Machines

    -   Create Azure VMs and deploy a sample web application.
    -   Configure networking and security settings for the VMs.
2.  Implement Containerized Microservices with AKS

    -   Create an Azure Kubernetes Service cluster.
    -   Deploy a sample microservices application to the AKS cluster.
3.  Implement Serverless Computing with Azure Functions

    -   Create an Azure Functions app.
    -   Write and deploy a few sample serverless functions.
4.  Implement Batch Processing with Azure Batch

    -   Create an Azure Batch account.
    -   Write and deploy a sample batch processing task.
5.  Set Up Messaging with Azure Service Bus

    -   Create an Azure Service Bus namespace.
    -   Implement messaging between the VM-based application and the AKS microservices.
6.  Migrate On-Premises Database to Azure SQL Database

    -   Create an Azure SQL Database.
    -   Migrate an on-premises database to Azure using Azure Database Migration Service.
7.  Implement Network Optimization and Security

    -   Create an Azure VPN Gateway to connect on-premises networks to Azure.
    -   Optimize network performance using Azure Network Security Groups.
    -   Implement load balancing using Azure Load Balancer.
8.  Test the Complete Setup

    -   Verify that all components (VMs, AKS, Functions, Batch) are working as expected.
    -   Test the messaging through Azure Service Bus.
    -   Validate the database migration.
    -   Test network connectivity, performance, and security.