# Meraki Magic MCP - Prompt Library

A collection of practical prompts for each Meraki Magic MCP tool, demonstrating real-world scenarios and use cases.

---

## Core Management Tools

### 1. getOrganizations

#### Basic Prompts:
```
"Show me all my Meraki organizations"

"List all organizations I have access to"

"What Meraki organizations can I manage?"

"Get a list of my Meraki orgs with their IDs"
```

#### Advanced Prompts:
```
"Show me all my Meraki organizations and tell me which ones are using co-term licensing vs per-device licensing"

"List all organizations I manage, group them by region, and show me which ones have API access enabled"

"I'm an MSP managing multiple customers. Show me all my organizations and create a summary report with organization names, customer numbers, and licensing models"

"Get all my organizations and identify which ones are in the North America region"
```

---

### 2. getOrganizationAdmins

#### Basic Prompts:
```
"Show me all administrators in my organization"

"Who has admin access to my Meraki dashboard?"

"List all dashboard admins for organization ID 123456"

"Get the admin list for the Cisco Validated 01 organization"
```

#### Advanced Prompts:
```
"Show me all administrators in my organization and identify which ones have full access vs read-only access"

"I need to audit admin accounts. Show me all administrators, their email addresses, privilege levels, and when they last logged in"

"We're doing a quarterly access review. List all admins in my organization and flag any accounts that haven't been active in the last 90 days"

"Show me all network-specific administrators and tell me which networks each admin can access"

"I need to prepare for a security audit. Generate a report of all administrators showing their names, email addresses, authentication methods (SAML vs local), and permission levels"

"Who are the full administrators in my organization? I need to review their access for compliance"
```

---

### 3. getOrganizationNetworks

#### Basic Prompts:
```
"Show me all networks in my organization"

"List all sites in my Meraki deployment"

"What networks do I have in organization 123456?"

"Get all my branch locations from Meraki"
```

#### Advanced Prompts:
```
"Show me all networks that have wireless products deployed"

"List all branch office networks tagged as 'retail' in my organization"

"I need to plan a firmware upgrade. Show me all networks with switches and group them by timezone"

"Show me all networks that are bound to configuration templates vs standalone networks"

"List all networks in the Eastern timezone so I can schedule maintenance during off-hours"

"Show me networks that have both appliances and wireless, exclude any that are template-bound"

"I'm doing capacity planning. Show me all networks, count how many have cameras, and tell me which ones might need additional licensing"

"Find all networks tagged with 'branch' and 'priority' that have wireless products"

"Show me all my Florida locations by filtering networks with the Florida tag"
```

---

### 4. getOrganizationDevices

#### Basic Prompts:
```
"Show me all devices in my organization"

"List all Meraki hardware across my deployment"

"What devices are deployed in organization 123456?"

"Get an inventory of all my Meraki equipment"
```

#### Advanced Prompts:
```
"Show me all wireless access points in my organization"

"List all devices and tell me which ones are running outdated firmware versions"

"I need to plan a hardware refresh. Show me all switches, group them by model, and tell me how many of each model I have"

"Find all devices tagged with 'critical' and show me their current status"

"Show me all cameras in my organization and which networks they're assigned to"

"I'm looking for a specific device. Find any device with serial number Q2XX in my organization"

"List all devices by product type and create a summary showing counts of each type (switches, APs, cameras, etc.)"

"Show me all devices in networks tagged 'branch' that are switches or access points"

"I need to track warranty expiration. Show me all devices with their models and serial numbers"

"Find all MX security appliances in my organization and show me their network assignments"
```

---

### 5. getNetwork

#### Basic Prompts:
```
"Show me details for network L_123456"

"What are the settings for the CV-54-DEN network?"

"Get information about my New York office network"

"Tell me about network ID L_685673043267171688"
```

#### Advanced Prompts:
```
"Show me the configuration details for the CV-101-NYC Hub Site1 network including product types and tags"

"I'm about to make changes to network L_123456. First, show me its current configuration including timezone and template binding status"

"Get the network details for CV-203-NNJ and tell me if it's bound to a configuration template"

"Show me all the details for the CV-00-OOB network and explain what products are deployed there"

"I need to verify the timezone setting for the CV-54-DEN network before scheduling maintenance"

"Show me the enrollment string for network L_123456 so I can onboard new devices"
```

---

### 6. getNetworkClients

#### Basic Prompts:
```
"Show me all clients connected to network L_123456"

"What devices are currently on the CV-54-DEN network?"

"List all connected clients in the last 24 hours for my network"

"How many devices are connected to my wireless network?"
```

