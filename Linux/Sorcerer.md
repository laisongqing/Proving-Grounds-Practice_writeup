## nmap scanning
- <img width="1918" height="755" alt="image" src="https://github.com/user-attachments/assets/90bf9a7a-fa62-4276-ad48-1b5378557d72" />

## 7742 port
- feroxbuster 發現 /zipfiles 底下有 zip 檔
  - <img width="1918" height="755" alt="image" src="https://github.com/user-attachments/assets/d0ad4ee3-670e-4d1f-9fb9-f05959fda438" />
- 解壓縮後，發現 max 家目錄底下有 .ssh
  - <img width="662" height="523" alt="image" src="https://github.com/user-attachments/assets/3668f163-15c3-4f30-8cce-e7c91d174322" />
- 在 kali 上產 id_rsa 和 id_rsa.pub
  ```
  ssh-keygen -t rsa
  ```
- 再將產出的 id_rsa.pub 改名成 authorized_keys 搭配 scp 將 authorized_keys 上傳到 max 的 .ssh 底下
  ```
  scp -i id_rsa -O /home/kali/Desktop/authorized_keys max@192.168.219.100:/home/max/.ssh/
  ```
  - <img width="1918" height="195" alt="image" src="https://github.com/user-attachments/assets/96e2bd31-6c73-4d4f-8a60-9d172e17cf54" />
- 成功用自建的 id_rsa 登入 max
  - <img width="1273" height="237" alt="image" src="https://github.com/user-attachments/assets/f3483938-c7c1-467a-8a97-df0adf9b1cb0" />
- 取得 local.txt
  - <img width="1160" height="101" alt="image" src="https://github.com/user-attachments/assets/ae091ffb-12ef-4323-9379-bc803e40241d" />

## 提權
- 發現 start-stop-daemon 可以用 suid 提權
  - <img width="1572" height="390" alt="image" src="https://github.com/user-attachments/assets/e245730a-1443-43e0-acb1-fd2505d98110" />
- GTFOBins 
  - <img width="1252" height="360" alt="image" src="https://github.com/user-attachments/assets/fda2f64c-43e2-450b-b80d-4c2a9d6835a2" />
- 成功提權
  - <img width="1265" height="112" alt="image" src="https://github.com/user-attachments/assets/54c82ee6-788e-498c-bb70-a2bac8948d33" />
- 取得 proof.txt
  - <img width="602" height="75" alt="image" src="https://github.com/user-attachments/assets/c23b31da-c0f2-4796-803b-b8bf0e75e71c" />














































