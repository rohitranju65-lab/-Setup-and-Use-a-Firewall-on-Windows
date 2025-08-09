# -Setup-and-Use-a-Firewall-on-Windows
 Configure and test basic firewall rules to allow or block traffic.
# Windows Firewall Configuration and Testing Guide

## 1. Open Firewall Configuration Tool
### **GUI Method**
1. Press `Win + R`, type `control`, and press **Enter**.
2. Navigate to **System and Security → Windows Firewall**.
3. Select **Advanced settings** to manage inbound and outbound rules.
  <img width="795" height="597" alt="1" src="https://github.com/user-attachments/assets/fb8c6fdc-d465-443a-acd5-5a9cd06b492a" />
 
Command Line Method** (Run as Administrator)
cmd
'''netsh advfirewall firewall show rule name=all

##2. List Current Firewall Rules
cmd
netsh advfirewall firewall show rule name=all
<img width="797" height="597" alt="2" src="https://github.com/user-attachments/assets/8514c57c-c14a-4207-9e1f-9e7f0a029cfe" />

##3. Add a Rule to Block Inbound Traffic on Port 23 (Telnet)
cmd

netsh advfirewall firewall add rule name="Block Telnet Port 23" dir=in action=block protocol=TCP localport=23
<img width="798" height="596" alt="3" src="https://github.com/user-attachments/assets/758721a9-3a73-4148-9dd5-83badd0b1505" />

##4. Test the Rule
cmd
   telnet localhost 23
 <img width="800" height="602" alt="4" src="https://github.com/user-attachments/assets/1966d97d-ee7b-4292-8f6c-3adb78deb6db" />
  
##5. Add a Rule to Allow SSH (Port 22) on Windows
cmd
netsh advfirewall firewall delete rule name="Block Telnet Port 23"
<img width="797" height="600" alt="5" src="https://github.com/user-attachments/assets/654327ed-fa79-4ded-b5c2-1f225d5c205c" />
<img width="800" height="601" alt="6" src="https://github.com/user-attachments/assets/f694d354-e8e7-4ce2-bf18-48910e657a95" />

##6. Remove the Test Block Rule
cmd
 netsh advfirewall firewall delete rule name="Block Telnet Port 23"
 <img width="791" height="598" alt="7 delete" src="https://github.com/user-attachments/assets/17095fbc-6768-4ae4-ae23-a443267a5890" />
<img width="797" height="602" alt="8show" src="https://github.com/user-attachments/assets/4fdcb6c0-c33d-4f14-96c9-f7170e03ac0b" />

