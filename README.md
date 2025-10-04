# creating-a-backdoor-with-SET
creating a backdoor with SET - Ethical Hacking Techniques course

# AIM:
To Create a backdoor with Social Engineering Toolkit (SET)

## DESIGN STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode


### Step 2:

Investigate on the various categories of tools as follows:

### Step 3:

Open terminal and try execute some kali linux commands

### Architecture Diagram

```
+----------------+        +------------------------+        +----------------------+
| Attacker's PC  | -----> | SET (Credential        | -----> | Fake Login Page      |
| (Kali Linux)   |        | Harvester via Apache)  |        | (Hosted by SET)      |
+----------------+        +------------------------+        +----------------------+
       |                                                             |
       |                                                             v
       |   1. Configure SET with phishing site (e.g., Gmail clone)   |
       |                                                             |
       |                                                             v
       |                                                 +----------------------+
       |                                                 | Victim's Browser     |
       | <------------------------------------------------| Clicks Phishing Link|
       |                                                 +----------------------+
       |                                                             |
       |                                                             v
       |     2. Victim Enters Credentials → Sent to SET/Attacker    |
       |                                                             |
       |                                                             v
       |                                                 +----------------------+
       |                                                 | Credentials Captured |
       |                                                 | in Apache log/SET DB |
       |                                                 +----------------------+

```

## EXECUTION STEPS AND ITS OUTPUT:
Social Engineering attacks are the various cons used by the hackers to trick people into providing sensitive data to the attackers.

**Steps to Use SET for Phishing (Credential Harvester Attack Method)**

**1. Open terminal:**
```bash
sudo setoolkit
```
<img width="1050" height="881" alt="Screenshot 2025-09-25 083745" src="https://github.com/user-attachments/assets/6b6f544b-f320-49c1-b77d-f965c5460d7d" />


**2. Navigate:**
```bash
1) Social-Engineering Attacks  
2) Website Attack Vectors  
3) Credential Harvester Attack Method  
```

<img width="1917" height="896" alt="Screenshot 2025-09-25 084240" src="https://github.com/user-attachments/assets/11a6bc1e-7907-4e70-9116-441c7d3d43c3" />

<img width="1642" height="700" alt="Screenshot 2025-09-25 084432" src="https://github.com/user-attachments/assets/e5f8bf6f-45fa-4cec-b2b2-6f30771eb1f8" />

<img width="1399" height="790" alt="Screenshot 2025-09-25 084503" src="https://github.com/user-attachments/assets/090a5838-12f5-44f6-8f14-e2728c564d2c" />

<img width="1913" height="819" alt="Screenshot 2025-09-25 084840" src="https://github.com/user-attachments/assets/ece8acd0-ddc5-4a44-9b51-8d3ea74a6e51" />





**3. Enter your IP address as the attacker server.**
192.168.184.30
**4. Choose:**
```bash
2) Site Cloner
```
<img width="1467" height="762" alt="image" src="https://github.com/user-attachments/assets/e4c648d6-638b-4374-8abd-13f5ab1fefdd" />

**5. Enter the URL of the legitimate site ```(e.g., https://accounts.google.com)```**
<img width="1232" height="207" alt="image" src="https://github.com/user-attachments/assets/7796eafc-d55a-4935-b485-f6985cbdd188" />

**6. Send the generated link to the victim.**

<img width="1918" height="921" alt="image" src="https://github.com/user-attachments/assets/f099d702-926c-44b8-b43b-5f35e3b4424b" />


**7. Once the victim logs in → their credentials are stored in:**
```bash
/var/www/html/
```
192.168.184.30

<img width="1918" height="987" alt="image" src="https://github.com/user-attachments/assets/c75e74ea-a511-438f-840f-89435806f6c8" />




## RESULT:
The Social Engineering Toolkit (SET) is used to create backdoor is  examined successfully
