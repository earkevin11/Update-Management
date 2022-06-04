# Update-Management

What is the purpose of Update Management for Virtual Machines?
- Service allows companies to manage the deployment of updates on virtual machines within on-premises envionrment or Azure Virtual Machines
- Companies would need to install log analytics agent on Azure VMs or manually on on-premises machines
- Data would be sent to a Log-analytics workspace and update management service would understand the data and see what is missing from the machines
- Scans can be performed for Linux or Windows machines
- From there, Azure Automation account can be responsible for updating the machines
- This service just ensures that all the machines are patched and up-to-date!


# Update Management Setup
- Spin up two machines based on Windows and Linux 
- Create an Azure Automation Account, which is responsible for applying the updates. Only some regions are supported.
- Create a log-analytics workspace.


# Connect the analytics workspace to the automation account
- Navigate to update management


