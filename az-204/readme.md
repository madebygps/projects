# Projects for AZ-204

[![Video Name](https://img.youtube.com/vi/Ny5SZcV7mbE/hqdefault.jpg)](https://youtu.be/Ny5SZcV7mbE)

[Study guide for Exam AZ-204: Developing Solutions on Microsoft Azure](https://learn.microsoft.com/certifications/resources/study-guides/az-204)

![diagram of 4 projects](az2024.png)

### 1\. Develop Azure compute solutions (25--30%)

-   Azure Container Registry
-   Azure Container Instance
-   Azure Container Apps
-   Azure App Service Web Apps
-   Azure Functions

### 2\. Develop for Azure storage (15--20%)

-   Azure Cosmos DB
-   Azure Blob Storage

### 3\. Implement Azure security (20--25%)

-   Microsoft Identity platform (for user authentication and authorization)
-   Microsoft Azure Active Directory (Azure AD)
-   Microsoft Graph (for solutions that interact with it)
-   Azure Key Vault (for securing app configuration data)
-   Managed Identities for Azure resources

### 4\. Monitor, troubleshoot, and optimize Azure solutions (15--20%)

-   Azure Cache for Redis (for caching solutions)
-   Azure Content Delivery Network (Azure CDN)
-   Application Insights (for troubleshooting solutions)

### 5\. Connect to and consume Azure services and third-party services (15--20%)

-   Azure API Management (APIM)
-   Azure Event Grid
-   Azure Event Hub
-   Azure Service Bus
-   Azure Queue Storage queues

# Projects

## 1. Weather Tracker (Develop Azure compute solutions)

A web application that allows users to track weather updates in real-time for their chosen cities. The system also triggers Azure Functions for alerts when a specific weather threshold is met (like if it's going to rain).

### Infrastructure
- Azure App Service Web App (Hosting the web application)
- Azure Container Registry (Storing Docker images for the app)
- Azure Container Instance (Running the containers for development/testing)
- Azure Functions (Weather alert system)
- Azure Container Apps (Running the containers in production)

### Diagram

```
User 
|-> Web Application (Hosted on Azure App Service Web App)
   |-> Weather Alerts (Azure Functions)
      |-> Docker Images (Azure Container Registry)
         |-> Testing Containers (Azure Container Instance)
            |-> Running Containers (Azure Container Apps)
```


### Implementation Guide 
1. Create an Azure App Service Web App.
2. Develop a basic web application that uses weather APIs.
3. Containerize the application.
4. Publish the container image to Azure Container Registry.
5. Test the application using Azure Container Instance.
6. Implement an Azure Function to send alerts when a specified weather threshold is met.
7. Integrate Azure Function with your web application.
8. Deploy the web application to Azure Container Apps.
9.  Setup a CI/CD pipeline for your application and Function.
10. Setup Application insights and Azure monitor
11. Push to GitHub 
12. Document

## 2. Azure Document Vault with Expiry & CDN Integration (Develop for Azure storage)

A secure platform where users can upload important documents, assign tags for easier organization, and retrieve them. This enhanced system integrates expiration dates on shared links and utilizes Azure CDN to deliver content efficiently to users across various regions.

### Infrastructure

-   Azure Blob Storage (For storing documents)
-   Azure Cosmos DB (For metadata, tags, and expiring link details)
-   Azure Functions (To handle link expiration logic)
-   Azure CDN (To efficiently deliver documents)

### Diagram 

```
[Users]
  |
  V
[Document Upload, Tagging, and Link Generation Portal]
  |    /        \         |
  |   /          \        |
  V  V            V       V
[Azure Blob Storage]--[Azure CDN]--[Azure Cosmos DB]--[Azure Functions]
```

### Implementation Guide

1.  Design Document Uploader Interface:
    -   Create a user-friendly interface for document uploads and tagging.
2.  Azure Blob Storage Setup:
    -   Set up Azure Blob Storage containers for document storage.
    -   Implement authentication and authorization.
3.  Azure Cosmos DB Integration:
    -   Initialize Azure Cosmos DB.
    -   Store metadata for each document upload, like the upload date, document type, user ID, and tags.
4.  Develop Document Upload and Tagging Portal:
    -   Build a portal where users can upload and tag documents.
    -   Use SDKs to communicate with Blob Storage and Cosmos DB.
5.  Develop Expiration Logic with Azure Functions:
    -   Allow users to generate unique download URLs with set expiration dates.
    -   The function will store the URL, associated document reference, and expiration in Cosmos DB.
6.  Modify Document Retrieval:
    -   Check the URL's validity and serve the document either directly from Azure Blob Storage or via Azure CDN.
7.  Setup Azure CDN:
    -   Create a CDN profile and endpoint.
    -   Link it to Azure Blob Storage.
8.  Modify Document Serving Logic with CDN:
    -   Use Azure CDN to cache and deliver documents, enhancing the retrieval speed.
9.  Manage Cache Lifespan:
    -   Set appropriate TTL (Time to Live) for cached documents on CDN.
10. Setup a CI/CD pipeline for your application and Function.
11. Setup Application insights and Azure monitor
12. Push to GitHub 
13. Document



## 3. Secret Notes Viewer (Implement Azure security)

A web application that displays secret notes from Azure Keyvault only when the user logins. 

### Infrastructure

-   Microsoft Azure Active Directory (User authentication)
-   Azure Key Vault (Storing sensitive data)
-   Azure App Service (Hosting the portal)

### Diagram

```
User 
|-> Login Portal (Hosted on Azure App Service)
   |-> User Authentication (Microsoft Azure Active Directory)
   |-> Configuration Data (Azure Key Vault)
```

### Implementation Guide

1.  Set up an Azure AD instance for user authentication.
2.  Create several test users in Azure AD.
3.  Create several secrets in Azure KeyVault.
4.  Assign permissions to users in Azure AD such that each user has access to different secrets.
5.  Develop a web application that integrates with Azure AD for login functionality.
6.  Integrate Azure Key Vault in the application to fetch configuration data.
7.  Display the information in the web app once user logins.
8.  Deploy the application on Azure App Service.
9.  Setup a CI/CD pipeline for your application
10. Setup Application insights and Azure monitor
11. Push to GitHub 
12. Document


## 4. Event-Driven Bookstore Notification System (Connect to and consume Azure services and third-party services)


An event-driven bookstore application that notifies subscribers when a new book is added to the inventory. This system integrates Azure's event-based and message-based solutions to handle the real-time notifications.

###  Infrastructure

-   Azure API Management (APIM): To manage and secure the API endpoints.
-   Azure Event Grid: To trigger events when new books are added.
-   Azure Service Bus: To send out notification messages to subscribers.
-   Azure Cosmos DB: To store book inventory and subscriber details.

### Diagram 

```
[Bookstore Application]
      |
      V
[Azure API Management (APIM)]
      |
      V
[Azure Cosmos DB] <--> [Azure Event Grid]
      |
      V
[Azure Service Bus]
      |
      V
[Subscriber Devices]
```

### Implementation Guide

1.  Initialize Azure API Management (APIM):

    -   Set up an APIM instance.
    -   Create and secure API endpoints to add books and register subscribers.
2.  Design Bookstore Inventory System:

    -   Store new book entries in Azure Cosmos DB.
    -   When a book is added, trigger an event in Azure Event Grid.
3.  Set Up Azure Event Grid:

    -   Configure it to watch for new book additions in Azure Cosmos DB.
4.  Notification Mechanism with Azure Service Bus:

    -   When an event is triggered by a new book addition, push a notification message into Azure Service Bus.
    -   Subscribers will pull their notifications from here.
5.  Subscriber Management in Azure Cosmos DB:

    -   Store details of subscribers.
    -   Maintain a list of books they are notified about, to prevent duplicate notifications.

### Additional Details:

Adding Books and Triggering Events:

-   When a new book is added through the API, the data is stored in Azure Cosmos DB.
-   This addition triggers an event in Azure Event Grid.

Notification to Subscribers:

-   Azure Event Grid, upon capturing the event, instructs Azure Service Bus to send out a notification.
-   Subscribers retrieve their notifications from Azure Service Bus, ensuring they are in3wsamed of the new book.