#### Advanced Prompts:
```
"Show me all wireless clients connected to network L_123456 in the last hour"

"I'm troubleshooting connectivity. Show me all clients with IP address 192.168.1.x on network L_123456"

"List all clients connected to VLAN 10 in the CV-101-NYC network"

"Show me all Apple iOS devices connected to my guest wireless network"

"I need to identify unauthorized devices. Show me all clients on network L_123456 with their MAC addresses and descriptions, filtered to show only online devices"

"Find any client with MAC address aa:bb:cc on my network"

"Show me all wired clients vs wireless clients on network L_123456 and give me a count of each"

"List all clients on the guest network in the last week and show me their connection duration"

"I suspect there's a rogue device. Show me all unknown or unnamed clients on network L_123456"

"Show me all clients on VLAN 100 and tell me if any are offline"
```

---

### 7. getNetworkEvents

#### Basic Prompts:
```
"Show me recent events for network L_123456"

"What happened on my network in the last hour?"

"Get the event log for CV-54-DEN network"

"Show me network events from this morning"
```

#### Advanced Prompts:
```
"A user reported WiFi issues at 2:30 PM today. Show me all wireless events around that time for network L_123456"

"Show me all configuration changes made to network L_123456 in the last 7 days"

"I need to troubleshoot a client connection issue. Show me all events related to MAC address aa:bb:cc:dd:ee:ff"

"Show me all security-related events for my network in the last 24 hours"

"List all events where devices went offline on network L_123456"

"Show me authentication failures on the corporate SSID in the last hour"

"I need to audit configuration changes. Show me all events where admins made changes to network settings"

"Show me all DHCP-related events for client IP 192.168.1.50"

"Find all events related to switch serial Q2XX-XXXX-XXXX in the last day"

"Show me all association and authentication events for the guest wireless network"

"I'm investigating a security incident. Show me all events with 'failed' or 'denied' in the description"
```

---

### 8. getNetworkDevices

#### Basic Prompts:
```
"Show me all devices in network L_123456"

"What hardware is deployed at the CV-54-DEN site?"

"List all devices in the New York office network"

"Get device inventory for network L_685673043267171688"
```

#### Advanced Prompts:
```
"Show me all switches in the CV-101-NYC network and their firmware versions"

"List all devices in network L_123456, group them by model, and show me their current status"

"I'm planning a firmware upgrade for the CV-203-NNJ network. Show me all devices and their current firmware versions"

"Show me all wireless access points in the CV-54-DEN network with their model numbers"

"List all devices in network L_123456 and identify which ones are offline"

"Show me the MX security appliance in the CV-101-NYC network and its configuration details"

"Get all devices in the CV-200-NNJ network and show me their LAN IP addresses"

"I need to update device notes. Show me all devices in network L_123456 with their current notes"

"Show me all cameras deployed in the CV-60-SUM network"
```

---

### 9. getDevice

#### Basic Prompts:
```
"Show me details for device serial Q2XX-XXXX-XXXX"

"What is the status of device Q2HP-XXXX-XXXX?"

"Get information about the device with serial number Q2XX-YYYY-ZZZZ"

"Look up device Q2XX-XXXX-XXXX"
```

#### Advanced Prompts:
```
"I'm troubleshooting a switch. Show me all details for device serial Q2XX-XXXX-XXXX including its network assignment, firmware version, and LAN IP"

"A technician needs to replace a device. Get full details for serial Q2XX-XXXX-XXXX including model, MAC address, and location"

"Show me device Q2XX-XXXX-XXXX and tell me if its firmware is up to date"

"I need to verify the location of device Q2XX-XXXX-XXXX before sending a technician"

"Get device Q2XX-XXXX-XXXX and show me all its tags and notes"

"Show me details for device Q2XX-XXXX-XXXX and confirm which network it's assigned to"

"I'm creating a support ticket. Get all information for device serial Q2XX-XXXX-XXXX"
```

---

### 10. getNetworkWirelessSsids

#### Basic Prompts:
```
"Show me all SSIDs configured in network L_123456"

"What wireless networks are available at the CV-54-DEN site?"

"List all WiFi networks in my corporate office"

"Get SSID configuration for network L_685673043267171688"
```

