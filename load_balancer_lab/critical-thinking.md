## finance
![finance-new](finance-new.PNG)
## H.R
![HR-new](HR-new.PNG)
## Sales
![sales-new](sales-new.PNG)
## Marketing
![markeing-new](marketing-new.PNG)
## I.T
![I.T-new](I.T-new.PNG)
## Operation
![operation-new](operation-new.PNG)

# 2 DOCUMENTATION

# Finance
## Subnet Mask: 255.255.255.192 
## IP Range: 192.168.0.1 – 192.168.0.126

# Human Resources
## Subnet Mask: 255.255.255.224
## IP Range: 192.168.1.193 – 192.168.1.222

# Sales
## Subnet Mask: 255.255.255.192
## IP Range: 192.168.1.1 – 192.168.1.62

# Marketing
## Subnet Mask: 255.255.255.192
## IP Range: 192.168.1.129 – 192.168.1.190

# IT 
## Subnet Mask: 255.255.255.128
## IP Range: 192.168.0.1 – 192.168.0.126

# Operations
## Subnet Mask: 255.255.255.128
## IP Range: 192.168.0.129 – 192.168.0.25

# Troubleshooting Scenarios:
## Check routing tables for correct subnet routes;
To troubleshoot incorrect subnet routes in a routing table, begin by examining the table itself using tools like show ip route (Cisco) or netstat -rn (Windows/Linux) to view the routing table entries. Ensure routes for each subnet are present and point to the correct next-hop IP address. If missing, add or adjust the routes accordingly. Additionally, check for potential conflicts between static and dynamically learned routes, and verify that routing protocols (like OSPF) are configured correctly. 

## Verify firewall rules for inter-subnet communication;
To troubleshoot and verify firewall rules for inter-subnet communication, start by reviewing inbound and outbound rules, ensuring they align with security policies and don't conflict. Analyze firewall logs for denied connections and rule priorities. Verify necessary ports are open and assess NAT configurations if applicable. Use tools like packet captures and con
nectivity tests to pinpoint issues and validate rule effectiveness. 

# IP Conflicts:
## Use DHCP server logs to identify conflicting IP addresses;
To troubleshoot and identify conflicting IP addresses using DHCP server logs, first enable comprehensive logging on your DHCP server. Then, examine the logs for entries indicating IP address conflicts, often marked as "BAD_ADDRESS" or similar. These entries will usually include the conflicting IP address and associated MAC address, allowing you to pinpoint the devices involved. Further investigation might involve checking the event log for specific device details or using tools to locate the device on the network.

## Manually assign IP addresses to resolve conflicts.
To resolve IP address conflicts when manually assigning addresses, identify the conflicting devices, change the IP address of one or both devices, and verify the new addresses are unique and within your network's range. Ensure the router's DHCP server isn't also assigning addresses within the same range as your manual assignments, and consider releasing and renewing IP addresses on affected devices if needed.

# Overlapping
## Ensure each subnet has a unique IP address range
To ensure each subnet has a unique IP address range, you need to understand how subnets are created and allocated within a network. Each subnet must have a unique network ID, which is determined by the IP address and subnet mask. If subnets overlap, it will cause IP address conflicts, preventing devices from communicating correctly. 

# Adjust subnet masks to avoid overlapping ranges.
To troubleshoot and adjust subnet masks to avoid overlapping ranges, you need to analyze your existing network configurations and identify overlapping IP ranges. Then, you can adjust the subnet masks to create non-overlapping subnets, either by using larger subnet masks (reducing the number of usable IP addresses) or by re-numbering your network. 

# Future Growth:
## Expand Subnets
## Increase subnet sizes by adjusting subnet masks;
To increase subnet sizes, adjust the subnet mask by borrowing bits from the host portion of the IP address and assigning them to the network portion. This allows for more subnets with fewer hosts per subnet, or fewer subnets with more hosts per subnet. For example, a /24 subnet mask (255.255.255.0) can be adjusted to a /20 subnet mask (255.255.240.0) to accommodate more hosts within the same network, or to a /26 subnet mask (255.255.255.192) for a more granular network split.
## Add new subnets for additional departments or teams.
To add new subnets for additional departments or teams, you'll need to determine a new IP address range and then configure your network devices (routers, switches, firewalls) to recognize and route traffic to those new subnets. This can involve using tools like Azure Portal or Active Directory Sites and Services for cloud environments or using command-line interfaces or network management software for on-premise networks.

# Modify Documentation
## Update IP address ranges and subnet masks accordingly.
 To update IP address ranges and subnet masks, you'll need to adjust the subnetting configuration of your network. This involves changing the subnet mask to allocate more or fewer host addresses per subnet, or creating new subnets to segment your network. 
 ## Keep track of changes for future reference.
 To effectively keep track of changes for future reference, you can utilize tools like Microsoft Word's "Track Changes" feature, create changelogs, or use project management software with version control. These methods help record modifications, revisions, and their impact, enabling easy retrieval and analysis. 

 # Optimization
 ## Efficient Routing; 
 ## Implement routing protocols to optimize traffic between subnets.
 To optimize traffic between subnets, implement dynamic routing protocols like OSPF or BGP on your network devices. These protocols dynamically update routing tables, ensuring the most efficient paths for data packets between subnets. 
 ## Use VLANs to segment traffic within departments
 VLANs (Virtual Local Area Networks) are used to segment network traffic within departments by logically grouping devices, even if they are on the same physical network. This allows for better security, performance, and manageability by isolating traffic between departments. 

 # IP Address Use
 ## Implement DHCP for dynamic IP address assignment
 To implement DHCP for dynamic IP address assignment, a DHCP server needs to be configured to manage an IP address pool and assign IP addresses to network devices. This involves enabling DHCP, defining address pools, configuring network and subnet settings, and optionally setting lease durations. 
 ## Reserve static IP addresses for critical devices and servers.
 To reserve static IP addresses for critical devices and servers, you can configure DHCP reservations on your network's DHCP server. This ensures that these devices consistently receive the same IP address, even if the DHCP server is restarted or if other devices on the network are requesting IP addresses. 