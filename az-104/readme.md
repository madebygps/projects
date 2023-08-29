# Projects for AZ-104

[![Video Name](https://img.youtube.com/vi/Qd0YI9ZMHHs/hqdefault.jpg)](https://youtu.be/Qd0YI9ZMHHs)

[Study guide for Exam AZ-104: Microsoft Azure Administrator](https://learn.microsoft.com/certifications/resources/study-guides/az-104)

## Onboard Automator (Manage Azure identities and governance)
Streamline and automate the process of onboarding a new employee into Azure AD and assigning necessary Azure resources.

- **Programming required?**: ❌
- **Azure Services Used:**
  - Azure AD
  - Azure Logic Apps
  - Azure Email Service (part of Logic Apps connector)
  - Azure Resource Manager
  
- **Steps**:
   1. **Azure AD Setup**:
        - Set up a new Azure AD instance (if not already present) using the Azure portal.
   
   2. **Logic App Workflow Design**:
        - Design a Logic App workflow triggered by an event (like an entry in a SharePoint list or an email to a specific mailbox) indicating a new employee hire.
   
   3. **Azure AD User Creation**:
        - Use the Azure AD connector in Logic Apps to automatically create a new user in Azure AD based on the trigger event's details.
   
   4. **Role and Group Assignment**:
        - Assign predefined roles and groups to the new user based on the job position or department indicated in the trigger.
   
   5. **Resource Provisioning**:
        - Use the Azure Resource Manager connector in Logic Apps to provision any necessary Azure resources for the user (like VMs or specific permissions).
   
   6. **Welcome Email**:
        - Leverage the Email connector in Logic Apps to send a welcome email to the new hire with instructions and necessary access details.
   
   7. **Monitoring and Review**:
        - Monitor and review the onboarding process through Logic Apps runs history and Azure AD logs to ensure smooth operations.


---

## ShareSafely - File Share Web App (Implement and manage storage)
Create a web application where users can securely upload files to Azure Blob Storage. Once uploaded, the application generates a unique, time-limited link for the user to share. This ensures that only authorized users with the link can access the uploaded file for a specified duration.

- **Programming required?**: ✅ (For creating the web application and generating unique time-limited links.)
- **Azure Services Used:**
  - Azure Blob Storage
  - Azure Web Apps
  - Azure SQL Database
  - Azure Key Vault
  - Azure Functions
  
- **Steps**:
   1. **Storage Setup**:
        - Set up an Azure Blob Storage account and create a container to store the uploaded files.
        - Configure appropriate security settings, ensuring data at rest encryption is enabled.
   
   2. **Web Application Deployment**:
        - Develop a web application that allows users to upload files. This can be done using preferred frameworks (like ASP.NET Core, Node.js, etc.).
        - Deploy the application to Azure Web Apps.
   
   3. **File Upload Logic**:
        - In the web application, integrate Azure Blob Storage SDKs/APIs to facilitate the file upload process directly to Blob Storage.
   
   4. **Database Integration**:
        - Create an Azure SQL Database to store metadata of uploaded files, including the original filename, upload timestamp, unique link, and expiration date.
        - From the web application, upon each file upload, store this metadata in the Azure SQL Database.
   
   5. **Unique Link Generation**:
        - When a file is uploaded, use Azure Functions to generate a unique, time-limited link for the user.
        - Save this link and its expiration time in the Azure SQL Database.
   
   6. **File Retrieval**:
        - When the unique link is accessed, the web app checks the Azure SQL Database for validity and expiration.
        - If valid and not expired, the web app facilitates the file download from Azure Blob Storage.
   
   7. **Secure Credentials**:
        - Store any sensitive credentials or configuration strings (like Blob Storage access keys) securely in Azure Key Vault.
        - Integrate Azure Key Vault with the web application to retrieve these credentials when needed.
   
   8. **Monitoring and Cleanup**:
        - Set up monitoring to track file upload/download activities.
        - Use Azure Functions or Logic Apps to periodically clean up expired files from both Azure Blob Storage and the Azure SQL Database.

---

## VM Fleet Commander (Deploy and manage Azure compute resources)
Implement an infrastructure-as-code approach to provision and manage virtual machines in Azure, using ARM templates and Bicep. The aim is to gain hands-on experience in automating the deployment of Azure resources and organizing them efficiently.

- **Programming required?**: ✅ (Knowledge of JSON for ARM templates and Bicep language syntax is essential.)
- **Azure Services Used:**
  - Azure Virtual Machines
  - Azure Resource Manager (ARM)
  - Bicep
  
- **Steps**:

   1. **Initial Setup**:
      - Ensure you have Azure CLI installed with Bicep support.
      - Set up a version control system (e.g., Git) to track changes in your Bicep and ARM templates.

   2. **Bicep Basics**:
      - Start with learning the basics of Bicep syntax and structure.
      - Convert a basic ARM template (like one that deploys a single VM) to Bicep to understand the differences.

   3. **Resource Group and Naming Conventions**:
      - Define a Bicep file to create an Azure Resource Group for your VMs.
      - Implement naming conventions for your resources using Bicep's string functions.

   4. **Virtual Machine Provisioning**:
      - Create a Bicep module for deploying Azure VMs, allowing for parameterized input like VM size, name, and region.
      - Use loops in Bicep to deploy multiple VM instances based on a specified count.

   5. **Network Resources**:
      - Design Bicep modules for associated networking resources like Virtual Network, Subnet, and Network Security Groups.
      - Ensure your VMs are provisioned within the designated VNet and have the necessary security rules applied.

   6. **Parameter Files and Validation**:
      - Create separate parameter files for your Bicep templates, allowing for different environment deployments (e.g., dev, test, prod).
      - Use the Azure CLI to validate your Bicep files before deploying, catching any structural errors.

   7. **Deployment**:
      - Use the Azure CLI to deploy your Bicep templates, creating all designated resources.
      - Test the reproducibility by deploying the same infrastructure to a different region or resource group.

   8. **Maintenance & Updates**:
      - Make changes to your Bicep files (e.g., VM size or count) and redeploy. Observe how Azure handles updates and maintains state.
      - Regularly pull updates to the Bicep language and Azure CLI to stay updated with new features and improvements.

   9. **Documentation & Cleanup**:
      - Document your Bicep modules, their purpose, and any parameters required.
      - After testing, ensure to delete resources or resource groups to avoid incurring unnecessary costs.




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

## Azure InsightScape (Monitor and back up Azure resources)
Design a comprehensive monitoring dashboard to gain insights, troubleshoot, and ensure smooth operations for all your previous projects. With this centralized monitoring solution, track the health, performance, and security of all integrated services.

- **Programming required?**: ❌ (This project relies mostly on configuration and integration, though understanding of Kusto Query Language (KQL) will be essential for custom monitoring queries.)
- **Azure Services Used:**
  - Azure Monitor
  - Azure Log Analytics
  - Azure Security Center
  - Azure Alerts
  - Azure Application Insights (for the web applications)
  - Azure Network Watcher (for networking projects)
  
- **Steps**:
   1. **Azure Monitor Integration**:
        - Set up Azure Monitor to collect telemetry data from all your Azure resources involved in the previous projects.
        - Enable multi-resource monitoring to see health and metrics across projects and services.

   2. **Log Analytics Workspace**:
        - Provision a Log Analytics workspace in Azure Monitor.
        - Integrate your services (like VMs, Web Apps, Logic Apps, Blob Storage) from previous projects into this workspace.
        - Write KQL queries to fetch specific log data, e.g., failed login attempts, high resource utilization, or abnormal network traffic patterns.

   3. **Application Insights**:
        - For the "ShareSafely - File Share Web App" project, integrate Azure Application Insights to capture telemetry data like user sessions, page views, and exceptions.
        - Visualize the performance of your web application and identify any bottlenecks or issues.

   4. **Network Monitoring**:
        - Use Azure Network Watcher to monitor the networking aspects from the "NetMaze Explorer" project.
        - Capture network packet data, check for any security threats, and analyze network topology.

   5. **Security & Compliance**:
        - Integrate Azure Security Center to get a unified view of the security posture across all projects.
        - Ensure compliance standards are met and get recommendations to improve the security of your resources.

   6. **Alerts Configuration**:
        - Based on the data from Log Analytics and Application Insights, set up Azure Alerts.
        - Configure notifications for unusual activities, like resource downtimes, security breaches, or performance degradation.

   7. **Dashboard Creation**:
        - Customize the Azure Monitor dashboard to display critical metrics, logs, and alerts for all projects in one place.
        - Share the dashboard with your team to ensure everyone has visibility into the system's health.

   8. **Backup and Disaster Recovery**:
        - Set up periodic backups for critical data across your projects.
        - Design a disaster recovery plan, and periodically test the recovery of services to ensure data integrity and availability in case of any failures.

   9. **Documentation & Best Practices**:
        - Document your monitoring strategies, KQL queries, and setup configurations.
        - Ensure you follow Azure's best practices for monitoring and alerting, optimizing costs, and resource usage.