#### Advanced Prompts:
```
"Show me all SSIDs in network L_123456 and tell me which ones use WPA2-PSK vs 802.1X authentication"

"I need to audit wireless security. Show me all SSIDs in the CV-101-NYC network with their encryption and authentication settings"

"List all SSIDs in network L_123456 and show me which VLANs they're assigned to"

"Show me the guest wireless configuration including splash page settings for network L_123456"

"I'm troubleshooting WiFi. Show me all SSIDs in the CV-54-DEN network and tell me which ones are currently enabled"

"Show me all SSIDs using pre-shared keys so I can plan a migration to 802.1X"

"List all SSIDs in network L_123456 and identify which ones have RADIUS authentication configured"

"Show me the SSID configuration for the corporate network and tell me if band steering is enabled"
```

---

### 11. getDeviceSwitchPorts

#### Basic Prompts:
```
"Show me all ports on switch Q2XX-XXXX-XXXX"

"What is the port configuration for switch Q2HP-YYYY-ZZZZ?"

"List all switch ports for device serial Q2XX-XXXX-XXXX"

"Get port status for switch Q2XX-XXXX-XXXX"
```

#### Advanced Prompts:
```
"Show me all ports on switch Q2XX-XXXX-XXXX and identify which ones are currently in use"

"I'm troubleshooting connectivity on port 12. Show me the configuration for all ports on switch Q2XX-XXXX-XXXX"

"List all trunk ports on switch Q2XX-XXXX-XXXX and show me their allowed VLANs"

"Show me which ports have PoE enabled on switch Q2XX-XXXX-XXXX and how much power they're providing"

"I need to find an available port. Show me all disabled ports on switch Q2XX-XXXX-XXXX"

"Show me all ports assigned to VLAN 10 on switch Q2XX-XXXX-XXXX"

"List all ports on switch Q2XX-XXXX-XXXX and show me which ones have access policies applied"

"I'm documenting the network. Show me all ports on switch Q2XX-XXXX-XXXX with their names and VLAN assignments"

"Show me port 24 configuration on switch Q2XX-XXXX-XXXX - I need to verify the VLAN and PoE settings"

"Find all ports with MAC allow lists configured on switch Q2XX-XXXX-XXXX"
```

---

### 12. updateDeviceSwitchPort

#### Basic Prompts:
```
"Enable port 12 on switch Q2XX-XXXX-XXXX"

"Change port 8 to VLAN 20 on switch Q2XX-XXXX-XXXX"

"Set port 5 name to 'Reception Printer' on switch Q2XX-XXXX-XXXX"

"Enable PoE on port 10 of switch Q2XX-XXXX-XXXX"
```

#### Advanced Prompts:
```
"Configure port 8 on switch Q2XX-XXXX-XXXX as an access port on VLAN 10 with PoE enabled and name it 'IP Phone - Desk 8'"

"I'm deploying a new IP phone. Configure port 12 on switch Q2XX-XXXX-XXXX with VLAN 10 for data, voice VLAN 20, and enable PoE"

"Change port 24 on switch Q2XX-XXXX-XXXX to a trunk port and allow VLANs 10, 20, 30, and 40"

"Disable port 15 on switch Q2XX-XXXX-XXXX temporarily for troubleshooting"

"Configure port 5 on switch Q2XX-XXXX-XXXX with a MAC allow list for devices aa:bb:cc:dd:ee:ff and 11:22:33:44:55:66"

"Set up port 18 on switch Q2XX-XXXX-XXXX for a guest device: VLAN 50, port isolation enabled, and name it 'Guest Port'"

"Enable storm control on port 20 of switch Q2XX-XXXX-XXXX to prevent broadcast storms"

"Configure port 3 on switch Q2XX-XXXX-XXXX: access port, VLAN 100, enable PoE, set link negotiation to auto, name it 'Wireless AP - Lobby'"

"I need to secure port 16. Configure it on switch Q2XX-XXXX-XXXX with sticky MAC allow list limited to 5 devices"

"Change all voice ports on switch Q2XX-XXXX-XXXX to use voice VLAN 99"
```

---

## Universal API Access Tools

### 13. call_meraki_api

#### Basic Prompts:
```
"Use call_meraki_api to get firewall rules for network L_123456"

"Call the Meraki API to update SSID settings"

"I need to use an API method that's not directly available - help me use call_meraki_api"
```

