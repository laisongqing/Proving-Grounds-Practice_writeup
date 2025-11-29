## nmap scanning
- <img width="1918" height="620" alt="image" src="https://github.com/user-attachments/assets/3260b92f-235e-4071-9a7d-b90306b6fa03" />

## 8000 port
- Gerapy CMS
  - <img width="1918" height="820" alt="image" src="https://github.com/user-attachments/assets/57a34584-0557-474f-8b41-e54645e14b08" />
- 可以用 admin:admin 登入
  -  <img width="1918" height="840" alt="image" src="https://github.com/user-attachments/assets/95ea1ae7-791e-4880-8998-f3dd001ca081" />
- Gerapy 版本是 v0.9.7
  - <img width="1918" height="837" alt="image" src="https://github.com/user-attachments/assets/5a68ca4c-509b-4672-a982-9225a2673834" />
- Gerapy 0.9.7 - Remote Code Execution (RCE) (Authenticated)
  - https://www.exploit-db.com/exploits/50640
- 要先隨便創一個 project，再跑 python 腳本
  - <img width="1918" height="837" alt="image" src="https://github.com/user-attachments/assets/48434403-736d-4a45-9bd8-7e18df69b637" />
- 成功取得 shell
  - <img width="1918" height="770" alt="image" src="https://github.com/user-attachments/assets/eb91aac1-e70b-46ae-8457-dd782afa46ce" />
- 取得 local.txt
  - <img width="895" height="152" alt="image" src="https://github.com/user-attachments/assets/43bb1477-f838-44ad-90a9-450b87aa6545" />

## 提權
- linpeas.sh 發現 python3.10 可以利用 capabilities 來提權
  - <img width="1602" height="210" alt="image" src="https://github.com/user-attachments/assets/4b5eac15-585d-41cd-8b96-615d0440dd8e" />
- GTFOBins 
  - <img width="1262" height="302" alt="image" src="https://github.com/user-attachments/assets/5585050c-e3a5-44fa-8598-6b04df35f10d" />
- 成功提權
  - <img width="1027" height="157" alt="image" src="https://github.com/user-attachments/assets/00af0812-7753-47c6-a837-68a18510e1aa" />
- 取得 proof.txt
  - <img width="610" height="112" alt="image" src="https://github.com/user-attachments/assets/80f6923e-79d5-4b55-a9cc-1fdf98dee1f4" />

















































