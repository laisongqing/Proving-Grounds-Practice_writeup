## nmap scanning
- <img width="1918" height="557" alt="image" src="https://github.com/user-attachments/assets/4ed0f76c-f72f-4888-aefd-79f1c330ec5d" />

## 80 port
- dirsearch
  - <img width="1918" height="750" alt="image" src="https://github.com/user-attachments/assets/b399bdff-7679-436a-a1df-fc10fb433131" />
  - /test/
    - <img width="1918" height="697" alt="image" src="https://github.com/user-attachments/assets/17ccf40f-f3b4-4144-80b8-0076bcb87e63" />
- /test/ 是 ZenPHOTO CMS
  - <img width="1918" height="851" alt="image" src="https://github.com/user-attachments/assets/df14e174-3473-4b55-9dbc-e53f03514c4a" />
- ZenPHOTO 的版本是 1.4.1.4
  - <img width="1918" height="840" alt="image" src="https://github.com/user-attachments/assets/447fee02-989e-4651-8eb5-813be76c9d23" />
- ZenPhoto 1.4.1.4 - 'ajax_create_folder.php' Remote Code Execution
  - https://www.exploit-db.com/exploits/18083
- 成功取得 shell
  - <img width="1282" height="603" alt="image" src="https://github.com/user-attachments/assets/3d2a07d1-865a-4a81-9a41-e26da39413a5" />
- 取得 local.txt
  - <img width="1177" height="75" alt="image" src="https://github.com/user-attachments/assets/dfbfbb63-db11-4d38-a8ab-db2543d6331e" />

## 提權
### 方法1
- linpeas.sh 發現可以利用 [CVE-2021-4034] PwnKit 提權
  - <img width="1355" height="173" alt="image" src="https://github.com/user-attachments/assets/2e3a9092-f946-4ab3-9267-1f3c4829877b" />
- 成功提權
  - <img width="1918" height="437" alt="image" src="https://github.com/user-attachments/assets/1e00493b-12db-4a3d-ac0a-40d9f0925c04" />
### 方法2
- linpeas.sh 發現可以利用 [CVE-2016-5195] dirtycow 提權
  - <img width="1918" height="671" alt="image" src="https://github.com/user-attachments/assets/e7748c33-41df-44e7-87ef-d7db6311f424" />
- 成功提權
  - <img width="1918" height="736" alt="image" src="https://github.com/user-attachments/assets/fb603939-15b8-4765-aace-f00c086f5a85" />
  - <img width="1918" height="750" alt="image" src="https://github.com/user-attachments/assets/2fd39070-d7d3-4ba6-a43e-dad633219d0d" />

## 取得 proof.txt
- <img width="627" height="76" alt="image" src="https://github.com/user-attachments/assets/49903d0a-03e9-4ff9-abaf-b5f050c19b17" />




















































