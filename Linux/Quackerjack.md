## nmap scanning
- <img width="1918" height="756" alt="image" src="https://github.com/user-attachments/assets/54968e59-27ae-49e1-8c84-956f76e99b28" />
- <img width="1918" height="697" alt="image" src="https://github.com/user-attachments/assets/ab156911-d6f7-41a4-9bda-19d3fa8e1b4a" />

## 8081 port
- 直接到 rConfig 的登入頁面，版本是 rConfig Version 3.9.4 
  - <img width="1918" height="821" alt="image" src="https://github.com/user-attachments/assets/a3932108-b8ca-413d-a4d6-98056b22a820" />
- rconfig <= 3.9.4 有很多漏洞，發現有開 mysql 服務，所以先嘗試爆 sql 的資料
  - https://github.com/v1k1ngfr/exploits-rconfig
- 成功爆出 mysql 的使用者帳密 (CVE-2020-10220 : unauthenticated SQL)
  - https://github.com/v1k1ngfr/exploits-rconfig/blob/master/rconfig_CVE-2020-10220.py
  - <img width="1517" height="725" alt="image" src="https://github.com/user-attachments/assets/4bf53790-18c9-4c3b-9851-31ba3d544f10" />
- 成功破解 admin 的密碼
  - <img width="1918" height="655" alt="image" src="https://github.com/user-attachments/assets/634a6359-6a2c-49a6-aead-36eec778e59a" />
- 成功登入
  - <img width="1918" height="818" alt="image" src="https://github.com/user-attachments/assets/71637423-b5ef-4452-a202-bd3523c55a50" />
- rConfig 3.9.4 - 'searchField' Unauthenticated Root Remote Code Execution
  - https://www.exploit-db.com/exploits/48261
- 成功取得 shell
  - <img width="1918" height="760" alt="image" src="https://github.com/user-attachments/assets/0200ee2c-4bb9-4e22-b650-c6b1daa92fd6" />
- 取得 local.txt
  - <img width="922" height="151" alt="image" src="https://github.com/user-attachments/assets/e3ce19f6-fb3a-4a72-9727-bacf961d1594" />

## 提權
- linpeas.sh 發現 /usr/bin/find 存在 suid 提權
  - <img width="1918" height="631" alt="image" src="https://github.com/user-attachments/assets/5b45bc87-dfbc-40a7-a5b4-4cafa638fb1e" />
- GTFOBins 
  - <img width="1362" height="368" alt="image" src="https://github.com/user-attachments/assets/bf387d79-0a1d-473c-8809-c136a347bdf0" />
- 成功提權
  - <img width="857" height="190" alt="image" src="https://github.com/user-attachments/assets/e6b66f34-23e9-40ba-969d-5c73d591451d" />
- 取得 proof.txt
  - <img width="837" height="103" alt="image" src="https://github.com/user-attachments/assets/c0ede3e3-de97-4bbd-90ea-ef264c5a5604" />












































