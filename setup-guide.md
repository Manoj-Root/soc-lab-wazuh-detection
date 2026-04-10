# ⚙️ SOC Lab Setup Guide – Wazuh SIEM (OVA Deployment)

This guide explains how I set up a SOC lab using the **Wazuh prebuilt OVA virtual machine** for monitoring and analyzing security events.

---

## 🖥️ 1. Lab Environment

- SIEM: Wazuh (Prebuilt OVA)
- Virtualization: VirtualBox
- Attacker Machine: Kali Linux
- Target Systems: Windows / Linux

---

## 📦 2. Import Wazuh OVA

1. Download Wazuh OVA from official website  
2. Open VirtualBox  
3. Click **File → Import Appliance**  
4. Select the `.ova` file  
5. Start the VM  

---

## 🌐 3. Access Wazuh Dashboard

- Get IP of Wazuh server:
```bash
ip a

   Open browser: https://<WAZUH-IP>

• Login using default credentials it will be always admin:admin

```
## 🔌 4. Add Agents

### Windows Agent:

#### • Install Wazuh agent on Windows machine
#### • Configure server IP
#### • Start agent service
