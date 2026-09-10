# 🔐 Cybersecurity & Pentesting Lab Setup

This is my Week 1 project for the Cybersecurity Program at Networkwalks (Batch B082).

In this project, I set up a basic cybersecurity lab using VirtualBox and Kali Linux. The lab will be used to practice cybersecurity concepts in a controlled environment.

## 🎯 Objectives

The main objectives of this project were to:

- Set up VirtualBox
- Install and configure Kali Linux
- Create a private NAT Network
- Configure Kali Linux network settings
- Test network connectivity

## 🛠️ Tools Used

- VirtualBox
- Kali Linux
- 7-Zip

## ⚙️ Lab Configuration

| 🧩 Component | ⚙️ Configuration |
|---|---|
| 🖥️ Host OS | Windows 10 |
| 🧠 Host RAM | 4 GB |
| ⚡ Processor | Intel Core i5 |
| 🧰 Hypervisor | VirtualBox 7.2 |
| 🐉 Security OS | Kali Linux 2026.2 |
| 🚪 Default Gateway | 10.0.0.1 |
| 🧠 Kali RAM | 2048 MB |
| 🌍 DNS Server | 8.8.8.8 |
| 🌐 Virtual Network | NAT Network |
| 📡 Network Address | 10.0.0.0/24 |
| 🐧 Kali IP Address | 10.0.0.2/24 |

## ⚙️ Lab Setup Process

### 1. Installing 7-Zip

I installed 7-Zip to extract the Kali Linux virtual machine files before importing them into VirtualBox.

📸 **Screenshot:**

![7-Zip Installation](images/<img width="1363" height="730" alt="Zip installation" src="https://github.com/user-attachments/assets/65b3868a-e107-43db-9b8c-296496d3da4a" />
)



---

### 2. Installing VirtualBox

I installed VirtualBox and used it to create and manage my Kali Linux virtual machine.

📸 **Screenshot:**

![VirtualBox](images/<img width="1366" height="768" alt="virtualbox" src="https://github.com/user-attachments/assets/f90b569f-8e98-414c-a1d7-b54a9f4356a2" />
)

---

### 3. Creating the NAT Network

I created a private NAT Network in VirtualBox to allow the virtual machines in the lab to communicate with each other.

**Network:** `10.0.0.0/24`

📸 **Screenshot:**

![NAT Network](images/<img width="1366" height="767" alt="NAT" src="https://github.com/user-attachments/assets/12c88516-ce41-4ae2-9330-80ca898362af" />
)

---

### 4. Setting Up Kali Linux

I imported Kali Linux into VirtualBox and configured the virtual machine to use the NAT Network.

**Kali RAM:** `2048 MB`

📸 **Screenshot:**

![Kali Linux Settings](images/<img width="1366" height="768" alt="kali conf" src="https://github.com/user-attachments/assets/b78e0a3d-a093-427a-ae57-635d88478fc4" />
)

---

### 5. Configuring the Network

I checked the network settings in Kali Linux and configured the IP address, gateway, and DNS.

```text
IP Address: 10.0.0.2
Subnet Mask: 255.255.255.0
Gateway: 10.0.0.1
DNS: 8.8.8.8 
```
## 🐞 Problems I Encountered & How I Solved Them

### 1. VirtualBox Could Not Start Kali Linux

At first, the Kali Linux virtual machine failed to boot and showed an error saying that the virtual machine could not find a bootable operating system.

I checked the VM settings, especially the storage and boot configuration, to make sure the Kali virtual disk was properly connected.

### 2. VirtualBox Was Not Recognized in Command Prompt

When I tried to use `VBoxManage` from Command Prompt, Windows showed that the command was not recognized.

I solved this by running the VirtualBox executable using its full installation path.

```cmd
"C:\Program Files\Oracle\VirtualBox\VBoxManage.exe" list vms
```
This allowed me to view the Kali virtual machines registered in VirtualBox.

3. Managing Multiple Kali VMs

I found two Kali Linux virtual machines registered in VirtualBox. Instead of deleting one immediately, I checked which VM was working correctly before making any changes.

This taught me to verify a virtual machine before deleting or modifying it.


