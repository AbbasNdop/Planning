Planning Phase

The planning phase involves gathering and preparing the necessary resources for the project. The Resource Group Name for this Project will be ReVMspinUpAZ, the Virtual Network name: is VNetVMspinUpAZ and the VM name will be VMspinUpAZ. Key steps include:

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

     A: Step by Step on how to Perform the Network Infrastructure Setup: 
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
  4. Configure the firewall settings as needed.
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


