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

- ➡️Enter a name and description (optional) for your connector <img width="926" alt="Connect Basic Details " src="https://github.com/sunny4lab-project/-Automate-Microsoft-Azure-Asset-Inventory-using-Qualys/assets/139194279/e60f414f-943b-4100-9317-2e59b1e714d8">


# - 🧭Navigate to Azure Integration:

The integration between Qualys and Microsoft Azure typically involves the configuration of Azure connectors in Qualys. This integration allows Qualys to gather information about your Azure resources for security and compliance assessments. 

ℹ️Setting up Authentication in Azure connectors in Qualys requires that you provide the necessary Azure credentials, including Subscription ID, Application (Client ID, Client Secret, and Directory (Tenant) ID.

# Here are the key steps and components involved in Azure integration with Qualys:

- 🖥️Locate the Azure integration settings in Qualys.
- 🧰Configure Azure Connection:

- ☑️Enter Azure credentials and establish a secure connection between Qualys and your Azure subscription.
  <summary>Click Here for Details</summary>
