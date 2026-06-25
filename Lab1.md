# Experiment 1: Virtualization Setup

## Objective

The objective of this experiment is to understand the fundamentals of virtualization and gain hands-on experience in setting up a virtual environment. By completing this experiment, students will learn how to:

- Install virtualization software (VirtualBox or VMware Workstation)
- Create and configure Virtual Machines (VMs)
- Install an Operating System inside a VM
- Allocate and manage VM resources
- Understand the concepts and benefits of virtualization

---

# Introduction

Virtualization is the technology that allows multiple operating systems to run on a single physical machine by creating virtual environments known as Virtual Machines (VMs).

A Virtual Machine behaves like a real computer with its own:

- CPU
- Memory (RAM)
- Storage
- Network Interface
- Operating System

Virtualization helps in:

- Efficient hardware utilization
- Testing and development
- Running multiple operating systems
- Cloud computing environments
- Server consolidation

---

# Software Requirements

## Option 1: VirtualBox

Download from:

https://www.virtualbox.org/

## Option 2: VMware Workstation Player

Download from:

https://www.vmware.com/

## Operating System ISO

Download any one:

### Ubuntu Linux

https://ubuntu.com/download

### Windows Evaluation Version

https://www.microsoft.com/evalcenter/

---

# Theory

## What is Virtualization?

Virtualization is the process of creating a virtual version of a computer system, operating system, storage device, or network resources.

### Traditional Environment

```text
Hardware
   ↓
Operating System
   ↓
Applications
```

### Virtualized Environment

```text
Hardware
   ↓
Hypervisor
   ↓
Virtual Machines
   ↓
Guest Operating Systems
```

---

## Hypervisor

A Hypervisor is software that creates and manages virtual machines.

### Types of Hypervisors

#### Type 1 Hypervisor (Bare Metal)

Runs directly on hardware.

Examples:

- VMware ESXi
- Microsoft Hyper-V
- Xen Server

#### Type 2 Hypervisor (Hosted)

Runs on top of an existing operating system.

Examples:

- VirtualBox
- VMware Workstation
- VMware Player

---

## Advantages of Virtualization

- Cost Reduction
- Resource Optimization
- Easy Backup and Recovery
- Safe Testing Environment
- Better Security Isolation
- Supports Multiple Operating Systems

---

# Procedure

## Step 1: Install VirtualBox

### Windows Installation

1. Download VirtualBox.
2. Run the installer.
3. Click **Next** through all installation steps.
4. Complete installation.
5. Launch VirtualBox.

### Linux Installation

```bash
sudo apt update
sudo apt install virtualbox -y
```

Verify installation:

```bash
virtualbox
```

---

## Step 2: Download an Operating System ISO

Download Ubuntu Desktop ISO:

```text
https://ubuntu.com/download/desktop
```

Save the ISO file to your system.

Example:

```text
ubuntu-24.04-desktop-amd64.iso
```

---

## Step 3: Create a Virtual Machine

Open VirtualBox.

Click:

```text
New
```

Enter:

| Setting | Value |
|----------|--------|
| Name | UbuntuVM |
| Type | Linux |
| Version | Ubuntu (64-bit) |

Click **Next**.

---

## Step 4: Allocate Memory (RAM)

Recommended:

| OS | RAM |
|-----|------|
| Ubuntu | 4 GB |
| Windows 10 | 8 GB |

Example:

```text
4096 MB
```

Click **Next**.

---

## Step 5: Create Virtual Hard Disk

Select:

```text
Create a Virtual Hard Disk Now
```

Click **Create**.

Choose:

```text
VDI (Virtual Disk Image)
```

Click **Next**.

Storage Type:

```text
Dynamically Allocated
```

Click **Next**.

Disk Size:

```text
25 GB
```

Click **Create**.

---

## Step 6: Attach Operating System ISO

Select VM.

Click:

```text
Settings → Storage
```

Under Controller IDE:

Click:

```text
Empty → Optical Drive → Choose ISO
```

Select downloaded Ubuntu ISO.

Click:

```text
OK
```

---

## Step 7: Start the Virtual Machine

Click:

```text
Start
```

The VM boots from the ISO image.

You will see the Ubuntu installer.

---

## Step 8: Install Ubuntu

Select:

```text
Install Ubuntu
```

Follow installation wizard.

Configure:

- Language
- Keyboard
- Time Zone
- Username
- Password

