## nmap scanning
- <img width="1918" height="760" alt="image" src="https://github.com/user-attachments/assets/0c985700-4b50-45e1-a02c-aa6b1ff36b2f" />

## 445 port
- enum4linux、crackmanexec、smbclient 都沒資訊
- nmap 掃 smb 漏洞發現存在 cve2009-3103 (ms09-050)
  ```
  nmap -p 135,139,445 -sV -Pn -T4 192.168.165.40 --script "smb-vuln-*,smb-os-discovery,smb-protocols,smb-security-mode"
  ```
  - <img width="1918" height="765" alt="image" src="https://github.com/user-attachments/assets/17257519-780e-4b7e-9a88-32e9025bc6ea" />
- msfconsole
  ```
  windows/smb/ms09_050_smb2_negotiate_func_index
  ```
  - <img width="1918" height="532" alt="image" src="https://github.com/user-attachments/assets/762e3bb5-427f-496c-a57b-8c7b6a2b3f66" />
- 取得 proof.txt
  - <img width="1302" height="100" alt="image" src="https://github.com/user-attachments/assets/85a83682-0e3d-457d-b259-ca1cb35783fa" />

















































