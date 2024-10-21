# PRZ-3_SBOR_LOGOV_Kostomahin
PRZ-3_SBOR_LOGOV
## Выполнил студень группы: ББМО-02-23 

## Костомахин Антон Александрович

Для начала подготовим ОС, которую будем использовать для того, чтобы хостить наше решение.
В данной практики будем рассматривать систему XDR Wazuh.

Я выбрал Ubuntu 22.04 server.
![image](https://github.com/user-attachments/assets/22091023-ef69-47fd-8454-cf082942fbe5)
![image](https://github.com/user-attachments/assets/d334786a-1077-454e-bd8d-9b0d07632a1e)

Далее запустим скрипт установки командой 

curl -sO https://packages.wazuh.com/4.7/wazuh-install.sh && sudo bash ./wazuh-install.sh -a
![image](https://github.com/user-attachments/assets/531dd00f-9965-4ec3-87f5-a4042e7d46b3)

Далее переходим на веб интерфейс Wazuh
![image](https://github.com/user-attachments/assets/bf0ad170-8fdf-4e2c-815f-78c3bcfb87cd)

Теперь необходимо установить агент на ВМ, которые мы хотим мониторить.с Wazuh
![image](https://github.com/user-attachments/assets/a7db7222-f33f-4cb6-932a-35b678db3108)
![image](https://github.com/user-attachments/assets/65257600-e8be-4e1e-b189-7c3e0adc8138)

Делается это очень просто. Переходим во вкладку агенты и выбираем нужную ос, вводим ip сервера и получаем ссылку, которую нужно вставить в консоль.
![image](https://github.com/user-attachments/assets/883421e6-4fdf-4daf-a064-0e6378bf546d)

Далее нам нужно подключить 1 ВМ к Wazuh.
Я выбрал Ubuntu 22.04 

![image](https://github.com/user-attachments/assets/371c609e-8f48-4eac-892c-30fc776f4ea1)

Как видно на нашем сервер теперь доступны 1 машины для мониторинга. 
![image](https://github.com/user-attachments/assets/19f8225b-9d78-495a-b648-827ae1ed218e)

Система имеет встроенный детектор уязвимостей. 
![image](https://github.com/user-attachments/assets/271d71fa-4c87-4099-9184-293be98d4f5f)

Перейдем к моделированию аномальной активности. Для этого буду использовать ВМ на Kali Linux.
![image](https://github.com/user-attachments/assets/522beca9-9da6-4c41-afef-9486e5582da9)

Как мы видим система успешно обнаружила атаку по ssh на клиентской машине.
![image](https://github.com/user-attachments/assets/cd2fe9d3-e95c-4e2e-afc2-2db88dcda6cd)

Фиксация получения данных с клиентской машины.
![image](https://github.com/user-attachments/assets/e95681ee-63e6-4166-b0d5-039d50d641cb)
