# Projects for AZ-104

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
Deploy a series of virtual machines with varying configurations, storage, and networking setups. These VMs will be scaled and balanced based on traffic/load.
- **Programming required?**: ❌
- **Azure Services Used:**
    - Azure Virtual Machines
    - Azure Disk Encryption
    - Azure Virtual Machine Scale Sets
    - Azure Load Balancer
- **Steps:**
   1. Initialize a virtual machine with the desired OS and settings.
   2. Apply Azure Disk Encryption for VM data protection.
   3. Design a Virtual Machine Scale Set (VMSS) to manage multiple VMs with scalability.
   4. Implement an Azure Load Balancer to distribute incoming traffic to the VMs.
   5. Simulate traffic to observe and test the scalability and load balancing.

---

## NetMaze Explorer (Implement and manage virtual networking)
Design a hybrid networking environment where on-premises networks connect securely to Azure resources, ensuring secure data transition and effective resource access controls.
- **Programming required?**: ❌
- **Azure Services Used:**
    - Azure Virtual Networks
    - Azure VPN Gateway
    - Network Security Groups (NSGs)
    - Azure Bastion
    - Azure Private Link
    - Azure DNS
    - Azure Load Balancer
- **Steps:**
   1. Set up an Azure Virtual Network with subnets.
   2. Create a VPN connection between a simulated on-premises network and Azure using the VPN Gateway.
   3. Place test resources in each subnet.
   4. Assign NSG rules for secure access between subnets.
   5. Integrate Azure Bastion for secure, direct VM access.
   6. Use Azure Private Link to create private connections to Azure PaaS services.
   7. Configure Azure DNS for domain name resolution.
   8. Implement Azure Load Balancer for distributing traffic to resources.

---

## Azure InsightScape (Monitor and maintain Azure resources)
Establish a monitoring and backup solution to oversee the health, performance, and resilience of your Azure environment.
- **Programming required?**: ❌
- **Azure Services Used:**
    - Azure Monitor
    - Azure Alerts
    - Azure Backup
    - Azure Site Recovery
    - Azure Network Watcher
    - Azure Advisor
    - Azure Log Analytics
- **Steps:**
   1. Set up foundational Azure resources.
   2. Configure Azure Monitor for real-time metrics.
   3. Establish a Log Analytics workspace for in-depth data inspection.
   4. Define specific alerts using Azure Alerts.
   5. Integrate Azure Network Watcher for network insights.
   6. Create backup policies and implement Azure Backup.
   7. Design disaster recovery strategies using Azure Site Recovery.
   8. Test recovery methods and disaster response.
   9. Gain insights from Azure Advisor for optimization.
   10. Customize Azure Monitor dashboards for at-a-glance resource health.

