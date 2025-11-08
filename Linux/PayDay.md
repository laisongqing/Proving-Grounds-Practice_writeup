## nmap scanning
- <img width="1918" height="703" alt="image" src="https://github.com/user-attachments/assets/017103a0-06e1-4905-ab8e-5076dad7ff2b" />
- <img width="1918" height="767" alt="image" src="https://github.com/user-attachments/assets/751c8df6-339f-4426-b277-aa346a3fe480" />

## 80 port
- dirsearch
  - <img width="1918" height="762" alt="image" src="https://github.com/user-attachments/assets/1e1f4a93-f2ec-4ae5-9bc1-93da3f5f3aaa" />
  - <img width="1918" height="760" alt="image" src="https://github.com/user-attachments/assets/31087665-d96e-43fa-b4b8-03b606454d2a" />
  - <img width="1918" height="715" alt="image" src="https://github.com/user-attachments/assets/ca76bf69-c1ac-469c-9441-6bb4dbc33045" />
- /admin 是 administrator 登入頁面，
  - <img width="1918" height="835" alt="image" src="https://github.com/user-attachments/assets/e4c03031-71e4-4b2a-a44a-3cb9e597ce09" />
  - 用 admin:admin 成功登入
    - <img width="1918" height="857" alt="image" src="https://github.com/user-attachments/assets/de350aa9-74b6-438f-9cf4-09f3b6aafd83" />
- 發現 cs-cart 的版本為 1.3.3
  - <img width="1918" height="850" alt="image" src="https://github.com/user-attachments/assets/f7218f9b-3c55-4444-9061-f4e174781972" />
- CS-Cart 1.3.3 - authenticated RCE
  - https://www.exploit-db.com/exploits/48891
- 在右邊點選 Template editor 上傳 shell.phtml
  - <img width="1918" height="865" alt="image" src="https://github.com/user-attachments/assets/73757a28-b16b-4769-8492-2dd6836430df" />
- 訪問 http://192.168.165.39/skins/ 點選 shell.phtml 成功取得 shell
  - <img width="1918" height="630" alt="image" src="https://github.com/user-attachments/assets/2c01abf0-e5a1-44b2-946d-89f869bd81d3" />

## 提權
- /home 底下有個 user 為 patrick，並用 patrick:patrick 成功登入
  - <img width="1288" height="172" alt="image" src="https://github.com/user-attachments/assets/aadcd58b-bf1d-4adb-a8a0-5b12dd2ffbdf" />
- 發現 patrick 可以 sudo 執行任何指令取得 root
  - <img width="1012" height="337" alt="image" src="https://github.com/user-attachments/assets/98271ac7-0e0e-42dc-8983-26344b3ed8f9" />
- sudo su 成功提權
  - <img width="990" height="126" alt="image" src="https://github.com/user-attachments/assets/268b407d-cf09-4f56-a769-9760388def73" />
- 取得 local.txt
  - <img width="947" height="75" alt="image" src="https://github.com/user-attachments/assets/47441fdb-8048-4727-84ac-39c4a216150a" />
- 取得 proof.txt
  - <img width="872" height="80" alt="image" src="https://github.com/user-attachments/assets/c01d6e05-b7a9-4ca3-a53f-6b33a4f8194b" />















































