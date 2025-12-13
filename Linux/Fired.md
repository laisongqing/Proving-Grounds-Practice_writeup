## nmap scanning
- <img width="1918" height="668" alt="image" src="https://github.com/user-attachments/assets/abad838a-e6a9-4b63-a8d4-c90f6660e761" />

## 9090 port
- Openfire cms
  - <img width="1918" height="785" alt="image" src="https://github.com/user-attachments/assets/15c36534-50ac-4f2c-b82b-4481b5524773" />
- CVE-2023-32315
  - https://github.com/miko550/CVE-2023-32315
  - <img width="1918" height="430" alt="image" src="https://github.com/user-attachments/assets/68d21b55-7593-4073-b5f3-d672d77d28e3" />
- 成功登入 Openfire
  - <img width="1918" height="835" alt="image" src="https://github.com/user-attachments/assets/f5f67db8-d637-430d-a63f-1a0e308c7a77" />
- Server > Server Settings > Management tool
  - <img width="1918" height="820" alt="image" src="https://github.com/user-attachments/assets/86e82b53-27bd-402e-8833-17dd8ad3a86e" />
- 輸入 123 成功 whoami
  - <img width="1918" height="817" alt="image" src="https://github.com/user-attachments/assets/996521ea-433d-4ea7-a0f5-a16b7f3c6eb5" />
- 上傳 shell.jsp 到 /var/lib/openfire/plugins/admin/webapp/
  - <img width="1918" height="842" alt="image" src="https://github.com/user-attachments/assets/b02b30f8-3f18-4cf7-bcae-8e47c29f7b38" />
- 成功取得 shell
  - <img width="1918" height="842" alt="image" src="https://github.com/user-attachments/assets/5c8eb5b9-252b-4750-8e77-e49f1b7f3352" />
- 取得 local.txt
  - <img width="1918" height="177" alt="image" src="https://github.com/user-attachments/assets/b4ccb289-8ab3-4935-9019-dfa5f1d93888" />

## 提權
- 在 /var/lib/openfire/embedded-db 底下的 openfire.script 檔案發現密碼
  - <img width="1918" height="747" alt="image" src="https://github.com/user-attachments/assets/257f9c16-c243-4465-8823-54fdabfc8547" />

- 用 root:OpenFireAtEveryone 成功提權
  - <img width="1080" height="200" alt="image" src="https://github.com/user-attachments/assets/fec004db-33c6-4587-9b73-6306ffd0ca04" />

- 取得 proof.txt
  - <img width="878" height="117" alt="image" src="https://github.com/user-attachments/assets/b0ef9388-4bbd-4394-9b1c-7de3a5cf9097" />















































