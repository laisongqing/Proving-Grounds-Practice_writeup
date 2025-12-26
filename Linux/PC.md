## nmap scanning
- <img width="1918" height="482" alt="image" src="https://github.com/user-attachments/assets/8e7533e1-25a0-4ba1-ac54-c4dd24cea41c" />

## 8000 port
- 直接 sh 回連到 kali 上
  - <img width="1918" height="768" alt="image" src="https://github.com/user-attachments/assets/cc74c8ae-5be7-409b-8dd8-315bdfd5b02e" />

## 提權
- ss -tuln 發現本地有開 65432 port
  - <img width="1918" height="217" alt="image" src="https://github.com/user-attachments/assets/3be91689-b69a-44ce-a92e-9cdaadbb52f1" />
- 加上 root 有執行 /opt/rpc.py
  - <img width="1918" height="752" alt="image" src="https://github.com/user-attachments/assets/5df48c25-96be-43dd-9273-c6a76a4e1cd1" />
- rpc.py 0.6.0 - Remote Code Execution (RCE)
  - https://www.exploit-db.com/exploits/50983
- 修改程式碼(把 3D 全刪掉，並在 exec_command 輸入指令)成功提權
  - <img width="1918" height="747" alt="image" src="https://github.com/user-attachments/assets/c563a6dd-6672-4a25-8359-988164c1174d" />
  - <img width="1918" height="185" alt="image" src="https://github.com/user-attachments/assets/b660d7e0-d490-4469-a587-e920de9de873" />
  - <img width="1262" height="185" alt="image" src="https://github.com/user-attachments/assets/ce5e45bf-149d-4659-9038-407cdb4fdd0a" />
- 取得 proof.txt
  - <img width="682" height="98" alt="image" src="https://github.com/user-attachments/assets/01ef7180-98c4-4666-8d9b-8cbce211d453" />














































