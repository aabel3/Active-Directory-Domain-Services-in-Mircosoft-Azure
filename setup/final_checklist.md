## Final Checklist

Before recording your video, verify:
### Azure Resources:
- [ ] Resource group: MST300-project1-rg created
- [ ] Three VNets created with correct names
- [ ] VNet1 has 2 subnets (including AzureBastionSubnet)
- [ ] VNet2 and VNet3 each have 1 subnet
- [ ] All subnets properly calculated from your /24 assignment
- [ ] Azure Bastion deployed and running
- [ ] All three VMs created and running
- [ ] No public IPs on VMs (only Bastion has public IP)

### Domain Configuration:
- [ ] Domain name: studentID.MST300.com
- [ ] Two users created: studentID and studentID.admin
- [ ] studentID.admin in Domain Admins group
- [ ] studentID in Domain Users group
- [ ] Both webserver-vm and client-vm joined to domain
- [ ] Both VMs appear in AD Computers container

### Network Configuration:
- [ ] All three VNets peered (6 peering connections total)
- [ ] All peering status shows "Connected"
- [ ] DNS configured on vnet2 and vnet3 pointing to DC
- [ ] DNS resolution working from client to webserver

### IIS Configuration:
- [ ] IIS installed on webserver-vm
- [ ] DNS A record created for webserver-vm
- [ ] Default page title modified to "studentID's Windows Server"
- [ ] Website accessible via FQDN from client-vm

### Permissions:
- [ ] Domain Users added to "Allow log on locally" policy
- [ ] Domain Users added to "Allow log on through Remote Desktop Services"
- [ ] Domain Users added to Remote Desktop Users group
- [ ] Can log in to all VMs with domain user (not just admin)

### Testing:
- [ ] Can log into client-vm with studentID@studentID.MST300.com
- [ ] Can access http://webserver-vm.studentID.MST300.com from client
- [ ] Website shows custom title
- [ ] All VMs communicating through peered networks
