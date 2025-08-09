# -Setup-and-Use-a-Firewall-on-Windows
 Configure and test basic firewall rules to allow or block traffic.
# Windows Firewall Configuration and Testing Guide

## 1. Open Firewall Configuration Tool
### **GUI Method**
1. Press `Win + R`, type `control`, and press **Enter**.
2. Navigate to **System and Security → Windows Firewall**.
3. Select **Advanced settings** to manage inbound and outbound rules.

### **Command Line Method** (Run as Administrator)
```cmd
netsh advfirewall firewall show rule name=all
2. List Current Firewall Rules
cmd
Copy
Edit
netsh advfirewall firewall show rule name=all
