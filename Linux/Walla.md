## nmap scanning
- <img width="1918" height="722" alt="image" src="https://github.com/user-attachments/assets/54026358-6b20-40cc-b862-1324f2a6bcf2" />
- <img width="1916" height="462" alt="image" src="https://github.com/user-attachments/assets/611b4a43-7d97-4666-b6cb-2e8d9de051ad" />

## 8091 port 
- 網頁是 RaspAP
  - <img width="1918" height="246" alt="image" src="https://github.com/user-attachments/assets/100f8f12-b548-43d3-a6a6-75b86b7658e1" />
- 訪問 http://192.168.210.97:8091/ 發現需要登入
  - <img width="1048" height="736" alt="image" src="https://github.com/user-attachments/assets/b45b0391-3287-4f2b-b4d5-69593d4896c9" />
- RaspAP 預設帳密是 admin:secret，成功登入
  - <img width="1917" height="862" alt="image" src="https://github.com/user-attachments/assets/a0de0826-513c-431f-a38f-ebf4af54250b" />
- 發現 RaspAP 版本是 v2.5
  - <img width="1918" height="852" alt="image" src="https://github.com/user-attachments/assets/66ba8c0f-a858-41dd-b278-b0373f094071" />
- CVE-2020-24572
  - https://github.com/lb0x/cve-2020-24572
  - https://github.com/gerbsec/CVE-2020-24572-POC
- 成功取得 shell
  - <img width="1918" height="633" alt="image" src="https://github.com/user-attachments/assets/dd28de25-0890-4cee-aa5f-906785df624a" />
- 取得 local.txt
  - <img width="1322" height="138" alt="image" src="https://github.com/user-attachments/assets/3545e2a3-460d-411c-b461-47c607ef36f0" />

## 提權
- 發現 www-data 可以 sudo 執行 /usr/bin/python /home/walter/wifi_reset.py
  - <img width="1502" height="362" alt="image" src="https://github.com/user-attachments/assets/202cda23-ed8b-4ff4-9e05-c57be95e3f0f" />
- 發現需要 wificontroller module
  - <img width="1062" height="108" alt="image" src="https://github.com/user-attachments/assets/cda6827d-59e6-476c-b3b3-ebdc07ff8137" />
- 可以建立假的 wificontroller 取得 shell
  - https://rastating.github.io/privilege-escalation-via-python-library-hijacking/
- 寫 python reverse shell 到 wificontroller.py
  - <img width="1312" height="102" alt="image" src="https://github.com/user-attachments/assets/de111177-249f-4da9-995e-1f85dbd6789d" />
- 成功提權
  - <img width="1006" height="72" alt="image" src="https://github.com/user-attachments/assets/98c63003-075e-49c1-ab37-6e420f2b7e51" />
- 取得 proof.txt
  - ![Uploading image.png…]()































































