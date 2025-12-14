## nmap scanning
- <img width="1918" height="728" alt="image" src="https://github.com/user-attachments/assets/ddd1ecac-1bba-4153-b0dd-457b00f6635e" />

## 3000 port
- Gitea
  - <img width="1918" height="845" alt="image" src="https://github.com/user-attachments/assets/fd04c743-7925-446e-8698-2d9c191cda9e" />
- 註冊後登入，發現 Gitea 版本是 1.7.5
  - <img width="1918" height="842" alt="image" src="https://github.com/user-attachments/assets/29429150-46ab-4809-93b3-f32fc0096c62" />
- Gitea 1.7.5 - Remote Code Execution
  - https://www.exploit-db.com/exploits/49383
- msfconsole 成通取得 meterpreter shell
  - <img width="1918" height="742" alt="image" src="https://github.com/user-attachments/assets/068775a4-54e6-4bb6-a0c1-3eb718bd359d" />
- 取得 local.txt
  - <img width="953" height="172" alt="image" src="https://github.com/user-attachments/assets/c72e7721-1b1f-4e18-8bb5-7c236e2cf705" />

## 提權
- crontab 可以提權，/usr/local/bin 有權限可以讀、寫、執行
  - <img width="1235" height="365" alt="image" src="https://github.com/user-attachments/assets/800b3ff2-6608-414a-b1dd-739268d63adf" />

- cat /etc/crontab 發現可以寫 reverse shell 到 run-parts
  - <img width="1437" height="442" alt="image" src="https://github.com/user-attachments/assets/df04e915-09e3-44f5-8667-2dfa69426208" />
  - <img width="1530" height="372" alt="image" src="https://github.com/user-attachments/assets/a5d30e96-51ac-4482-8bea-3778780e03ff" />
- 成功提權
  - <img width="992" height="190" alt="image" src="https://github.com/user-attachments/assets/ba8226aa-7c9c-435e-b92d-f62bb0b39f27" />
- 取得 proof.txt
  - <img width="547" height="91" alt="image" src="https://github.com/user-attachments/assets/ec7c5584-eaf9-490f-bab2-305605a2b787" />

















































