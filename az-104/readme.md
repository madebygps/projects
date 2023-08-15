# Projects for AZ-104

[Study guide for Exam AZ-104: Microsoft Azure Administrator](https://learn.microsoft.com/certifications/resources/study-guides/az-104)

## Azure Onboard-o-Matic (Manage Azure identities and governance)
Automate the onboarding process of new employees into the organization's Azure AD and Azure resources. This would involve creating user accounts, assigning necessary roles, and providing access to required Azure resources.
- **Programming required?**: ❌
- **Azure Services Used:**
    - Microsoft Azure Active Directory (Azure AD)
    - Azure Policy
    - Azure Resource Groups
    - Azure Management Groups
- **Steps:**
   1. Set up a new Azure AD instance or use an existing one.
   2. Configure automated user account creation in Azure AD using Azure AD capabilities.
   3. Set up Azure AD groups and assign users to these groups based on roles.
   4. Use Azure Policy to define and enforce organization-specific requirements.
   5. Automate role assignment based on the user's department or position using Azure AD.
   6. Test the onboarding process by adding a new mock employee.
   7. Use Azure Monitor to oversee and log the onboarding activities.

---

## ShareSafely - File Share Web App (Implement and manage storage)
Design a web app where users can upload files to Azure Blob Storage and get a shareable link with controlled access and expiration time.
- **Programming required?**: ✅
- **Azure Services Used:**
    - Azure Blob Storage
    - Azure Storage Accounts
    - Azure App Service
- **Steps:**
   1. Create a new Storage Account and a Blob container.
   2. Design and code a web application with file upload capabilities.
   3. Integrate the web app with Azure Blob Storage to save the uploaded files.
   4. Generate and provide users with a link constructed with Shared Access Signature (SAS) tokens for time-limited file access.
   5. Deploy the web application on Azure App Service.

---

## VM Fleet Commander (Deploy and manage Azure compute resources)

Launch and manage a fleet of virtual machines, simulate workloads, and monitor their performance to understand optimal configurations. This project is designed to help you understand the nuances of Azure VMs, their scalability, and the importance of correct VM size selection.

- **Programming required?**: ❌
- **Azure Services Used:**
  - Azure Virtual Machines
  - Azure Virtual Machine Scale Sets
  - Azure Monitor
  - Azure Resource Manager (ARM) templates or Bicep files
  - Azure Disk Encryption
- **Steps:**
   1. Use the Azure portal to create an initial virtual machine. Select a typical configuration suitable for general-purpose tasks.
   2. Deploy an application or software on the VM. This can be a sample web server or any lightweight application. 
   3. Clone this VM using ARM templates or Bicep files to simulate a fleet. Make sure to adjust configurations (like VM size) for a few to understand how different configurations perform.
   4. Deploy virtual machines to availability zones and availability sets to ensure high availability.
   5. Implement Azure Disk Encryption on one of the VMs to understand the process and performance implications.
   6. Setup Azure Monitor to monitor the performance, health, and metrics of each VM in the fleet.
   7. Introduce synthetic load to the VMs using tools or scripts. Observe the performance metrics in Azure Monitor.
   8. Use Azure Virtual Machine Scale Sets to understand auto-scaling based on the load. Adjust the load and see how Azure responds to it.
   9. Document findings on different VM configurations, the impact of disk encryption, and the efficiency of scale sets under load.
   10. Clean up resources after the tests to avoid unnecessary costs.


---

## NetMaze Explorer (Implement and manage virtual networking)
Design a hybrid networking environment where on-premises networks connect securely to Azure resources using Azure's networking capabilities, ensuring secure data transition and effective resource access controls.
- **Programming required?**: ❌ Minimal to none. This project is largely focused on networking configurations, but understanding scripting for automating certain tasks or deploying resources could be beneficial.
- **Azure Services Used:**
    - Azure Virtual Networks
    - Azure VPN Gateway
    - Network Security Groups (NSGs)
    - Azure Bastion
    - Azure Private Link
    - Azure DNS
    - Azure Load Balancer
- **Steps:**

   1. Azure Virtual Network Setup:

        Provision an Azure Virtual Network (VNet) in your chosen region.
    Create multiple subnets within this VNet to segregate resources effectively (e.g., WebApp Subnet, Database Subnet, Admin Subnet).

    2. On-Premises Network Simulation:

        For the sake of this project, use another VNet to simulate your on-premises environment. This can be in another Azure region or the same region based on preference.

    3. Secure Connectivity:

        Implement Azure VPN Gateway to create a site-to-site VPN connection between your simulated on-premises environment (VNet) and your main Azure VNet.
    Verify the connection and ensure resources from one VNet can communicate with another, effectively simulating a hybrid environment.

    4. Resource Deployment

        Deploy test resources (like VMs) in each subnet of your main Azure VNet. For instance, deploy a web server VM in the WebApp Subnet, a database in the Database Subnet, etc.

    5. Network Access Control:

        Use Network Security Groups (NSGs) to define inbound and outbound access rules for each subnet, ensuring that only valid traffic is allowed. For instance, only allow HTTP/HTTPS traffic to the WebApp Subnet.

    6. Secure Administrative Access:

        Implement Azure Bastion for secure and seamless RDP and SSH access to your virtual machines, ensuring you don't expose your VMs to the public internet.

    7. Private Access to Azure PaaS Services:

        Use Azure Private Link to access Azure PaaS services (like Azure SQL Database) over a private endpoint within your VNet, ensuring data doesn't traverse over the public internet.

    8. DNS and Load Balancing:

        Configure Azure DNS to have custom domain names for your resources.
    Implement Azure Load Balancer to distribute traffic across your VMs in the WebApp Subnet.

    9. Performance and Security Testing:

        Simulate various network scenarios to test performance, such as data transition between on-premises and Azure.
    Attempt to access resources from outside the permitted paths to validate the security configurations in place.

    10. Monitoring and Auditing:

        Enable monitoring and diagnostics on your VPN Gateway, NSGs, and other network resources to gain insights into network operations.
    Review logs and set up alerts for any suspicious activities.


---

## Azure InsightScape (Monitor and maintain Azure resources)
Get a complete picture of your Azure environment by setting up a comprehensive monitoring and alerting system. This project will centralize the monitoring of all your previous projects, providing a holistic view of resources, performance metrics, alerts, and health statuses.

- **Programming required?**: ✅ (For crafting KQL queries)
- **Azure Services Used:**
  - Azure Monitor
  - Azure Metrics
  - Azure Log Analytics
  - Azure Alerts
  - Azure Network Watcher
  - Azure Backup
  - Azure Site Recovery
  - Azure Resource Health
  
- **Steps:**
   1. **Azure Monitor Setup**:
        - Set up Azure Monitor to collect telemetry and other data from all your Azure resources involved in the previous projects.

   2. **Azure Metrics Configuration**:
        - Configure Azure Metrics to keep track of performance metrics across the board. Focus on VM performance, storage access times, and network latencies.

   3. **Azure Log Analytics Integration**:
        - Use Azure Log Analytics to create a centralized logging solution. Ensure logs from VMs, storage accounts, and network activities are flowing into the platform.
    
   4. **KQL Queries Crafting**:
        - Dive into Azure Log Analytics and use KQL to extract valuable insights.
            - VM performance: 
                ```kql
                Perf
                | where ObjectName == "Processor" and CounterName == "% Processor Time" 
                | summarize avg(CounterValue) by bin(TimeGenerated, 5m), Computer
                ```
            - Failed login attempts:
                ```kql
                SecurityEvent 
                | where EventID == 4625
                ```
            - Data transfer out from Azure blob storage:
                ```kql
                AzureDiagnostics
                | where ResourceType == "BLOB" and OperationName == "GetBlob"
                | summarize sum(by user_principal_name_s, TimeGenerated)
                ```
        - Use these queries (and more) to better understand the behavior, performance, and security aspects of your resources.

   5. **Threshold Definitions**:
        - Define key metrics and thresholds that are relevant to each project's success. For instance, CPU and Memory utilization thresholds for VMs from "VM Fleet Commander".

   6. **Azure Alerts Configuration**:
        - Setup Azure Alerts based on the thresholds defined. Ensure that you get notified when any metric goes beyond the acceptable range.

   7. **Azure Network Watcher**:
        - Use Azure Network Watcher to monitor and diagnose conditions at a network scenario level in, and out of Azure.

   8. **Disaster Recovery Planning**:
        - Implement Azure Backup and Azure Site Recovery for mission-critical resources, ensuring you have a disaster recovery plan in place.

   9. **Azure Resource Health Checks**:
        - Regularly check Azure Resource Health for the status of your resources and get detailed insights when they are facing issues.

   10. **Dashboard Creation**:
        - Create a comprehensive dashboard in Azure Monitor, giving a visual representation of all metrics, logs, and alerts.

   11. **Test Scenarios**:
        - Perform test scenarios, like simulating high load or network issues, to validate the effectiveness of your monitoring setup.

   12. **Refinement**:
        - Refine and adjust your monitoring strategy based on insights gathered over a period.

   13. **Documentation**:
        - Document best practices and learnings from this comprehensive monitoring setup.



