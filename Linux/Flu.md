## nmap scanning
- <img width="1918" height="848" alt="image" src="https://github.com/user-attachments/assets/30243dc4-50f9-482c-b14b-e682b82251a0" />

## 8090 port
- Atlassian Confluence 7.13.6
  - <img width="1918" height="828" alt="image" src="https://github.com/user-attachments/assets/28313aa5-0ad3-47da-96ed-ede67a18464d" />
- CVE-2022-26134 - Atlassian Confluence OGNL Injection (RCE)
  - https://github.com/Yuri08loveElaina/CVE-2022-26134
  - https://github.com/jbaines-r7/through_the_wire
- 成功取得 shell
  - <img width="1918" height="843" alt="image" src="https://github.com/user-attachments/assets/7c4baa12-f755-4daa-9bde-449ccf133ab3" />
  - <img width="1918" height="286" alt="image" src="https://github.com/user-attachments/assets/d63d5abc-69ce-420c-9fe7-e5db110b2d55" />
- 取得 local.txt
  - <img width="883" height="76" alt="image" src="https://github.com/user-attachments/assets/5cf2ba46-300d-44a7-9a62-35f0390b926a" />

## 提權
- 用 pspy64 發現經過一段時間會用 root 權限去執行 /opt/log-backup.sh
  - <img width="1918" height="802" alt="image" src="https://github.com/user-attachments/assets/5a98930f-2839-4c46-8f1d-8d69f7ee18a5" />
- 發現 /opt/log-backup.sh 可以修改程式碼
  - <img width="1116" height="75" alt="image" src="https://github.com/user-attachments/assets/bc510304-ffed-439c-9d5f-43c8c1104986" />
- 寫 reverse shell 到 /opt/log-backup.sh
  - <img width="1827" height="285" alt="image" src="https://github.com/user-attachments/assets/1449d1e6-61e4-464a-b0ca-92989e82d65a" />
- 成功提權
  - <img width="1167" height="213" alt="image" src="https://github.com/user-attachments/assets/6114c7ad-6cfa-4217-85a7-36b4f3a6e067" />
- 取得 proof.txt
  - <img width="706" height="110" alt="image" src="https://github.com/user-attachments/assets/fc83b2d3-f261-4eb0-b3f9-f10928d458ae" />













