#### Advanced Prompts:
```
"Use call_meraki_api to configure L3 firewall rules on network L_123456. Add a rule to allow HTTP and HTTPS from any source to any destination"

"I need to configure VPN settings. Use call_meraki_api with the appliance section to get the current site-to-site VPN configuration for network L_123456"

"Use call_meraki_api to update the content filtering settings on network L_123456 to block social media categories"

"Call the camera API to adjust motion detection sensitivity on device Q2XX-XXXX-XXXX to high"

"Use call_meraki_api to create a new group policy on network L_123456 for guest devices with bandwidth limits of 5 Mbps down and 2 Mbps up"

"I need to configure QoS rules. Use call_meraki_api to set up traffic shaping on network L_123456 prioritizing VoIP traffic"

"Use call_meraki_api to get the MTU settings for all switches in network L_123456"

"Call the appliance API to update the one-to-one NAT rules for network L_123456"

"Use call_meraki_api to retrieve camera snapshot from device Q2XX-XXXX-XXXX taken 5 minutes ago"

"I need to configure OSPF routing. Use call_meraki_api to get and then update OSPF settings for network L_123456"
```

---

### 14. list_all_methods

#### Basic Prompts:
```
"Show me all available Meraki API methods"

"List all API methods I can use"

"What Meraki API operations are available?"

"Show me the full list of supported methods"
```

#### Advanced Prompts:
```
"Show me all available methods in the wireless section"

"List all switch-related API methods so I can plan my automation"

"I'm working on camera integration. Show me all available methods in the camera section"

"Show me all methods available for the appliance section - I need to configure firewall and VPN"

"List all organization-level methods that deal with licensing"

"Show me all available sensor-related methods for environmental monitoring"

"I need to work with Systems Manager. Show me all available methods in the sm section"

"List all network-level methods related to clients"

"Show me all device-related methods for live tools and troubleshooting"
```

---

### 15. search_methods

#### Basic Prompts:
```
"Search for API methods related to 'firewall'"

"Find methods that deal with 'alert'"

"Search for 'SSID' related methods"

"Look for methods about 'admin'"
```

#### Advanced Prompts:
```
"Search for all API methods related to 'firewall' - I need to configure both L3 and L7 rules"

"Find all methods that contain 'alert' or 'notification' - I'm setting up monitoring"

"Search for methods related to 'VPN' configuration and status"

"Find all API methods for 'QoS' and traffic shaping"

"Search for 'camera' methods that deal with 'snapshot' or 'recording'"

"Find all methods related to 'firmware' - I need to check versions and plan upgrades"

"Search for methods containing 'client' to find all client-related operations"

"Find methods related to 'port' configuration for switches"

"Search for 'license' methods to help with license management and reporting"

"Find all methods that deal with 'event' or 'log' for audit purposes"
```

---

### 16. get_method_info

#### Basic Prompts:
```
"Show me details about the updateNetworkWirelessSsid method"

"What parameters does getOrganizationDevices accept?"

"Explain the updateDeviceSwitchPort method"

"Get information about the getNetworkEvents method"
```

#### Advanced Prompts:
```
"I need to update firewall rules. Show me detailed parameter information for updateNetworkApplianceFirewallL3FirewallRules"

"What are all the available parameters for updateNetworkWirelessSsid? I want to configure advanced wireless settings"

"Show me the parameter details for createNetworkGroupPolicy - I need to understand bandwidth limits and VLAN tagging options"

"Explain all parameters for getNetworkEvents including how to filter by event type and time range"

"I'm configuring VLANs. Show me parameter details for createNetworkApplianceVlan"

"What parameters can I use with getOrganizationDevices to filter by product type and tags?"

"Show me detailed information about updateDeviceSwitchPort including all available port settings like PoE, VLANs, and access policies"

"Get parameter details for updateNetworkApplianceContentFiltering - I need to configure web filtering"

"Explain the parameters for getNetworkClients including timespan and filtering options"
```

---

## Cache Management Tools

### 17. cache_stats

#### Basic Prompts:
```
"Show me cache statistics"

"How is the cache performing?"

"Get cache status and metrics"

"Display MCP cache information"
```

#### Advanced Prompts:
```
"Show me cache statistics and tell me the cache hit rate - is it performing well?"

"Display cache stats and identify which API endpoints are being cached most frequently"

"I'm troubleshooting slow performance. Show me cache statistics including hit/miss ratios and TTL settings"

"Get cache stats and tell me how much storage the cache is using"

"Show me cache performance metrics and recommend if I need to adjust cache settings"
```

---

### 18. cache_clear

#### Basic Prompts:
```
"Clear the cache"

"Reset all cached data"

"I need fresh data - clear the cache"

"Flush the API response cache"
```

