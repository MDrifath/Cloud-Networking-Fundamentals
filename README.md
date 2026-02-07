# Cloud Networking Fundamentals (Azure)

## 📌 Project Overview
This project demonstrates core cloud networking concepts by creating a Virtual Network (VNet) with multiple subnets and deploying virtual machines in each subnet. Internal connectivity and default routing behavior are tested and analyzed.

## 🧰 Tools & Technologies
- Microsoft Azure
- Virtual Network (VNet)
- Subnets
- Linux Virtual Machines
- ICMP (ping)

## 🧱 Architecture
Two virtual machines deployed in separate subnets within the same VNet communicate using private IP addresses via Azure default routing.

## 🚀 Project Implementation

### 1️⃣ Create VNet with Multiple Subnets
- Created a virtual network with address space `10.0.0.0/16`
- Configured two subnets:
  - Subnet-A: `10.0.1.0/24`
  - Subnet-B: `10.0.2.0/24`

### 2️⃣ Deploy VMs in Different Subnets
- Deployed one Linux VM in Subnet-A
- Deployed one Linux VM in Subnet-B
- Verified private IP address assignment

### 3️⃣ Test Internal Connectivity
- Connected to VM in Subnet-A using RDP
- Successfully pinged VM in Subnet-B using private IP
- Confirmed internal VNet communication

### 4️⃣ Default Routing Behavior
- Verified Azure system routes via Effective Routes
- Observed `VNetLocal` route for internal traffic

## 🔍 Key Learnings
- IP addressing and subnetting
- Private network communication in cloud
- Azure default routing
- Networking troubleshooting basics

## 📷 Screenshots
Relevant screenshots are available in the `screenshots/` directory.

## 📌 Conclusion
This project strengthens foundational networking knowledge required for cloud and network support roles.
# Cloud-Networking-Fundamentals
Azure cloud networking fundamentals using VNets, subnets, private IPs, and ICMP-based connectivity testing
