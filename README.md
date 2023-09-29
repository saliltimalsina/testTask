**Network Design:**


**Assumptions and Requirements:**

The network design for the small manufacturing company is driven by the following key assumptions and requirements:

**Company Assumptions:**

1. **Single Location:** The company is based in a single location with two attached buildings: the factory and the office building. All network infrastructure and operations are centralized within this location.

2. **Network-Controlled Equipment:** Most of the factory's machinery and equipment are network-controlled and monitored. This includes machinery with wired LAN interfaces and those with wireless WiFi interfaces.

3. **Cloud Services Utilization:** While the company uses cloud services for some servers like the website and email, critical and sensitive data such as engineering designs and financial information are stored on local servers within the office building.

4. **Employee Diversity:** The company employs a diverse range of staff engaged in various functions, including sales, customer support, engineering design, and business administration. The network must cater to the needs of all these departments.

5. **IP-Based Security Cameras:** IP-based security cameras are deployed both inside and outside the buildings for security monitoring. These cameras stream video back to a local server within the office building for storage and monitoring purposes.

**Company Requirements:**

1. **Network Segmentation:** The company requires a well-defined network segmentation to isolate and manage traffic between the factory, office, and security cameras segments. This segmentation is crucial for enhancing security and efficient network management.

2. **IP Subnets:** The network must provide at least three different IP subnets, one for the factory, one for the office, and one for security cameras. These subnets must align with the network segmentation.

3. **IPv4 Addressing:** The company mandates the use of IPv4 addresses with /16 or /24 network masks throughout the network.

4. **Internet Connectivity:** The network design should include an Internet Gateway Router to provide internet connectivity to all segments of the company. This is essential for accessing cloud services and ensuring seamless communication with external networks.

5. **Security and Privacy:** The network must prioritize security and privacy, especially for critical data stored on local servers. Robust security controls and monitoring mechanisms are required to safeguard sensitive information.

6. **Scalability and Redundancy:** The network should be designed with scalability in mind to accommodate future growth. Redundancy should also be considered to ensure high availability and fault tolerance.


**Network Topology:**

The network topology is divided into three primary segments:

1. **Factory Segment:** This segment includes the machinery and control systems used in the manufacturing process. The Factory Router connects to various machines, some of which have wired LAN interfaces, while others use wireless WiFi connections. IP addresses in this segment start with "53."

2. **Office Segment:** The Office Router connects various departments, including Sales, Customer Support, Engineering, and Business Administration. Users in this segment use a mix of wired desktop computers and wireless devices. IP addresses in this segment start with "25."

3. **Security Cameras Segment:** Security cameras are deployed for monitoring both the exterior and interior of the facilities. The Security Camera Server stores and manages the video feed from these cameras. IP addresses in this segment also start with "25."

**Explanation of Key Design Decisions:**
- **Segmentation:** We have segmented the network to isolate different functional areas of the company, enhancing security and network management.
- **Student IDs as IP Prefix:** The use of student IDs in IP addresses provides a consistent and easily identifiable naming convention.
- **VLANs:** Virtual LANs (VLANs) are used to logically isolate and manage traffic within each segment.
- **Internet Gateway Router:** The Internet Gateway Router connects the company's network to the internet, enabling internet access for all segments while providing firewall security.
- **Redundancy:** Redundant switches and routers are used to ensure high availability and fault tolerance.
- **Security Monitoring:** Intrusion detection and prevention systems (IDS/IPS) are implemented to monitor network traffic for any suspicious activity.

**Address Allocations:**

1. **Factory Subnet (53.0.0.0/16):**
   - DHCP Range: 53.0.0.1 to 53.0.0.254
   - Static IPs for critical machinery and devices.

2. **Office Subnet (25.0.0.0/24):**
   - DHCP Range: 25.0.0.1 to 25.0.0.254
   - Static IPs for servers and network devices.

3. **Security Cameras Subnet (25.1.0.0/24):**
   - DHCP Range: 25.1.0.1 to 25.1.0.254
   - Static IPs for the security camera servers.


**Explanation of Recommended Hardware:**

- **Internet Gateway Router:** The Cisco ASR 1000 Series router is recommended as the Internet Gateway Router. It is a high-performance router suitable for small to medium-sized enterprises. It provides advanced security features, including firewall capabilities, to protect the network from external threats while allowing for efficient internet connectivity.

- **Core Switches:** The Cisco Catalyst 9000 Series switches are ideal for the core of the network. These switches offer high reliability, scalability, and advanced network services. They can handle the traffic between various segments efficiently.

- **Access Switches:** The Cisco Catalyst 3000 Series switches serve as access switches in the network. They provide reliable connectivity to end-user devices in both the Factory and Office segments. These switches are known for their performance and support for various VLANs.

- **Routers:** Cisco ISR 4000 Series routers are used within the network to provide routing capabilities. These routers offer high throughput and flexibility, making them suitable for connecting different segments and routing traffic effectively.

- **Firewall:** The Palo Alto Networks PA-Series firewall is recommended for network security. It provides next-generation firewall capabilities, intrusion prevention, and application visibility and control. This firewall enhances the security of the network perimeter.

- **VPN Gateway:** The Cisco ASA Firewall with AnyConnect is used as a VPN gateway to enable secure remote access to the network. It supports VPN connectivity for remote workers and ensures secure data transmission.

- **IDS/IPS:** The Snort IDS/IPS system is deployed for intrusion detection and prevention. It helps monitor network traffic for suspicious activity and provides alerts to administrators in real-time.

This selection of hardware components is designed to meet the company's network requirements, ensuring reliable connectivity, security, and scalability while accommodating the unique needs of the Factory, Office, and Security Cameras segments.
