## nmap scanning
- <img width="1918" height="695" alt="image" src="https://github.com/user-attachments/assets/4d269480-c506-4c2a-9634-4c91c2e45452" />

## 1978 port
- RemoteMouse 3.008 - Arbitrary Remote Command Execution
  - https://www.exploit-db.com/exploits/46697
  - https://github.com/p0dalirius/RemoteMouse-3.008-Exploit
- 先上傳 nc.exe，再利用 nc.exe 取得 shell
  - <img width="1918" height="780" alt="image" src="https://github.com/user-attachments/assets/0e75340e-4766-4a27-97af-716b6a8c23e5" />
  - <img width="1918" height="645" alt="image" src="https://github.com/user-attachments/assets/cb4eca5b-c8fd-4867-84fe-c225952766d8" />
- 取得 local.txt
  - <img width="862" height="97" alt="image" src="https://github.com/user-attachments/assets/99dfe951-9c0a-4dcf-86dd-16f9ae0342b6" />

## 提權
- 利用 find 指令找到 divine 的密碼
  ```
  findstr /SIM /C:"pass" *.ini *.cfg *.xml
  ```
  - <img width="1918" height="571" alt="image" src="https://github.com/user-attachments/assets/a22faef6-fee4-48d7-ab14-24a56a5a8eed" />
- 成功解密
  - <img width="1918" height="842" alt="image" src="https://github.com/user-attachments/assets/13ca9d10-2827-4119-8098-1a35ea0b0452" />
- rdp 登入 divine
  - <img width="1918" height="840" alt="image" src="https://github.com/user-attachments/assets/a9a7b76a-1b28-4f36-83de-96539548e804" />
- Remote Mouse GUI 3.008 - Local Privilege Escalation
  - https://www.exploit-db.com/exploits/50047
- 按照步驟成功提權
  - 先開啟服務
    - <img width="1030" height="797" alt="image" src="https://github.com/user-attachments/assets/5eba6ab2-2879-460d-82a0-1f3f7012d5a5" />
  - 點選 setting 再點選 change
    - <img width="1027" height="800" alt="image" src="https://github.com/user-attachments/assets/6e8f6039-b92a-4f5e-8cd8-da375417482c" />
  - 輸入 C:\Windows\System32\cmd.exe 後 enter 就跳出用 system 權限執行的 cmd 
    - <img width="1026" height="790" alt="image" src="https://github.com/user-attachments/assets/b6c71ff8-8221-4470-ba18-618a04d77a38" />
- 取得 proof.txt
  - <img width="1030" height="813" alt="image" src="https://github.com/user-attachments/assets/8700842f-1143-46dc-8dbc-5ca141efd6df" />










































