## AD-Splunk-Detection-Lab

### Objective
The AD-Splunk Lab was designed to simulate a small corporate network environment using virtual machines and open-source tools. The purpose of this lab was to learn how to configure Active Directory, collect logs from Windows endpoints, and detect brute-force attacks using Splunk.

### Skills Learned

- Configured Active Directory Domain Services (AD DS) on Windows Server 2022.
- Installed and managed Splunk Enterprise for log analysis.
- Used Sysmon for detailed Windows event logging.
- Simulated brute-force attacks with Kali Linux and analyzed detection events.
- Connected domain-joined machines and practiced user/OU management.
- Developed end-to-end visibility into authentication activity and attack monitoring.

### Tools Used

- **Windows Server 2022** – Domain Controller running AD DS and DNS.
- **Windows 10** – Domain-joined endpoint, configured with Sysmon and Splunk UF.
- **Ubuntu Server (22.04)** – Hosted Splunk Enterprise for centralized log analysis.
- **Kali Linux** – Simulated brute-force RDP attacks using Crowbar.
- **Sysmon** – Logged process creation, network events, and more.
- **Splunk (Enterprise & UF)** – Collected, indexed, and visualized log data.
- **Crowbar** – Brute-forced RDP login attempts on domain user accounts.
- **VirtualBox** – Virtualization platform for the full lab.

### Steps

**Step 1** – Set up VirtualBox and installed 4 VMs (Windows Server, Windows 10, Ubuntu, Kali).  
**Step 2** – Assigned static IPs to all VMs and confirmed interconnectivity.  
**Step 3** – Promoted Windows Server to Domain Controller (mydfir.local) and created users/OUs.  
**Step 4** – Installed Sysmon and Splunk Universal Forwarder on the Windows 10 machine.  
**Step 5** – Installed Splunk Enterprise on Ubuntu and configured it to receive logs on port 9997.  
**Step 6** – Simulated brute-force RDP attacks using Crowbar from Kali targeting 'tsmith'.  
**Step 7** – Monitored logs in Splunk and detected authentication events (4625 failed, 4624 success).  
