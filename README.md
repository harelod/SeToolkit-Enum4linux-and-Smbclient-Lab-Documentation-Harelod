# SeToolkit-Enum4linux-and-SMBClient-Lab-Documentation
This documentation focuses on how Setoolkit (Site Cloner) is used to clone a website and also on how to perform SMB vulnerability scaning using Enum4linux tool for testing or educational purposes only.

## 1. Objectives of Lab
### i. To explore how attackers use social engineering tool like SeToolkit to clone website in other to harvest credentials of their targets (individuals or companies).
### ii. To ethically educate learners on how to cross check websites before loging in, to aviod credential harvest by attackers.
### iii. To create awareness of SMB vulnerability scanning tool (Enum4linux &smbclient) used to identify potential threats like anonymous access to a system, shared documents and user information.


## 2. Lab Set up Environment
- Vitual Machine: Oracle Virtual Box
 - Operating System: Ethical-Hack- Kali Linux(Netacad)
 - Tools: SeToolkit (Site Cloner), Enum4linux & SMBClient
 - Add on Editor: Text Editor
 - Post back IP Address: 10.6.6.1
 - Clone Website: http://dvwa.vm
 - Enumeration Host IP address: 172.17.0.2
 - Lab Guide: Parocyber ethical hacking training


# (A) Website Clonning using SeToolkit (Site Cloner) Results & Docummentations
SeToolkit is an open source pentesting tool used to simulate social engineering attacks. In this lab we will demostrate how people or organisations can become vulnerable to social engineering using site cloner example.

## 1. Initiating SeToolkit
### Command: ``` Sudo su ``` 
### Purpose: To activate root privilege
<img width="466" height="262" alt="image" src="https://github.com/user-attachments/assets/8d41ccd7-80bc-4be6-83b3-4dac57dd7b3e" />

### Command: ``` Setoolkit ``` 
### Purpose: To start tool
<img width="940" height="927" alt="image" src="https://github.com/user-attachments/assets/980000f4-c584-432f-bdb6-495b346d50fe" />
<img width="940" height="624" alt="image" src="https://github.com/user-attachments/assets/f50df14b-388a-4a89-add6-26796ab8ec49" />

## 2. Site Cloner
<img width="620" height="310" alt="image" src="https://github.com/user-attachments/assets/6b3a4c07-a704-45c9-82de-79f7d3a750c6" />

### 1st Instruction: Type 1 & Press Enter to Select Social-Engineering Attacks Menu
<img width="691" height="418" alt="image" src="https://github.com/user-attachments/assets/1fe5a3fa-da53-497d-b2b7-a7b1006e7d4e" />

### 2nd Instruction: Type 2 & Press Enter to Select Website Attack Vectors Menu
<img width="940" height="387" alt="image" src="https://github.com/user-attachments/assets/ebb45469-e876-471e-a10c-da0ad3e2d83b" />

### 3rd Instruction: Type 3 & Press Enter to Select Credential Harvester Attack Method Menu
<img width="940" height="418" alt="image" src="https://github.com/user-attachments/assets/5483e3b6-9da2-4d29-92ef-74462c9dbdff" />

### 4th Instruction: Type 2 & Press Enter to Select Site Cloner
<img width="1134" height="535" alt="image" src="https://github.com/user-attachments/assets/750719ad-3b3f-4860-a429-3414661ffd55" />

### 5th Instruction: Type 10.6.6.1 as post back IP address & Press Enter
<img width="1157" height="123" alt="image" src="https://github.com/user-attachments/assets/c7949ca1-291d-4606-b985-94269a633843" />

### 6th Instruction: Type http://dvwa.vm as target website to clone & Press Enter
<img width="1708" height="248" alt="image" src="https://github.com/user-attachments/assets/1e441e8f-473a-45e8-87b6-4615c51223d0" />
It can be observed port 80 is used by default to host the fake/clone website.

### 7th Instruction: Open Text Editor to Create html for clone website
1 ```<html>```

2 ```<head>```

3 ```<meta http-equiv="refresh" content="0; url=http://10.6.6.1/" />```

4 ```</head>```

5 ```</html>```

### Save as hare.html on Desktop location
<img width="643" height="275" alt="image" src="https://github.com/user-attachments/assets/651f7506-4063-4bee-8d7f-2cdbc7fa1c64" />


