## nmap scanning
- <img width="1622" height="510" alt="image" src="https://github.com/user-attachments/assets/38975ff3-049b-4e24-aaf2-b3baf4628b29" />

## 80 port
- 是一個 PE-files upload file 的網頁
  - <img width="1918" height="655" alt="image" src="https://github.com/user-attachments/assets/92c74393-2c30-49df-8c39-c201b51f7d75" />
- dirsearch
  - <img width="1918" height="677" alt="image" src="https://github.com/user-attachments/assets/ffb19aae-de10-4b36-b1b7-80ada70787d2" />
- /backups 有個 zip 檔案
  - <img width="1918" height="482" alt="image" src="https://github.com/user-attachments/assets/6d8aada2-5ae5-4c25-a3cb-1af2f2b59e21" />
- 解壓縮後發現 upload.php 會檢查上傳的檔案開頭有沒有 4D 5A (magic bytes)
  - <img width="987" height="780" alt="image" src="https://github.com/user-attachments/assets/fd456f18-1c10-4fd5-bf12-22a9aa6cd3da" />
- 上傳 shell.php
  - <img width="1062" height="157" alt="image" src="https://github.com/user-attachments/assets/1e69d485-e3f3-4b2c-861f-7b86bac88cc5" />
- 成功上傳
  - <img width="1532" height="783" alt="image" src="https://github.com/user-attachments/assets/e79178ae-4d15-442b-987d-fcee5a0cf1ca" />
- 取得 shell
  - <img width="1918" height="827" alt="image" src="https://github.com/user-attachments/assets/df4d413d-096e-4354-8990-d5f11220bfd6" />
- 取得 local.txt
  - <img width="1157" height="150" alt="image" src="https://github.com/user-attachments/assets/6ccf8ee5-a45f-49c7-95b7-76065528bf75" />

## 提權
- linpeas.sh 發現 /opt/fileS 存在 SUID 提權
  - <img width="1918" height="505" alt="image" src="https://github.com/user-attachments/assets/af8f7db1-5016-499c-b4bd-9ab52093125d" />
- /opt/fileS --help 發現指令跟 find 一模一樣
  - <img width="1912" height="765" alt="image" src="https://github.com/user-attachments/assets/910496d9-e2cf-4f0d-a7ae-7f0a93bdf312" />
  - <img width="1918" height="738" alt="image" src="https://github.com/user-attachments/assets/a715387b-4ed8-49e0-ac94-1bcc53893cee" />
- GTFOBins 
  - <img width="1433" height="370" alt="image" src="https://github.com/user-attachments/assets/87764013-48ab-4e5c-abe7-91d55ac21cfd" />
- 成功提權
  - <img width="1053" height="127" alt="image" src="https://github.com/user-attachments/assets/5298f5b4-e5d6-4265-acf9-99ce9eeab5b3" />
- 取得 proof.txt
  - <img width="635" height="173" alt="image" src="https://github.com/user-attachments/assets/8f4f70b6-2f2c-4f69-9d21-647186176bc9" />













































