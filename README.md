# -Automate Microsoft Azure Asset Inventory using Qualys: Streamlining Security and Compliance

Managing a comprehensive asset inventory in Microsoft Azure is critical for effective security and compliance. By integrating Qualys, a leading cybersecurity solution, you can automate the asset inventory process, ensuring real-time visibility into your Azure environment. This guide outlines the steps to automate Microsoft Azure asset inventory using Qualys.

# -Deploying Azure Connector 🖱️

Set up Microsoft Azure connectors to collect resource information from your Azure account. You can establish an Azure Connector through AssetView and TotalCloud, as detailed in the prerequisites section<details> <summary> Click here for details</summary>
# -Pre-requisites :smile:
Before you create an Azure connector, ensure that you have the following permissions:
 - :book:Assign Azure Active Directory permissions to register an application with your Azure
Active Directory
- :book:Checking Azure Subscription Permissions to assign the application to a role in your
Azure subscription</details>
This process only requires a few minutes. Now, let's explore the permissions required to create an Azure connector.<details>
# -Step 1: Integration Setup
Access Qualys Platform:

- 👨‍💻Log in to your Qualys account and access the platform.<img width="961" alt="Qualys Login screen " src="https://github.com/sunny4lab-project/-Automate-Microsoft-Azure-Asset-Inventory-using-Qualys/assets/139194279/a7a33272-234d-4c48-9a67-cedb6854de61">

- ➡️Click on the Connector app on the menu bar to your Left.<img width="509" alt="navigate to the connector app" src="https://github.com/sunny4lab-project/-Automate-Microsoft-Azure-Asset-Inventory-using-Qualys/assets/139194279/b24eac47-0b83-4417-9a0e-3fa115e68418">
- ▶️ Select the Cloud service you wish to connect to. In this case it's going to be "Azure Connector" <img width="954" alt="cloud connector selection" src="https://github.com/sunny4lab-project/-Automate-Microsoft-Azure-Asset-Inventory-using-Qualys/assets/139194279/967b5f13-41f0-4259-b0bd-a978818dd8ad">

- ➡️Enter a name and description (optional) for your connector  # <img width="926" alt="Connect Basic Details " src="https://github.com/sunny4lab-project/-Automate-Microsoft-Azure-Asset-Inventory-using-Qualys/assets/139194279/e60f414f-943b-4100-9317-2e59b1e714d8">


# - 🧭Navigate to Azure Integration:

💁 The integration between Qualys and Microsoft Azure typically involves the configuration of Azure connectors in Qualys. This integration allows Qualys to gather information about your Azure resources for security and compliance assessments. 

ℹ️ Setting up Authentication in Azure connectors in Qualys requires that you provide the necessary Azure credentials, including Subscription ID, Application (Client) ID, Client Secret, and Directory (Tenant) ID.

# Here are the key steps and components involved in Azure integration with Qualys:

- ▶️Log on to the Microsoft Azure console and Search "Microsoft Entra ID" <img width="646" alt="Microsoft entra ID search" src="https://github.com/sunny4lab-project/-Automate-Microsoft-Azure-Asset-Inventory-using-Qualys/assets/139194279/29c5a477-67c7-4462-a04d-1bb61db0df2e">

- ▶️ On the Navigation Panel on the left, scroll down and Click App Registrations > New Registration.
<img width="419" alt="App Registration" src="https://github.com/sunny4lab-project/-Automate-Microsoft-Azure-Asset-Inventory-using-Qualys/assets/139194279/8c41640c-a78f-4441-952c-b5bd8f47481c">

- ▶️ Click on the "New Registration" with the + sign. <img width="783" alt="New Registration" src="https://github.com/sunny4lab-project/-Automate-Microsoft-Azure-Asset-Inventory-using-Qualys/assets/139194279/0b76d242-1091-4264-aa24-fb0d55a4d9f0">

