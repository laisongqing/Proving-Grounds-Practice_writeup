## nmap scanning
- <img width="1918" height="588" alt="image" src="https://github.com/user-attachments/assets/e13d14b1-ee71-481d-8d34-7631df447a5c" />

## 8081 port
- Sonatype Nexus Repository Manager 3.21.0-05
  - <img width="1918" height="817" alt="image" src="https://github.com/user-attachments/assets/99d48e89-13bc-4afc-af81-0307f26fc783" />
- 嘗試 nexus:nexus 成功登入
  - <img width="1918" height="827" alt="image" src="https://github.com/user-attachments/assets/64a11454-2e90-4cc7-be79-f7568ef6de59" />
- Sonatype Nexus 3.21.1 - Remote Code Execution (Authenticated)
  - https://www.exploit-db.com/exploits/49385
- 要改程式碼，上傳 nc.exe 並執行 nc.exe 取得 shell
  - <img width="977" height="585" alt="image" src="https://github.com/user-attachments/assets/d07ea7a7-bad4-41ff-be73-5492567ce40f" />
- 成功取得 shell
  - <img width="1918" height="615" alt="image" src="https://github.com/user-attachments/assets/012f2256-4080-434d-9465-8f73db114205" />
- 取得 local.txt
  - <img width="1043" height="488" alt="image" src="https://github.com/user-attachments/assets/fb8033d1-1873-4569-a975-bea0822c79d4" />

## 提權
- whoami /priv 發現可以用 SeImpersonatePrivilege 提權
  - <img width="1397" height="377" alt="image" src="https://github.com/user-attachments/assets/d018e905-85cb-485b-a249-fa5ac1b9f118" />
- 成功用 GodPotato 提權
  - <img width="1918" height="833" alt="image" src="https://github.com/user-attachments/assets/88a8cbda-2e50-426b-a5dc-e85609b3bca5" />
- 取得 proof.txt
  - <img width="1083" height="427" alt="image" src="https://github.com/user-attachments/assets/95c8aafd-f247-4be8-ae45-58c835e59e48" />












































