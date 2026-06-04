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
https://login.us-east-1.auth.skillbuilder.aws/otp/input/response?redirect_uri=https%3A%2F%2Fus-east-1.auth.skillbuilder.aws%2Foauth2%2Fidpresponse&state=H4sIAAAAAAAAAG2R2W6jMBSG38XXIcUY2zh3WQkkaRJKWphRFQFmjQOEJTSt5t3H1UijuZi7T_qXc6T_CwRgAvpWiYO2U-B5E3nmcyccH4xAKJW9e5AUSdJpnGch4fe4TMIEVzm7N0RnuIykgUtD1nV1O3l6ElWal-O_leOg77Jxe8mFCPtc8LgZB0P7x_XUxG1dlW0sK2JZEVX8G5Pvw9ZiLjEFk5-gquMy5-B9BDKptJ3nJlEu-tVgW8GV7XKoPiBba_vt6eL6qUIwojrGEFMCKaUBMRDFmMQUE6RrWNWpziklTDd0iDji8kwue9NTYSUlCTp_0ylqZKLso0LHqoirJSnwbcXtdhCfmPVWJROFTLxomEi8SFx8nG_Tzau1Gxb8gAbvskHQRSmB7koo68Tn-0LxHozXx-O5bOxpuaXNm_95nTv528xcm9lq8bzfmtsbnV12QtxsX7xEe0uN4a4f-tnqbthNOS3npJpii85TcnXWJnrl7sHG9Lz7UT78fH931eI6O88Ip7UDuWcsS7Jgm2Wbn6Zu4feOcFpPlR-Lfzf__0DSdQUTSA0VM6IyPAI1mCSBaOMRaGScBVw3WJAoJFRVRYchVIxIw0pIUKhRxDSGNdlxl_u9__oNw3nhJmYCAAA.H4sIAAAAAAAAANvdOdWpNK9mtlHv3L_yLissFRwnvZ1ok_T2m_dqa-PAM28B0JkktCAAAAA.4