#### Advanced Prompts:
```
"I just made configuration changes to multiple networks. Clear the cache so I can verify the changes"

"Clear the cache and then re-fetch organization devices to ensure I have current data"

"I suspect cached data is causing issues. Clear the cache and then show me updated network information"

"Clear all cached responses and then re-run my device inventory report"

"I've completed bulk firmware upgrades. Clear the cache so next queries show updated firmware versions"
```

---

### 19. get_cached_response

#### Basic Prompts:
```
"Show me the first 100 devices from the cached response"

"Get paginated data from cached file"

"Retrieve cached response starting at offset 500"
```

#### Advanced Prompts:
```
"I have a cached response with 5000 devices. Show me devices 1000-1100"

"Get the next 50 records from the cached event log starting at offset 200"

"The organization device query was cached. Show me the first 100 devices, then I'll process them in batches"

"Retrieve paginated data from the cached response - show me records 500-600 for processing"

"Show me the cached network list in chunks of 25 networks at a time starting from the beginning"
```

---

### 20. list_cached_responses

#### Basic Prompts:
```
"Show me all cached API responses"

"What data is currently cached?"

"List all cached files"

"Display cached response inventory"
```

#### Advanced Prompts:
```
"Show me all cached responses and tell me which ones are older than 6 hours"

"List all cached files and identify the largest ones"

"Display all cached API responses with their timestamps so I can decide what to clean up"

"Show me cached responses and tell me which endpoints are cached most frequently"
```

---

### 21. clear_cached_files

#### Basic Prompts:
```
"Clear cached files older than 24 hours"

"Remove old cached data"

"Clean up cache files from yesterday"

"Delete cached responses older than 12 hours"
```

#### Advanced Prompts:
```
"Clear all cached files older than 24 hours to free up storage space"

"Remove cached data older than 6 hours - I need to ensure fresh data for my reports"

"Clean up cached files older than 48 hours as part of weekly maintenance"

"Delete all cached responses older than 1 hour so I'm always working with recent data"

"Clear cached files older than 12 hours and then show me remaining cache statistics"
```

---

### 22. get_mcp_config

#### Basic Prompts:
```
"Show me MCP configuration"

"What are the current MCP settings?"

"Display MCP configuration details"

"Get MCP setup information"
```

#### Advanced Prompts:
```
"Show me the MCP configuration including cache TTL and rate limiting settings"

"I'm troubleshooting API issues. Display the MCP configuration to verify my API key and settings"

"Get MCP configuration and confirm that caching is enabled with appropriate TTL values"

"Show me MCP config and tell me what organization ID is currently configured"

"Display MCP configuration details so I can document our integration setup"
```

---

## Complex Multi-Tool Workflows

### Workflow Prompts:

#### Network Health Assessment
```
"I need a complete health check of my organization. Show me:
1. All networks and their device counts
2. Any devices that are offline
3. Recent critical events in the last 24 hours
4. Networks with unusually high or low client counts"
```

#### Security Audit
```
"Perform a security audit on my network:
1. List all administrators and their privilege levels
2. Show all wireless SSIDs and flag any using weak security (WPA2-PSK)
3. List any clients on the guest network that have been connected for more than 24 hours
4. Show all security-related events from the last week"
```

#### Device Provisioning
```
"I'm deploying a new switch at our branch office:
1. First, show me the devices in network L_123456
2. The new switch serial is Q2XX-YYYY-ZZZZ - can you confirm it's in the network?
3. Show me port 1-24 configuration
4. Configure ports 1-8 as access ports on VLAN 10 with PoE for IP phones
5. Configure port 24 as a trunk port allowing VLANs 10, 20, 30"
```

#### Troubleshooting Workflow
```
"A user at 192.168.1.50 can't connect to WiFi:
1. Find this client in network L_123456
2. Show me all events related to this client's MAC address in the last hour
3. Check which SSID they're trying to connect to
4. Show me the SSID configuration
5. Look for any authentication or DHCP failures"
```

#### Bulk Configuration
```
"I need to update wireless settings across all branch locations:
1. Show me all networks tagged with 'branch'
2. For each network, get the SSID configuration for 'Corporate-WiFi'
3. I need to update the WPA2 key to a new value across all branches
4. After updating, verify the changes by showing me the updated SSID configs"
```

#### Firmware Upgrade Planning
```
"Help me plan a firmware upgrade:
1. Show me all devices in my organization
2. Group them by model and current firmware version
3. Identify which models have firmware updates available
4. Create an upgrade plan prioritizing critical infrastructure
5. Group devices by network timezone so I can schedule upgrades during maintenance windows"
```

