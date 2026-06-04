## Install virtual box and ubutntu Desktop

- Once u done then we can do

## Check once in termina weather its installed or not

- Method 1: Check VirtualBox Version

- Open CMD and run:
```python
VBoxManage --version
```
- If VirtualBox is installed and added to PATH, you'll see something like:
```python
7.2.8r168469
```

### OR try this cmd 

```pyhton
"C:\Program Files\Oracle\VirtualBox\VBoxManage.exe" --version

```
## then u see the version
```python

7.1.6rXXXXX
```

## What you should do now
```python
Open Oracle VM VirtualBox
Click New
Create a VM with:
Name: Ubuntu24 (or Ubuntu26)
Type: Linux
Version: Ubuntu (64-bit)
RAM: 4096 MB
CPU: 2 cores
Disk: 25 GB
When VirtualBox asks for an ISO Image, browse and select the Ubuntu file you just downloaded (.iso).
Finish creating the VM.
Click Start.
```

### Fix 1: Change Graphics Controller
```python
Close the VM (Power Off).
In VirtualBox, select your Ubuntu VM.
Click Settings → Display.
Change:
Graphics Controller:
VMSVGA  →  VBoxSVGA
Uncheck:
Enable 3D Acceleration
Click OK.
Start the VM again.
```
```python
Graphics Controller : VBoxSVGA
Enable 3D Acceleration : OFF
Video Memory : 128 MB (if available)

```
```python
1. Check Linux Version
uname -a
2. Check RAM
free -h
3. Check CPU
lscpu
4. Check Disk Space
df -h
5. Check Current User
whoami
```
