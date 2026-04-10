# ⚙️ SOC Lab Setup Guide – Wazuh SIEM (OVA Deployment)

This guide explains how I set up my SOC lab using the **Wazuh prebuilt OVA virtual machine** for monitoring and analyzing security events.

---

## 🖥️ 1. Lab Environment

- SIEM: Wazuh (Prebuilt OVA)
- Virtualization: VirtualBox
- Attacker Machine: Kali Linux
- Target Systems: Windows / Linux

<img src="screenshots/wazuh-ova-file.png" width="800"/>

---

## 📦 2. Import Wazuh OVA

1. Download Wazuh OVA from official website  
2. Open VirtualBox  
3. Click **File → Import Appliance**  
4. Select the `.ova` file  
5. Start the VM

After you completely install the VM then use this below commands to start the wazuh server

```Linux cmd
sudo su

systemctl start wazuh-manager

systemctl start wazuh-indexer

systemctl start wazuh-dashboard
```
After this check the status of the services by using this commands 
```Linux cmd
systemctl status wazuh-manager

systemctl status wazuh-dashboard
```

<img src="screenshots/wazuh-VM.png" width="800"/>

<img src="screenshots/wazuh-dashboard-status.png" width="800"/>

---

## 🌐 3. Access Wazuh Dashboard

- Get IP of Wazuh server:
```bash
ip a

   Open browser: https://<WAZUH-IP>

• Login using default credentials it will be always admin:admin

```
## 🔌 Adding a New Wazuh Agent

To add a new agent:

1. Go to the Wazuh Dashboard and click on **"Add new agent"**.  
2. Select the required operating system (Windows, Linux, or macOS).  
3. Enter a name for the agent.  
4. Copy the generated installation command.

---

### 🪟 For Windows Agent

1. Open **PowerShell as Administrator**.  
2. Paste the copied command and execute it.  
3. Start the Wazuh agent service:

```powershell
NET START wazuh
```

<img src="screenshots/wazuh-new-agent.png" width="800"/>


<img src="screenshots/wazuh-agent-selection.png" width="800"/>


<img src="screenshots/wazuh-windows-agent.png" width="800"/>



