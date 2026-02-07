# Connectivity Troubleshooting

## ❌ Issue
Unable to reach a VM in a different subnet using ping.

## 🔍 Investigation
- Verified both VMs were running
- Confirmed private IP addresses were used
- Reviewed Network Security Group (NSG) inbound rules
- Confirmed ICMP was allowed at the Azure network level

## 🧠 Root Cause
ICMP traffic was blocked by the Windows Firewall on the destination virtual machine, even though the Network Security Group allowed ICMP within the virtual network.

## ✅ Resolution
- Verified NSG rules permitted ICMP traffic from the VirtualNetwork service tag
- Enabled ICMP Echo Request in Windows Firewall on the destination VM
- Retested connectivity and confirmed successful ping response

## 📘 Lesson Learned
Cloud-level networking controls (NSGs and routing) and OS-level firewalls must both be validated when troubleshooting connectivity issues in Azure.