## 3. Credential Harvester
At this stage the attacker sends an html of clone website to the victim and unknowing to the victim, he/she opens the website and log in with credential which results in the attacker having access to username and password of victim. 

### 1st Instruction: Double click saved html file (hare.html) on Desktop
<img width="1073" height="700" alt="image" src="https://github.com/user-attachments/assets/633ac593-6749-4626-b773-cb06eaceb48a" />
<img width="940" height="437" alt="image" src="https://github.com/user-attachments/assets/0ade0ae7-964f-4879-a6d3-158688e1a743" />
Nb: By double clicking file name hare.html, the clone website is open which looks exactly as original website.

### 2nd Instruction: Log in with Username:parocybertesting@gmail.com & Password: Paro@2025
<img width="1917" height="893" alt="image" src="https://github.com/user-attachments/assets/1165899c-dacf-4841-9b9c-135aa0b5e99e" />

### From above it can be observed the victim is redirected to original website. Also the clone website address was http://10.6.6.1 and original website address is http://dvwa.vm/login.php

## 3. Results of Credential Harvester
<img width="1238" height="195" alt="image" src="https://github.com/user-attachments/assets/7e15e3dc-3951-4776-85cb-426b69b6c3f0" />

It can be observed the credential used by the victim has been accessed by the attacker immediately the victim loged in.

## 4. Saving and Viewing Credential Harvester Report
### 1st Instruction: Press Ctrl + c to stop service
<img width="1274" height="127" alt="image" src="https://github.com/user-attachments/assets/3bc59e7f-0da7-4f0f-9212-115f63f20e42" />

### 2nd Instruction: 
Type 99  to return Credential Harvester Attack Method Menu
<img width="1904" height="848" alt="image" src="https://github.com/user-attachments/assets/b6d8c4db-bd64-4408-94cb-7111a225f2dc" />

Type 99 to return Website Attack Vectors Menu
<img width="1918" height="855" alt="image" src="https://github.com/user-attachments/assets/d4615083-dc73-4b6a-a90a-aa853695538b" />

Type 99 to return Social-Engineering Attacks Menu
<img width="1913" height="838" alt="image" src="https://github.com/user-attachments/assets/0f2dcc81-3c45-4a3e-8ffd-6d88a9a63c3f" />

Type 99 to return root privilege
<img width="1082" height="280" alt="image" src="https://github.com/user-attachments/assets/7c366ca7-9eaa-44ed-8f34-676ddd476ed5" />


### Command: ```cat /root/.set/reports/"2025-12-18 07:31:17.512331.xml"  ``` 
### Purpose: To view saved crendential harvester report

<img width="954" height="304" alt="image" src="https://github.com/user-attachments/assets/988fef97-3bfd-4654-910c-864e41238fc9" />

## 5. Ethical Decisions
- Before loging in to a website please kindly cross check first before inputing your credentials.

# (B) SMB Vulnerability Scanning using Enum4linux Results & Docummentations
Enum4linux is a linux base tool used for pentesting to gather username, groups, workgroup name, password policy, shared folder, printer shares and OS information.

## 1. Initiating Enum4linux
### Command: ``` Sudo su ``` 
### Purpose: To activate root privilege
<img width="466" height="262" alt="image" src="https://github.com/user-attachments/assets/8d41ccd7-80bc-4be6-83b3-4dac57dd7b3e" />

### 1st Command: ``` enum4linux ``` 
### Purpose: To start tool
<img width="940" height="642" alt="image" src="https://github.com/user-attachments/assets/2c932326-94a5-464c-ab2d-d33f8e4abf17" />
<img width="940" height="318" alt="image" src="https://github.com/user-attachments/assets/cd74e4b4-3ac2-45b5-aeba-011d64af7eda" />

### 2nd Command: ``` nmap -sN 172.17.0.2 ``` 
### Purpose: To scan for open ports
<img width="940" height="711" alt="image" src="https://github.com/user-attachments/assets/60d8a3e7-44fb-4115-869f-d681f4d5c77c" />


## 2. Userlist Information
### Command: ``` enum4linux -U 172.17.0.2 ``` 
### Purpose: To extract list of users on the host IP
<img width="940" height="563" alt="image" src="https://github.com/user-attachments/assets/a85d8da8-5cfe-46b7-9c91-65f8a79b66fe" />
<img width="940" height="611" alt="image" src="https://github.com/user-attachments/assets/93f2ede8-aead-41ff-a515-3b9441433bf1" />
<img width="737" height="992" alt="image" src="https://github.com/user-attachments/assets/e1fcb28f-4afc-427e-b386-27cab6db58a6" />


