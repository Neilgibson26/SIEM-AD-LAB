# 🖥️ SIEM & Active Directory Lab

This project documents the setup and configuration of a virtual cybersecurity lab hosted on **Vultr**, featuring:

- A **Windows Server Domain Controller** with Active Directory (`mydfir.local`)
- A **Windows 10 client** joined to the domain
- A **Splunk server** running on Ubuntu for centralized log collection and analysis

## 🔧 Lab Setup

### 🧱 Virtual Machines (Hosted on Vultr)

| Role                     | OS                | IP Address         |
|--------------------------|-------------------|---------------------|
| Splunk Server            | Ubuntu 22.04      | `45.32.219.225`     |
| Domain Controller (AD)   | Windows Server 2019 | `155.138.228.119` |
| Domain Client            | Windows 10 Pro    | `155.138.202.51`    |

---

### 🛠 Tools Used
- Splunk Enterprise (Free license for testing)
- Splunk Universal Forwarder
- Sysmon (with [Sysmon Config](https://github.com/olafhartong/sysmon-modular))
- VirtualBox / VMware (for local replication)
- Active Directory Users & Computers
- Group Policy Management Console (GPMC)
- Windows Event Viewer

## 🗂️ Configuration Summary

- Deployed three virtual machines via Vultr and configured networking to enable secure communication.
- Created the domain `mydfir.local` on the Windows Server and successfully joined the client machine.
- Installed and configured **Sysmon** for enhanced security logging on both Windows systems.
- Deployed **Splunk Universal Forwarder** to forward event logs (Security, Sysmon, etc.) to the Splunk server.
- Ingested and analyzed logs within Splunk dashboards, including failed logons, group membership changes, and process execution events.

## 🧰 Step-by-Step Lab Setup

### 🔹 1. Create Virtual Machines on Vultr

Provision three virtual machines from the Vultr dashboard and configure static IPs or track public IPs for Splunk and Windows communication.

📸 *Screenshot: Vultr dashboard showing VM instances*

---