Wait for installation to complete.

Restart VM when prompted.

Remove installation media if requested.

---

## Step 9: Verify Installation

Login using created credentials.

Open terminal:

```bash
uname -a
```

Expected output:

```text
Linux UbuntuVM ...
```

Check memory:

```bash
free -h
```

Check disk:

```bash
df -h
```

---

# Managing VM Resources

## Modify RAM

1. Shut down VM.
2. Open Settings.
3. Select System.
4. Adjust Memory slider.

---

## Modify CPU

1. Settings
2. System
3. Processor

Allocate:

```text
2 CPUs
```

or

```text
4 CPUs
```

based on host capacity.

---

## Modify Storage

Settings → Storage

Increase virtual disk size if needed.

---

## Networking Modes

### NAT

Default mode.

```text
VM → Internet
```

Suitable for most users.

---

### Bridged Adapter

```text
VM → Same Network as Host
```

VM gets its own IP address.

Useful for server experiments.

---

## Snapshots

Snapshots allow saving VM state.

Create Snapshot:

```text
VM → Take Snapshot
```

Benefits:

- Rollback changes
- Safe experimentation
- Backup before updates

---

# Architecture Diagram

```text
+-------------------------+
| Physical Hardware       |
| CPU | RAM | Storage     |
+-----------+-------------+
            |
            v
+-------------------------+
| Hypervisor              |
| VirtualBox / VMware     |
+-----------+-------------+
            |
    -------------------
    |                 |
    v                 v
+--------+      +--------+
| VM 1   |      | VM 2   |
| Ubuntu |      | Win11  |
+--------+      +--------+
```

---

# Expected Output

Students should be able to:

- Successfully install VirtualBox/VMware
- Create a virtual machine
- Install Ubuntu or Windows inside the VM
- Allocate resources to the VM
- Configure networking
- Create snapshots
- Understand virtualization concepts

---

# Result

Successfully installed and configured a Virtual Machine using VirtualBox/VMware. The guest operating system was installed, resources were allocated, networking was configured, and virtualization concepts were understood.

---

# Viva Questions

### 1. What is virtualization?

Virtualization is the process of creating virtual versions of computing resources such as operating systems, servers, storage, or networks.

### 2. What is a Virtual Machine?

A Virtual Machine is a software-based computer that runs an operating system and applications like a physical machine.

### 3. What is a Hypervisor?

A Hypervisor is software that creates and manages virtual machines.

### 4. Name two Type-2 Hypervisors.

- VirtualBox
- VMware Workstation

### 5. What is the difference between NAT and Bridged networking?

- NAT shares the host network.
- Bridged gives the VM its own IP address.

### 6. What is a Snapshot?

A snapshot captures the current state of a virtual machine for future restoration.

### 7. Why is virtualization important in cloud computing?

Cloud providers use virtualization to efficiently allocate resources and run multiple isolated environments on shared hardware.

### 8. Can multiple operating systems run simultaneously on a single machine using virtualization?

Yes, multiple operating systems can run simultaneously using virtual machines.

---

# Conclusion

This experiment introduced virtualization technology and demonstrated how to create, configure, and manage virtual machines using VirtualBox or VMware. The knowledge gained in this experiment serves as the foundation for cloud computing, DevOps, containerization, and server management concepts explored in subsequent experiments.


```python
# Update system
sudo apt update -y

# Install Nginx
sudo apt install nginx -y

# Start and enable Nginx
sudo systemctl start nginx
sudo systemctl enable nginx

# Go to web root
cd /var/www/html

# Fix permission
sudo chown -R ubuntu:ubuntu /var/www/html

# Remove default files
sudo rm -rf *

# Go to home directory (safe place to clone)
cd ~

# Clone your GitHub repo
git clone https://github.com/hamza-shabbir-ansari/Restaurant-website.git

# Move files to nginx folder
sudo cp -r Restaurant-website/* /var/www/html/

# Restart nginx
sudo systemctl restart nginx


```

```python
sudo apt update -y

sudo apt install nginx -y

sudo systemctl start nginx
sudo systemctl enable nginx

cd /var/www/html

sudo chown -R ubuntu:ubuntu /var/www/html

sudo rm -rf *

cd ~

git clone https://github.com/hamza-shabbir-ansari/Restaurant-website.git

sudo cp -r Restaurant-website/* /var/www/html/

sudo systemctl restart nginx




```