## 2. Enumerate Workgroup
### Command: ``` enum4linux -n 172.17.0.2 ``` 
### Purpose: To discover workgroup and determine if active
<img width="940" height="607" alt="image" src="https://github.com/user-attachments/assets/7a530e47-4dcd-47ee-ac2c-cce808974931" />
<img width="940" height="231" alt="image" src="https://github.com/user-attachments/assets/a539b005-318f-488e-b7ad-932ecbda5f34" />


## 3. OS Information
### Command: ``` enum4linux -o 172.17.0.2 ``` 
### Purpose: To obtain information from server on the operating system used on our target host
<img width="1315" height="457" alt="image" src="https://github.com/user-attachments/assets/e84164d0-1d6e-41c4-83e9-86107c4c562f" />
<img width="1056" height="582" alt="image" src="https://github.com/user-attachments/assets/274e914c-406b-4a38-8a70-a6b03c500bc9" />


## 4. Shared List Information
### Command: ``` enum4linux -S 172.17.0.2 ``` 
### Purpose: To obtain shared folders on our target host
<img width="1145" height="786" alt="image" src="https://github.com/user-attachments/assets/6ded4b1e-1c2e-4579-8ba1-de91436ac29b" />
<img width="1136" height="726" alt="image" src="https://github.com/user-attachments/assets/59a1c77b-9644-4c92-bf69-a1a1f4eed9ca" />
From above Printer, IPc and Admin folders are shared


## 5. Detailed Shared List Information
### Command: ``` enum4linux -Sv 172.17.0.2 ``` 
### Purpose: To obtain detailed information on shared folders on our target host
<img width="1180" height="735" alt="image" src="https://github.com/user-attachments/assets/2eaf7dcf-df5f-4ad5-8319-a1c818ee64c7" />
<img width="1267" height="682" alt="image" src="https://github.com/user-attachments/assets/c17243bd-3387-4ab6-b023-645d49d34c7c" />
<img width="1333" height="687" alt="image" src="https://github.com/user-attachments/assets/04930fd3-f380-406f-a615-d6601a9596f7" />
<img width="1431" height="175" alt="image" src="https://github.com/user-attachments/assets/a333937d-54bf-4f00-8717-44feeea6be4c" />


## 5. Password Policy
### Command: ``` enum4linux -P 172.17.0.2 ``` 
### Purpose: To determine password policy information
<img width="1170" height="652" alt="image" src="https://github.com/user-attachments/assets/efe97757-4fac-4db3-bbd6-2d02f0480267" />
<img width="1024" height="825" alt="image" src="https://github.com/user-attachments/assets/e51cad32-4289-4d35-88e8-03ed1ab57e41" />

### The information gathered can be used by an attacker for expliotation plans and also by a pentester to determine if password policy is adhered to or not on the host target.


## 5. All in one simple information gathering
### Command: ``` enum4linux -P 172.17.0.2 ``` 
### Purpose: To perfrom all simple enumeration (-U -S -G -P -r -o -n -i).
<img width="1190" height="634" alt="image" src="https://github.com/user-attachments/assets/4bde602e-ac8b-46df-b80c-078be2c1bcd8" />
<img width="1160" height="527" alt="image" src="https://github.com/user-attachments/assets/b998abaa-6088-4fd0-b524-f3c65866d7d3" />
<img width="1214" height="772" alt="image" src="https://github.com/user-attachments/assets/c643c317-46be-4ae7-bde9-248986875111" />
<img width="1137" height="626" alt="image" src="https://github.com/user-attachments/assets/5bc73955-9baa-4f14-9980-be13709bbfde" />
<img width="1142" height="828" alt="image" src="https://github.com/user-attachments/assets/c819a108-f478-4827-b937-766a27fd4f19" />
<img width="1094" height="425" alt="image" src="https://github.com/user-attachments/assets/4b526ca3-b311-4579-bc49-2aaa7a236237" />
<img width="1089" height="764" alt="image" src="https://github.com/user-attachments/assets/4fd6a990-c0d8-4756-87a8-6694b43e6d0d" />


