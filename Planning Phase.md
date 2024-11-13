Planning Phase

The planning phase involves gathering and preparing the necessary resources for the project. 
Key Resources:
- The Resource Group Name: ReVMspinUpAZ
- The virtual Network name: VNetVMspinUpAZ
-  The VM name: VMspinUpAZ.
-  Subnet Name: SubVNetVMspinUpAZ
-  Firewall Name:  FVMspinUpAZ

     Key steps include:

A. Network Infrastructure Setup:
   - Create a Virtual Network (VNet) and subnet  
   - Set up Firewall and Application Gateway (Layer 7) for traffic management  
   - Configure a Network Security Group (NSG) for the subnet to control inbound and outbound traffic  
   - Use CIDR to determine the VNet size  
   - Create a Resource Group to organize related resources  

B. Network Configuration Confirmation:  
   - Confirm network settings with the developer, focusing on **inbound** and outbound traffic requirements

C. Resource Cost Estimation:  
   - Estimate resource costs and ensure they stay within the project's budget

D. Topology Design:  
   - Create a network topology diagram for better visualization and planning






A: Step-by-step Guide on how to Perform Network Infrastructure Setup.
     
 1. Creating a Resource Group
- Name: ReVMspinUpAZ
- Purpose: Organize all related resources for easy management.
- Steps: 
  1. Go to the Azure portal.
  2. Navigate to "Resource Groups."
  3. Click "Add" and fill in the details (name, region).
  4. Click "Review + Create" and then "Create."

 2. Creating a Virtual Network (VNet) and Subnet
- VNet Name: VNetVMspinUpAZ
- Subnet Name: SubVNetVMspinUpAZ
- Steps:
  1. In the Azure portal, go to "Create a resource."
  2. Search for "Virtual Network" and select it.
  3. Click "Create" and fill in the details:
     - Resource Group: ReVMspinUpAZ
     - Name: VNetVMspinUpAZ
     - Address space: Use CIDR notation to define the size (e.g., 10.0.0.0/16). For this project, I used /16 because it allows for up to 65,536 IP addresses, providing plenty of room for growth. It offers flexibility to create multiple smaller subnets, reduces the risk of IP conflicts, and ensures I won't need to reconfigure.
  4. Add a subnet:
     - Name: SubVNetVMspinUpAZ
     - Subnet address range: Use CIDR notation (e.g., 10.0.1.0/16).
  5. Click "Review + Create" and then "Create."

 3. Set Up Firewall and Application Gateway (Layer 7)
- Purpose: Manage and secure traffic.
- Steps:
  1. In the Azure portal, go to "Create a resource."
  2. Search for "Firewall" and select it.
  3. Click "Create" and fill in the details:
     - Resource Group: ReVMspinUpAZ
     - Name: FVMspinUpAZ
  4. Configure the firewall settings as needed and Firewall policy as needed.
  5. Repeat the process for the Application Gateway.

 4. Configure a Network Security Group (NSG)
- Purpose: Control inbound and outbound traffic on the Subnet.
- Steps:
  1. In the Azure portal, go to "Create a resource."
  2. Search for "Network Security Group" and select it.
  3. Click "Create" and fill in the details:
     - Resource Group: ReVMspinUpAZ
     - Name:  NSGVMspinUpAZ.
  4. Add inbound and outbound security rules as needed.
  5. Associate the NSG with the subnet (SubVNetVMspinUpAZ).
  Set Up Azure Bastion:

Purpose: Provide secure and seamless RDP/SSH connectivity to the VM.
Steps:
In the Azure portal, go to "Create a resource."
Search for "Bastion" and select it.
Click "Create" and fill in the details:
Resource Group: ReVMspinUpAZ
Name: BAVMspinUpAZ
Virtual Network: VNetVMspinUpAZ
Configure the subnet for Bastion (typically named "AzureBastionSubnet").
Click "Review + Create" and then "Create." 





  B. Network Configuration Confirmation:
Here, I will

1. Review Network Settings: Go over the current network settings, including the Virtual Network (VNet), subnets, and Network Security Groups (NSGs) with the developer.
2. Discuss Traffic Requirements: Confirm with the developer the specific inbound and outbound traffic requirements, such as which ports need to be open (e.g., HTTP, HTTPS, RDP, etc.).
3. Adjust Configurations: Make any necessary adjustments to the NSGs or firewall rules based on the developer's feedback.
4. Document Changes: Keep a record of any changes made for future reference and troubleshooting.





C. Resource Cost Estimation:
Here, I will,

1. Identify Resources: List all the resources I'll be using, such as VMs, storage, networking components, and any additional services.
2. Use Azure Pricing Calculator: Go to the Azure Pricing Calculator and input the details of each resource to get an estimate.
3. Review Costs: Compare the estimated costs with my project's budget to ensure they align.
4. Adjust as Needed: If the costs exceed the budget, consider adjusting the resource specifications or exploring cost-saving options.
5. Document Estimates: Keep a record of the cost estimates for future reference and budget tracking.





D: Topology Design:

![image](https://github.com/user-attachments/assets/1dc8f471-8b86-4e2c-8edb-411465273e47)





