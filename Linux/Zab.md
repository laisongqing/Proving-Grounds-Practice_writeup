## nmap scanning
- <img width="1918" height="531" alt="image" src="https://github.com/user-attachments/assets/052ee135-e906-4bcd-a2cf-b7f9ff319ae9" />

## 6789 port
- Mage AI
  - <img width="1918" height="832" alt="image" src="https://github.com/user-attachments/assets/350402bc-2dc2-4166-bed5-4f9f577c0b68" />
- terminal 取得 shell
  - <img width="1918" height="667" alt="image" src="https://github.com/user-attachments/assets/d2108853-e489-41bb-b476-f3985e205c89" />
- 取得 local.txt
  - <img width="1918" height="840" alt="image" src="https://github.com/user-attachments/assets/67eb92ef-a9eb-46ca-84b9-26b8c7d385ee" />

## 提權
- 發現 zabbix 帳密
  ```
  cat /etc/zabbix/web/zabbix.conf.php
  ```
  - <img width="1918" height="752" alt="image" src="https://github.com/user-attachments/assets/ef4b75ef-20bf-4339-8c32-d2c7fc702f32" />
- 登入 mysql 發現 Admin 的帳密
  - <img width="1918" height="383" alt="image" src="https://github.com/user-attachments/assets/269c38ee-db3a-44ad-ae4d-87b4c3575174" />
- 成功解密
  - <img width="1918" height="286" alt="image" src="https://github.com/user-attachments/assets/0a4c3e66-6988-4c7d-b750-d10c790175b9" />
- 發現有開 10050 port (Zabbix Agent)
  - <img width="1918" height="440" alt="image" src="https://github.com/user-attachments/assets/870ddb11-739a-4d7f-8f05-a99176d67496" />
  - <img width="1227" height="610" alt="image" src="https://github.com/user-attachments/assets/6936bc27-4459-4246-b9dd-9360839fce9c" />
- 用 chisel 將 zabbix 網頁導到 kali 上
  - kali
    - <img width="1918" height="225" alt="image" src="https://github.com/user-attachments/assets/95fb73b6-3ad5-4a78-8ef8-eb5c84303ebb" />
  - 靶機
    - <img width="1462" height="126" alt="image" src="https://github.com/user-attachments/assets/8b4b5c31-c593-4fa7-a1bd-e92791ebf1b1" />
- dirsearch 發現 http://localhost:8080/ 底下有個 /zabbix 是 zabbix 登入頁面
  - <img width="1918" height="652" alt="image" src="https://github.com/user-attachments/assets/f77d274b-b4f1-486d-abae-05d2aa90f9f8" />
  - <img width="1917" height="845" alt="image" src="https://github.com/user-attachments/assets/c6468223-612a-44bf-bb16-2a14e119808e" />
- 用 Admin:dinosaur 成功登入
  - <img width="1918" height="845" alt="image" src="https://github.com/user-attachments/assets/810533e0-e450-4e51-9119-f076584dd921" />
- Alerts -> Scripts 建立 script
  - <img width="1918" height="840" alt="image" src="https://github.com/user-attachments/assets/5f2a1edd-a0ae-46ec-90e0-1960b3b6c683" />
- Monitors -> Hosts 點擊 Zabbix server 選擇 reverse_shell 成功取得 shell
  - <img width="1918" height="823" alt="image" src="https://github.com/user-attachments/assets/47c25347-153a-4c35-b4fc-64f153c4185d" />
- sudo -l 發現可以 sudo /usr/bin/rsync 提權
  - <img width="1918" height="275" alt="image" src="https://github.com/user-attachments/assets/2593fad0-60b3-424e-a366-cca9b913b8fb" />
- GTFOBins 
 - <img width="1095" height="262" alt="image" src="https://github.com/user-attachments/assets/8e4573f0-c935-4667-80d2-c87fc2bef7a5" />

- 成功提權
  - <img width="1313" height="152" alt="image" src="https://github.com/user-attachments/assets/8fe7ce42-79ea-4b25-af2d-b5da384d2f8b" />
- 取得 proof.txt
  - <img width="637" height="107" alt="image" src="https://github.com/user-attachments/assets/66eb409c-4905-40bf-a0c3-553032145b36" />




















































