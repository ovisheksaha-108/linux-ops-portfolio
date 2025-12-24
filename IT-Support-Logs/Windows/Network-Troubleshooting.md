# Incident Report: Windows Network Stack Recovery

## 📝 Overview
This report documents a real-world troubleshooting scenario where a host machine lost internet connectivity. The fix was performed using the Command Line Interface (CLI) to ensure a precise and efficient resolution.

## 🔍 Problem Discovery
- **Symptoms:** Wi-Fi connected to the router but showed "No Internet." 
- **Root Cause:** A manual static IP mismatch prevented the system from communicating with the local gateway.

## 🛠️ Resolution Steps (CLI-Based)
I chose to use the CLI over the GUI to ensure all network protocols were properly reset.

1. **Reverted to DHCP:** Used `netsh` to allow the router to assign a valid IP automatically.
2. **Reset Network Stack:** Ran `netsh winsock reset` and `netsh int ip reset` to clear corrupted configurations.
3. **Flushed DNS:** Used `ipconfig /flushdns` to clear stale name resolution data.
4. **Verified Connection:** Confirmed `DHCP Enabled: Yes` using `ipconfig /all`.

## 🔄 Professional Transferable Skills
This troubleshooting logic is a core part of my IT Operations toolkit and applies to many support environments:

| Task | Skill Demonstrated |
| :--- | :--- |
| **CLI Navigation** | Comfort with terminal-based system administration. |
| **Network Diagnostics** | Understanding of TCP/IP, DHCP, and DNS protocols. |
| **Documentation** | Ability to create clear Standard Operating Procedures (SOPs). |
| **Problem Solving** | Systematic approach to identifying and resolving hardware/software conflicts. |

## ✅ Final Outcome
Connectivity was fully restored. This documented process serves as proof of my technical accuracy and my ability to communicate complex fixes in a simple, effective way.
