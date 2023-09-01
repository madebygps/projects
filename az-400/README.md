# Projects for AZ-400

[![Video Name]()]()

[Study guide for Exam AZ-400: Designing and Implementing Microsoft DevOps Solutions](https://learn.microsoft.com/certifications/resources/study-guides/az-400)

The AZ-400 exam measures an individual's expertise in designing and implementing DevOps practices using Azure DevOps and Microsoft Azure tools. The exam evaluates five core skill sets: configuring processes and communications for traceability and workflow; designing and implementing source control strategies including branching and repository management; building and managing release pipelines with considerations for automation, package management, and testing; developing a security and compliance plan focused on sensitive information management and automated scanning; and implementing an instrumentation strategy for monitoring and metrics analysis. Each skill set ensures that the candidate is proficient in optimizing the entire software development lifecycle for Azure applications.

# Hands-on Projects

## 1. TraceableTribe (Configure Processes and Communications)

### Skills Practiced

- Configure activity traceability and flow of work
- Configure collaboration and communication

### Project Description

In this project, you'll integrate Azure Boards, GitHub Actions, and Azure Pipelines to manage the flow of work items from creation to completion. You'll also implement custom dashboards for actionable insights, document the project with wikis and diagrams, and automate notifications and release documentation.

### Diagram description

A flowchart illustrating the integration of Azure Boards, GitHub Actions, and Azure Pipelines. The chart will show how work items move from 'To Do' to 'Done' and how code changes trigger pipeline actions and update the board.

### Programming required?: ✅

### Azure Services Used

- Azure Boards
- Azure Pipelines
- GitHub Actions
- Azure Monitor

### Steps

1.  Initial Setup:

    -   Create a new project in Azure DevOps.
    -   Initialize a new repository on GitHub.
2.  Azure Boards Configuration:

    -   Enable Azure Boards and create a backlog.
    -   Create different work item types like User Stories, Bugs, and Tasks.
3.  Repository Integration:

    -   Integrate the GitHub repository with Azure Boards.
4.  Workflow Automation:

    -   Create a GitHub Actions workflow that triggers on pull request events.
    -   Integrate this workflow to update work item status in Azure Boards.
5.  Azure Pipelines Configuration:

    -   Set up a build and release pipeline in Azure Pipelines.
    -   Connect this pipeline to your GitHub repository.
    -   Implement traceability by linking pipeline runs to work items.
6.  Metrics and Dashboards:

    -   Use Azure Boards to create a custom dashboard.
    -   Include widgets for cycle time, lead time, and other flow metrics.
7.  Documentation and Diagrams:

    -   Create a Wiki in Azure DevOps to document the project.
    -   Use a tool like draw.io to create process diagrams and embed them in the Wiki.
8.  Release Documentation:

    -   Configure the Azure Pipeline to generate release notes and API documentation automatically.
    -   Integrate this documentation into your project Wiki.
9.  Notification Automation:

    -   Set up webhook notifications to inform team members about key events, such as work item updates or pipeline failures.
10. Review and Test:

    -   Review the entire setup for traceability and communication.
    -   Perform a dry-run to validate that everything is working as expected.

## 2. BranchMaster: The Ultimate Source Control Hub (Design and Implement Source Control)

### Skills Practiced

- Design and implement a source control strategy
- Plan and implement branching strategies for the source code
- Configure and manage repositories

### Project Description

In this project, you'll set up a Git-based source control system using Azure Repos or GitHub, then implement advanced strategies for authentication, branching, and data recovery. You'll use Git hooks for workflow automation and will integrate with Azure Pipelines for CI/CD.

### Diagram description

A flow diagram depicting the branching strategy (trunk, feature branches, release branches), the integration with Azure Pipelines, and the workflow hooks triggering various actions.

### Programming required?: ✅

### Azure Services Used

- Azure Repos or GitHub for source control
- Azure Pipelines for CI/CD
- Azure Active Directory for authentication

### Steps

1.  Initial Repository Setup:

    -   Create a new Git repository in Azure Repos or GitHub.
2.  Authentication Strategy:

    -   Implement SSH key-based authentication for the repository.
    -   Optionally, integrate with Azure Active Directory.
3.  Large Files Management:

    -   Integrate Git LFS (Large File Storage) to handle large files.
4.  Optimization Strategy:

    -   Implement Git Scalar to speed up operations in your repository.
5.  Workflow Hooks:

    -   Implement pre-commit and post-commit hooks to automate workflows, such as code linting or issue linking.
6.  Branching Strategy:

    -   Create a trunk-based development model with separate branches for features and releases.
7.  Pull Request Workflow:

    -   Implement branch policies for pull requests to enforce code reviews, build validation, and other checks.
8.  Branch Protections:

    -   Implement restrictions on merging to protect important branches like 'main' or 'release'.
9.  Azure Pipelines Integration:

    -   Link your Azure Repos or GitHub repository to an Azure Pipeline for continuous integration and deployment.
10. Repository Management:

    -   Configure repository permissions to control access.
    -   Use tags to mark important milestones or versions.
    -   Learn Git commands to recover lost commits or data.
    -   Implement strategies to purge sensitive or unnecessary data from the repository history.
11. Test the Setup:

    -   Simulate a workflow that takes a feature from a feature branch through a pull request, triggers the Azure Pipeline, and merges into the main trunk.

## 3. PipelinePalooza: A Comprehensive CI/CD Masterclass (Design and Implement Build and Release Pipelines)

### Skills Practiced

-   Designing and implementing pipeline automation
-   Package management strategy
-   Job execution order, parallelism, and multi-stage
-   Deployments with various strategies
-   Infrastructure as Code (IaC)
-   Maintaining pipelines

### Project Description

In this project, you will design and implement a comprehensive CI/CD pipeline using Azure Pipelines and GitHub Actions. The pipeline will integrate various tools for code quality, package management, and deployments. You will also practice Infrastructure as Code (IaC) and implement monitoring and optimization for the pipeline.

### Diagram description

The diagram will consist of multiple stages representing code building, automated testing, package management, deployment strategies, and monitoring. Each stage will be integrated with different tools and Azure services.

### Programming required?: ✅

### Azure Services Used: 

- Azure Pipelines
- Azure Repos or GitHub
- Azure Artifacts
- Azure App Configuration Feature Manager
- Azure Resource Manager
- Azure Automation State Configuration
- Azure Traffic Manager
- Azure App Service

### Steps

1.  Initial Setup:

    -   Create a new Git repository in Azure Repos or GitHub.
    -   Setup an Azure Pipeline for the repository.
2.  Pipeline Automation:

    -   Integrate code quality tools such as SonarQube.
    -   Implement automated testing, including unit tests, integration tests, and UI tests.
    -   Design and implement quality and release gates.
3.  Package Management Strategy:

    -   Set up Azure Artifacts and create feeds for NuGet and npm.
    -   Implement a package versioning strategy.
4.  Pipeline Design:

    -   Use YAML to define pipeline stages, jobs, and steps.
    -   Implement triggers for the pipeline based on your workflow.
5.  Job Execution Order:

    -   Design the pipeline for parallel execution where possible.
    -   Create reusable elements such as task groups and variable groups.
6.  Deployment Strategies:

    -   Implement blue/green and canary deployments.
    -   Use Azure Traffic Manager for load balancing.
    -   Implement feature flags using Azure App Configuration Feature Manager.
7.  Infrastructure as Code:

    -   Implement IaC using Azure Resource Manager templates or Bicep.
    -   Create a desired state configuration using Azure Automation State Configuration.
8.  Pipeline Maintenance:

    -   Monitor pipeline health using Azure Monitor or other tools.
    -   Implement a retention strategy for pipeline artifacts.
9.  Testing and Verification:

    -   Run several builds and deployments to verify the entire pipeline workflow.
10. Optimization:

    -   Analyze the pipeline load and optimize for performance and cost.


### 4. SecureIt: Azure Vault of Secrets (Developing a Security and Compliance Plan)

### Skills Practiced

-   Managing sensitive information in automation
-   Automating security and compliance scanning

### Project Description

In this project, you will be focusing on creating a secure and compliant CI/CD pipeline for a sample application. You'll manage sensitive information like secrets, keys, and tokens securely, and you'll also integrate automated security and compliance scanning into the pipeline. This project aims to provide a working model of how to implement best practices for securing pipelines and code.

### Diagram description

The diagram will consist of multiple components such as Source Control, Azure Pipelines, Azure Key Vault, GitHub Secrets, and various scanning tools like SonarQube, GitHub Code Scanning, and OWASP ZAP. Each component will interact securely to prevent leakage of sensitive information.

### Programming required?: ✅

### Azure Services Used

- Azure Pipelines
- Azure Key Vault
- Azure Monitor

### Steps:

1.  Initial Setup:

    -   Create a new repository for your sample application.
    -   Set up an Azure Pipeline for this repository.
2.  Managing Sensitive Information:

    -   Integrate Azure Key Vault to manage secrets and keys.
    -   Use GitHub secrets for repository-specific sensitive information.
    -   Implement and manage service connections and personal access tokens securely.
3.  Pipeline Configuration for Sensitive Files:

    -   Design your pipeline to handle sensitive files securely during the build and release phases.
    -   Implement strategies to prevent the leakage of sensitive information.
4.  Automate Code Scanning:

    -   Integrate GitHub Code Scanning and SonarQube into the pipeline for static code analysis.
5.  Automate Security Scanning:

    -   Implement container scanning and OWASP ZAP for dynamic security scanning.
6.  Automate Compliance Scanning:

    -   Use tools like Mend Bolt and GitHub Dependency Scanning to automatically analyze licensing, vulnerabilities, and versioning of open-source components.
7.  Monitoring and Logging:

    -   Use Azure Monitor to keep track of all activities, especially the access and use of secrets and tokens.
8.  Pipeline Testing:

    -   Run several builds and releases to ensure all security and compliance checks are functioning as expected.
9.  Documentation:

    -   Document all configurations, scanning results, and any manual steps necessary for maintaining security and compliance.
10. Review and Optimization:

    -   Conduct a review of the configurations to make sure they align with security best practices.
    -   Optimize where necessary.


## 5. EyeOnIt: Azure Metrics Maestro (Implementing an Instrumentation Strategy)

### Skills Practiced

-   Configuring monitoring for a DevOps environment
-   Analyzing metrics and interpreting logs

### Project Description

In this project, you will set up monitoring and analytics for a DevOps environment using Azure Monitor and Azure Application Insights. You will define key application and infrastructure performance indicators, set up alerts for pipeline events, and analyze metrics using Kusto Query Language (KQL).

### Diagram description

The diagram should include the application, Azure Pipelines, Azure Monitor, and Azure Application Insights. It should show data flow from the application to Azure Monitor and Azure Application Insights. User interactions triggering Application Insights should also be indicated.

### Programming required?: ✅

### Azure Services Used

- Azure Monitor
- Azure Application Insights
- Azure Pipelines

### Steps:

1.  Initial Setup:

    -   Create a new repository for a sample application (e.g., a simple web application).
    -   Create an Azure Pipeline for CI/CD for the sample application.
2.  Configuring Monitoring Tools:

    -   Set up Azure Monitor and Azure Application Insights for the sample application.
    -   Integrate these services with Azure Pipelines.
3.  Access Control:

    -   Configure who has access to Azure Monitor and Application Insights.
4.  Setting Up Alerts:

    -   Configure alerts in Azure Monitor for various pipeline events (build failure, deployment failure, etc.).
5.  Setting Up Key Performance Indicators (KPIs):

    -   Identify and set up application KPIs in Application Insights (e.g., page load time).
    -   Identify and set up infrastructure KPIs in Azure Monitor (e.g., CPU usage, disk usage).
6.  Analyze Metrics:

    -   Inspect application performance using Application Insights.
    -   Inspect infrastructure performance using Azure Monitor.
7.  Business Metrics:

    -   Set up and monitor metrics that are aligned with business value, like user engagement.
8.  Kusto Query Language (KQL):

    -   Use basic KQL queries to interrogate logs for deeper insights.
9.  Testing:

    -   Use the application to generate metrics and ensure that all KPIs and alerts are working as expected.
10. Documentation:

    -   Document the monitoring setup, key metrics, and any custom KQL queries you've created.