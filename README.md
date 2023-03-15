# Update-Management

# What is the purpose of Update Management for Virtual Machines?
- Azure Update Management Service allows companies to manage the deployment of updates on Windows and Linux servers/virtual machines from a single location - for both on-premises envionrment AND Azure environments
- Update Management is available at no additional cost (companies only pay for the log data that Azure Log Analytics stores), and companies can easily enable it for Azure and on-premises Virtual Machines.


# Benefits
- Simple and easy to configure
- An up-to-date machine provides a secure environment. Think of security in layers.

# What is required to implement Update Management?
- Companies would need to install Log Analytics Agent for Windows and Linux needs to be installed on the Azure VMs or manually on their on-premises machines in order to enable the virtual machines with Update Management.
- Data would be sent to a Log-analytics workspace and update management service would understand the data and see what is missing from the machines
- Scans can be performed for Linux or Windows machines
- From there, Azure Automation account can be responsible for updating the machines
- This service just ensures that all the machines are patched and up-to-date!


# Update Management Setup
- Spin up two machines based on Windows and Linux 
- Create an Azure Automation Account, which is responsible for applying the updates. Only some regions are supported.
- Create a log-analytics workspace.


# Set up two Virtual Machines - One Windows and one Linux in a different virtual network

# Connect the analytics workspace to the automation account
- Navigate to update management and add the virtual machines 

- Windows Machine in a different vnet
<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/172025447-23b9e29b-f2b3-436c-a142-638e2b6d5336.png" height="65%" width="65%" alt="application gateway"/>

<p/>

- Linux Ubuntu machine in a different vnet
<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/172025461-e77c3ff0-00ba-43e3-ac43-1b226bc8e776.png" height="65%" width="65%" alt="application gateway"/>

<p/>

# Create an Automation account 
- This automation account will link the Linux Virtual Machines and Windows Virtual Machines and apply the updates

<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/172034359-72248d84-619f-4668-8624-2f4b060171bd.png" height="65%" width="65%" alt="application gateway"/>

<p/>



# Dynamic Groups
- Admins can update machines based on certain conditions
- It can be based on machines within a particular resource groups or location or tags!
- Instead of manually adding virtual machines



# Alternative to Update Management - Automatic VM Guest Patching
- This service auto-updates your Azure Virtual Machines during off-peak hours.
- Update Management uses the Azure Automation service to provide updates.
