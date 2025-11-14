## nmap scanning
- <img width="1918" height="592" alt="image" src="https://github.com/user-attachments/assets/49b26414-5768-4341-a650-560e0db8852e" />

## 80 port
- dirsearch 掃 /
  - <img width="1918" height="535" alt="image" src="https://github.com/user-attachments/assets/87e48394-1fc4-426d-98d3-3dc76f94223d" />
- http://192.168.186.145/ 點選 Scheduler 會跳轉到 /openemr/interface/login/login.php?site=default
  - <img width="1918" height="825" alt="image" src="https://github.com/user-attachments/assets/e4540ab7-8758-4c2c-8cd1-c22759fd2d9e" />
- dirsearch 掃 /filemanager/
  - <img width="1343" height="705" alt="image" src="https://github.com/user-attachments/assets/a73b464a-a22e-4162-b29e-1959c8e83366" />
- http://192.168.186.145/filemanager/ 發現是 filemanager v.9.13.4
  - <img width="1918" height="813" alt="image" src="https://github.com/user-attachments/assets/4bf98dd7-d2f2-4fbd-ad01-8f3e4ec503f1" />
- Responsive FileManager 9.13.4 - 'path' Path Traversal
  - https://www.exploit-db.com/exploits/49359
- 可以藉由 LFI 將靶機上的檔案上傳到 FileManager 上面的 Documents 底下，所以要改 code
  - <img width="822" height="585" alt="image" src="https://github.com/user-attachments/assets/f0c13045-cbc3-417d-9de5-7f570e3433ec" />
- 成功將 /etc/passwd 上傳到 Documents 底下
  - <img width="1918" height="670" alt="image" src="https://github.com/user-attachments/assets/b7d453d1-501f-4875-bd7e-a87baecf350c" />
- openemr default credential path 是 openemr/sites/default/sqlconf.php
  - <img width="835" height="120" alt="image" src="https://github.com/user-attachments/assets/3a0216ca-9037-436d-b2d5-f63346ced0ad" />
  - <img width="1918" height="687" alt="image" src="https://github.com/user-attachments/assets/a43881be-c638-47c7-b8b7-119a1d4050bc" />
- 成功將 /var/www/openemr/sites/default/sqlconf.php 上傳到 Documents 底下
  ```
  python3 49359.py http://192.168.186.145 PHPSESSID=fb6854ntr72vtlemkjiipn86m6 /var/www/openemr/sites/default/sqlconf.php
  ```
## 445 port
- smbclient 匿名登入將 sqlconf.php get 下來
  - <img width="1918" height="397" alt="image" src="https://github.com/user-attachments/assets/779dcefd-556d-44c5-b941-94560aff3708" />
- 發現 mysql 的帳號密碼
  - <img width="1918" height="732" alt="image" src="https://github.com/user-attachments/assets/931f2d1a-3ea8-4102-a976-4b57bcd4dfe5" />

## 3306 port
- 成功登入 mysql 發現 admin 密碼
  ```
  mysql -h 192.168.186.145 -u openemr --skip-ssl -p
  ``` 
  - <img width="1918" height="395" alt="image" src="https://github.com/user-attachments/assets/a112f22a-5436-4177-9362-6b164481da29" />
- 成功破解
  - <img width="1465" height="291" alt="image" src="https://github.com/user-attachments/assets/cd621ff0-e34c-48bc-8701-b267f2b4a0e2" />

## 80 port
- 成功登入 openemr
  - <img width="1918" height="837" alt="image" src="https://github.com/user-attachments/assets/984b9a65-840f-4dba-96e1-51502eb9cab2" />
- OpenEMR 版本是 v5.0.1 (1)
  - <img width="1918" height="817" alt="image" src="https://github.com/user-attachments/assets/7419f690-ee0a-4cff-8a89-eec8293ab0ba" />
- OpenEMR 5.0.1.3 - Remote Code Execution (Authenticated)
  - https://www.exploit-db.com/exploits/45161
- 要改 code
  - <img width="832" height="580" alt="image" src="https://github.com/user-attachments/assets/2c48eb64-0c0b-469f-9bed-de86c3ced7b1" />
- 成功取得 shell
  - <img width="1918" height="683" alt="image" src="https://github.com/user-attachments/assets/f20da87f-884e-4e50-afbb-2a1ed86a835a" />
- 取得 local.txt
  - <img width="913" height="80" alt="image" src="https://github.com/user-attachments/assets/cb8760bf-aece-40d6-8a85-46909f44d084" />

## 提權
- linpeas.sh 發現可以用 [CVE-2021-4034] PwnKit 提權
  - <img width="1428" height="335" alt="image" src="https://github.com/user-attachments/assets/fccfaa62-3c30-4333-b919-16aae1c33bee" />
- 成功提權
  - <img width="1918" height="517" alt="image" src="https://github.com/user-attachments/assets/98732afa-bf3c-495d-9c15-3556ca8ad587" />
- 取得 proof.txt
  - <img width="530" height="78" alt="image" src="https://github.com/user-attachments/assets/a869a2ec-5c84-4275-b7ad-fd965044aa65" />











