- ▶️ Provide the following details: A name for the application and also select the Supported account types: directory for single Tenant, Multi-Tenant. Also, Click on "Register" when done.<img width="749" alt="Register an application" src="https://github.com/sunny4lab-project/-Automate-Microsoft-Azure-Asset-Inventory-using-Qualys/assets/139194279/02076576-5a2e-4620-9142-249e6cf20b1e">
  <details>
  <summary><span style="color: #4CAF50;">Details on Azure Tenant Architecture</span></summary>

  In the context of Microsoft Azure, the terms "single-tenant" and "multi-tenant" refer to the architectural models for deploying and managing applications, services, or resources.

  # <span style="color: #FF5733;">Single-Tenant:</span>

  Definition:
  <span style="color: #FF5733;">Single-Tenant (or Single-Tenancy):</span> In a single-tenant architecture, each instance of an application or service is dedicated to a single customer (tenant). The resources and data associated with that instance are isolated and not shared with other customers.

  # <span style="color: #3370FF;">Characteristics:</span>
  - <span style="color: #3370FF;">Isolation:</span> Each customer has a dedicated and isolated environment.
  - <span style="color: #3370FF;">Customization:</span> Customers have the flexibility to customize and configure the environment according to their specific needs.
  - <span style="color: #3370FF;">Control:</span> Customers have more control over the infrastructure, security, and policies.

  # <span style="color: #FF5733;">Use Cases:</span>
  Single-tenant architectures are often preferred in scenarios where customers require a high level of customization, control, and isolation. Examples include certain compliance requirements, security-sensitive applications, or scenarios where customers have specific regulatory constraints.

  # <span style="color: #3370FF;">Multi-Tenant:</span>

  Definition:
  <span style="color: #3370FF;">Multi-Tenant (or Multi-Tenancy):</span> In a multi-tenant architecture, multiple instances of an application or service share the same resources and infrastructure. Each customer (tenant) remains logically isolated, but they all share a common underlying platform.

  # <span style="color: #FF5733;">Characteristics:</span>
  - <span style="color: #FF5733;">Resource Sharing:</span> Multiple customers share the same set of resources and infrastructure.
  - <span style="color: #FF5733;">Cost Efficiency:</span> Shared resources lead to cost efficiency and resource optimization.
  - <span style="color: #FF5733;">Scalability:</span> Multi-tenant architectures are often more scalable as resources can be dynamically allocated based on demand.

  # <span style="color: #3370FF;">Use Cases:</span>
  Multi-tenant architectures are suitable for scenarios where resource efficiency, scalability, and cost-sharing are priorities. Many cloud services, including Azure, adopt a multi-tenant model, allowing multiple customers to leverage shared infrastructure while maintaining logical isolation.

  # <span style="color: #FF5733;">Azure and Tenancy:</span>
  In Azure Active Directory (Azure AD), tenancy refers to the organization's instance of Azure AD. It can be either a single-tenant (dedicated to a single organization) or a multi-tenant (shared by multiple organizations). Azure AD supports both models.

  # <span style="color: #3370FF;">Azure Services:</span>
  Many Azure services are designed to be multi-tenant by default, allowing multiple customers to use the same underlying infrastructure. However, certain services or deployment options may provide options for dedicated, single-tenant instances.

  Understanding the tenancy model is crucial when designing and deploying applications or services in Azure, as it influences factors such as security, isolation, customization, and cost considerations. The choice between single-tenant and multi-tenant architectures depends on the specific requirements and priorities of the application or service being deployed.
</details>


- ▶️ Navigate to the Registered app by selecting the "all application" button as shown on below
<img width="950" alt="Navigate to App Registration" src="https://github.com/sunny4lab-project/-Automate-Microsoft-Azure-Asset-Inventory-using-Qualys/assets/139194279/54c35a12-29b7-4047-b661-18914a3d8404"> For example: I will select the "IOT" app I created.
- ▶️ Navigate to the Menu panel to your left and select "API Permissions" and then Click on the "Add Permission" button<img width="820" alt="API Permissions1" src="https://github.com/sunny4lab-project/-Automate-Microsoft-Azure-Asset-Inventory-using-Qualys/assets/139194279/f2459961-3d3a-4302-bc81-cc8a0fbb166d">
- ▶️ Select "Azure Service Management"<img width="677" alt="API Request" src="https://github.com/sunny4lab-project/-Automate-Microsoft-Azure-Asset-Inventory-using-Qualys/assets/139194279/a74956b3-9c86-4d78-9537-73bcb4aad6dd">
- ▶️  Select user impersonation permission and click Add permissions. <img width="680" alt="Add Permissions" src="https://github.com/sunny4lab-project/-Automate-Microsoft-Azure-Asset-Inventory-using-Qualys/assets/139194279/932058b8-345d-449b-93b4-4fcd47553a8c">
</details>



