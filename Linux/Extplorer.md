## nmap scanning
- <img width="1918" height="497" alt="image" src="https://github.com/user-attachments/assets/5c171390-c03f-4203-846b-fe63acea1d22" />

## 80 port
- dirsearch
  - <img width="1918" height="582" alt="image" src="https://github.com/user-attachments/assets/a48cb7c9-83c1-4092-af0e-d6fc969bcddc" />
- /filemanager/ 是 eXtplorer 的登入頁面
  - <img width="1918" height="826" alt="image" src="https://github.com/user-attachments/assets/4bde0ebe-568a-4609-a3b5-2a92a2048948" />
- 用 admin:admin 成功登入
  - <img width="1918" height="862" alt="image" src="https://github.com/user-attachments/assets/2185d3d5-da39-4759-a4b1-bb0209dea723" />
- 在 /filemanager/ftp_tmp 底下上傳 php reverse shell 並且改權限為 777
  - <img width="1918" height="806" alt="image" src="https://github.com/user-attachments/assets/c6952aa1-afba-4b48-8ff9-1395f5135d62" />
  - <img width="1917" height="848" alt="image" src="https://github.com/user-attachments/assets/294b8838-a260-4163-8c4d-9f3457417968" />
- 訪問 /filemanager/ftp_tmp/shell.php 成功取得 shell
  - <img width="1918" height="552" alt="image" src="https://github.com/user-attachments/assets/5531e167-88be-46ad-9401-569cbd1e2ea2" />

## 提權
- 在 /var/www/html/filemanager/config/.htusers.php 發現帳號密碼
  - <img width="1918" height="511" alt="image" src="https://github.com/user-attachments/assets/951f0400-b728-4bae-99d6-bb1b3bcc2e36" />
- john 成功破解密碼
  - <img width="1918" height="281" alt="image" src="https://github.com/user-attachments/assets/3cbb2d81-a33d-4609-a0c4-7e5570686b6f" />
- 成功登入 dora
  - <img width="1275" height="215" alt="image" src="https://github.com/user-attachments/assets/52100169-69fc-43bb-97b8-17d28f7dfdd3" />



















