# (c) SMBCLIENT Results & Docummentations
## 1. Initiating smbclient
### Command: ``` smbclient --help ``` 
### Purpose: To start smbclient help menu
<img width="952" height="572" alt="image" src="https://github.com/user-attachments/assets/9151335b-e5f9-42d5-81b9-83ab75d3ec14" />
<img width="907" height="361" alt="image" src="https://github.com/user-attachments/assets/1f78a0a3-1ea8-4434-ad51-e5bb081e9cb3" />


## 2. Host Shared List 
### Command: ``` smbclient -L //172.17.0.2 ``` 
### Purpose: To get list of shares
<img width="366" height="104" alt="image" src="https://github.com/user-attachments/assets/2fdb6bad-5082-4e0c-afa9-1a40537c63c4" />

### Instruction: Press Enter as Password for workgroup/root
## Result:
<img width="1101" height="486" alt="image" src="https://github.com/user-attachments/assets/c1de622a-b149-456b-a4cf-9d0204c237b6" />


## 3. Anonymous login to Host shared
### Command: ``` smbclient //172.17.0.2/tmp ``` 
### Purpose: To anonymously log in to share list tmp
<img width="583" height="166" alt="image" src="https://github.com/user-attachments/assets/b62eed72-8d8e-4dcd-8b9c-91fef0c1c4a3" />

### 1st Instruction: Type help to access help function
### Result:
<img width="773" height="419" alt="image" src="https://github.com/user-attachments/assets/4af0c9bd-4382-462a-9593-e86da2b68a40" />

### 2nd Instruction: Type dir to access directories
### Result: 
<img width="829" height="484" alt="image" src="https://github.com/user-attachments/assets/a9db2c7c-5fbe-43f8-88c8-d68530223db7" />


## 3. Creating intended Malicious File
### 1st Instruction: Open New Termical to create malicious file
### Command: ``` nano harevirus.exe ``` 
### Purpose: To create and save malicious script
<img width="1914" height="877" alt="image" src="https://github.com/user-attachments/assets/8a5d78b7-e118-45f1-832d-d4e1a5c2de34" />

### 2nd Instruction: 
- Ctrl + x to Exist
  <img width="1917" height="864" alt="image" src="https://github.com/user-attachments/assets/fc14a5a9-10b9-404d-9f8c-55bf61a0e189" />

- y to save
  <img width="1917" height="864" alt="image" src="https://github.com/user-attachments/assets/c66c86f2-8644-4766-8b0a-c4baf12c641c" />

  - Press Enter to Exist Nano Interface
    <img width="410" height="104" alt="image" src="https://github.com/user-attachments/assets/7fe97ade-91bf-4cc2-b900-dc7544202de1" />
    
## 4. View created file location and detailed content
### 1st Command: ``` ls ``` 
### Purpose: To see file saved location
<img width="1744" height="78" alt="image" src="https://github.com/user-attachments/assets/c620232d-9275-4e98-b755-e9ceeac94914" />

### 2nd Command: ``` cat harevirus.exe ``` 
### Purpose: To see file details
<img width="752" height="88" alt="image" src="https://github.com/user-attachments/assets/a735f1a3-811c-4c24-a47b-d8183d5e5ad8" />


## 3. Adding Malicious files to share directory
### 1st Instruction: Return to old terminal
### Command: ``` put harevirus.exe haregroup_work.txt ``` 
### Purpose: To add file harevirus.exe to host share
<img width="886" height="52" alt="image" src="https://github.com/user-attachments/assets/5e4dec58-66d3-4c97-b2f7-60a6e6523a8d" />

### 2nd Instruction: Type dir to see added file displayed in directory
   <img width="874" height="504" alt="image" src="https://github.com/user-attachments/assets/ecee0674-a3a4-4a20-adba-8d92449127af" />

   ### 3rd Instruction: Type quit to exist smb
   <img width="351" height="109" alt="image" src="https://github.com/user-attachments/assets/ade7cdf9-885e-4ddc-a082-812db05f10df" />



## Conclusion of Docummentation
In summary to aviod been exploited by an attacker, it is require to first cross check a website before filling in your crendentials. Site cloner is social engeenering strategy that can be adopted by an attacker to harvest your credentials before knowing. Also multi factor authentification has to be activated or enabled on websites or applications that require your credential login and strengthening password policy compliance. Moreover, misconfiguration on systems must be checked, shared folders or directories must be disabled from anonymous access or removed to aviod attackers from freely uploading malicious files or content into your share. Finally, educate users of your host service about social engineering or information gathering for expliotation by an attacker.





