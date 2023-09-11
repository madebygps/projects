# ShareSafely - File Share Web App (Implement and manage storage

Create a web application where users can securely upload files to Azure Blob Storage. Once uploaded, the application generates a unique, time-limited link for the user to share. This ensures that only authorized users with the link can access the uploaded file for a specified duration.

- **Programming required?**: ✅ (For creating the web application and generating unique time-limited links.)
  
- **Azure Services Used:**
  - Azure Blob Storage
  - Azure Web Apps
  - Azure KeyVault

  
- **Steps**:
   1. **Storage Setup**:
        - Set up an Azure Blob Storage account and create a container to store the uploaded files.
        - Configure appropriate security settings, ensuring data at rest encryption is enabled.
   
   2. **Web Application Deployment**:
        - Develop a web application that allows users to upload files. This can be done using preferred frameworks (like ASP.NET Core, Node.js, etc.).
        - Deploy the application to Azure Web Apps.
   
   3. **File Upload Logic**:
        - In the web application, integrate Azure Blob Storage SDKs/APIs to facilitate the file upload process directly to Blob Storage.
   
   
   4. **Unique Link Generation**:
        - When a file is uploaded, use Azure Storage SDK to generate a unique, time-limited link for the user.

   
   5. **Secure Credentials**:
        - Store any sensitive credentials or configuration strings (like Blob Storage access keys) securely in Azure Key Vault.
        - Integrate Azure Key Vault with the web application to retrieve these credentials when needed.
   
   6. **Monitoring and Cleanup**:
        - Set up monitoring to track file upload/download activities.
        - Use Azure Functions or Logic Apps to periodically clean up expired files from both Azure Blob Storage and the Azure SQL Database.

---