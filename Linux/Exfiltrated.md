## nmap scanning
- <img width="1918" height="562" alt="image" src="https://github.com/user-attachments/assets/8d6accdc-4923-461d-82db-5fb2442eb5c2" />

## 80 port
- Subrion CMS
  - <img width="1918" height="831" alt="image" src="https://github.com/user-attachments/assets/1d38c2a1-02d6-472a-947d-bbe7bb4eed81" />
- 版本是 4.2.1
  - <img width="1918" height="832" alt="image" src="https://github.com/user-attachments/assets/ae29f4e8-764f-457b-aada-12708d6ede35" />
- Subrion CMS 4.2.1 - Arbitrary File Upload
  - <img width="1918" height="840" alt="image" src="https://github.com/user-attachments/assets/cf28f1f0-21a5-45b4-a80c-9d6b8fda9d46" />
- 取得 shell
  - <img width="1918" height="826" alt="image" src="https://github.com/user-attachments/assets/7cf7c76d-320f-42c4-ad6a-3e639e42bf4d" />

## 提權
- linpeas.sh 發現可以用 crontab 提權
  - <img width="1628" height="227" alt="image" src="https://github.com/user-attachments/assets/4d970307-cf3c-46c3-b64c-3873bc44a4c8" />
 - /opt/image-exif.sh 發現是利用 exiftool 來提權
   - <img width="1375" height="520" alt="image" src="https://github.com/user-attachments/assets/68e07e04-c6e2-41c9-8749-fc45efb0d427" />
- ExifTool 12.23 - Arbitrary Code Execution
  - https://www.exploit-db.com/exploits/50911
  - https://github.com/UNICORDev/exploit-CVE-2021-22204
- 成功執行 exploit 取得 image.jpg
  - <img width="1918" height="562" alt="image" src="https://github.com/user-attachments/assets/1f750ebc-6e5b-4432-9841-18e870bd670c" />
- 上傳 image.jpg 到靶機 /var/www/html/subrion/uploads，等1分鐘後就成功提權
  - <img width="1918" height="831" alt="image" src="https://github.com/user-attachments/assets/6fcf9fd2-7a68-470f-8293-91b540f2d0fa" />
- 取得 local.txt
  - <img width="853" height="56" alt="image" src="https://github.com/user-attachments/assets/b6878421-8d71-4e22-a537-2bb2365cb026" />
- 取得 proof.txt
  - <img width="638" height="75" alt="image" src="https://github.com/user-attachments/assets/d04a7ac0-89c6-479a-b8f6-d29134ae88b0" />











