#### Capacity Planning
```
"I need to assess network capacity:
1. Show me all networks and their deployed product types
2. For wireless networks, show me peak client counts
3. Identify networks with more than 50 concurrent clients
4. Show me switch port utilization across all switches
5. Recommend which sites might need additional access points or switches"
```

#### Compliance Reporting
```
"Generate a compliance report:
1. List all administrators with full organization access
2. Show all networks that are NOT bound to configuration templates
3. List any SSIDs using WPA2-PSK instead of 802.1X
4. Show all configuration changes made in the last 30 days
5. Identify any devices with firmware versions older than 6 months"
```

#### Client Investigation
```
"I need to investigate suspicious network activity:
1. Show me all clients connected to network L_123456 in the last 4 hours
2. Filter for clients with hostnames containing 'unknown' or no description
3. Show me what VLANs these clients are on
4. Get event logs for these clients showing connection and authentication events
5. Identify any clients that have changed IP addresses multiple times"
```

#### Port Inventory and Documentation
```
"Help me document switch configurations:
1. Show me all switches in network L_123456
2. For each switch, get the port configuration
3. Create a report showing:
   - Port numbers and names
   - VLAN assignments
   - PoE status
   - Which ports are in use vs available
4. Identify any ports with non-standard configurations"
```

---

## Tips for Writing Effective Prompts

### Be Specific:
❌ "Show me networks"
✅ "Show me all networks in organization 123456 that have wireless products and are tagged with 'branch'"

### Include Context:
❌ "Check the device"
✅ "I'm troubleshooting connectivity. Show me device Q2XX-XXXX-XXXX including its status, firmware version, and network assignment"

### Chain Operations:
❌ "Configure port 5"
✅ "I'm deploying an IP phone on port 5 of switch Q2XX-XXXX-XXXX. Configure it as access port on VLAN 10, voice VLAN 20, enable PoE, and name it 'Reception Phone'"

### Specify Timeframes:
❌ "Show events"
✅ "Show me all authentication failure events for network L_123456 in the last 2 hours"

### Request Summaries:
❌ "Get devices"
✅ "Show me all devices in my organization, group them by product type, and give me a count of each type"

### Include Expected Actions:
❌ "Show me SSIDs"
✅ "Show me all SSIDs in network L_123456 and tell me which ones use WPA2-PSK so I can plan a migration to 802.1X"

---

## Prompt Templates by Use Case

### Troubleshooting Template:
```
"I'm troubleshooting [ISSUE]. 
1. Show me [RELEVANT DATA]
2. Check [SPECIFIC COMPONENT]
3. Look for [ERROR INDICATORS]
4. Help me identify the root cause"
```

### Configuration Template:
```
"I need to configure [COMPONENT] on [DEVICE/NETWORK].
1. First, show me the current configuration
2. Apply these changes: [SPECIFIC CHANGES]
3. Verify the changes were applied successfully"
```

### Audit Template:
```
"Perform a [TYPE] audit:
1. List all [COMPONENTS TO AUDIT]
2. Check for [COMPLIANCE CRITERIA]
3. Identify any [ISSUES OR EXCEPTIONS]
4. Generate a summary report"
```

### Reporting Template:
```
"Generate a report showing:
1. [METRIC 1] grouped by [DIMENSION]
2. [METRIC 2] with [FILTERS]
3. Highlight [NOTEWORTHY ITEMS]
4. Provide recommendations for [IMPROVEMENTS]"
```

---

## Common Question Patterns

### "Show me..." - Retrieval
- "Show me all devices..."
- "Show me network configuration..."
- "Show me who has access..."

### "Find..." - Search
- "Find the device with serial..."
- "Find all clients on VLAN..."
- "Find networks tagged with..."

### "Configure..." - Modification
- "Configure port 5 to..."
- "Configure SSID settings..."
- "Configure firewall rules..."

### "Check..." - Verification
- "Check if device is online..."
- "Check VLAN assignment..."
- "Check recent events..."

### "List all..." - Enumeration
- "List all administrators..."
- "List all SSIDs..."
- "List all offline devices..."

### "Help me..." - Assisted Workflow
- "Help me troubleshoot..."
- "Help me plan firmware upgrade..."
- "Help me audit security settings..."

### "I need to..." - Task-Oriented
- "I need to deploy a new switch..."
- "I need to investigate suspicious activity..."
- "I need to prepare for audit..."
