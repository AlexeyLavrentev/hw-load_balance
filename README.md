# Домашнее задание к занятию 2 «Кластеризация и балансировка нагрузки»
## Задание 1
Запустите два simple python сервера на своей виртуальной машине на разных портах
Установите и настройте HAProxy, воспользуйтесь материалами к лекции по ссылке
Настройте балансировку Round-robin на 4 уровне.
На проверку направьте конфигурационный файл haproxy, скриншоты, где видно перенаправление запросов на разные серверы при обращении к HAProxy.

### Выполнение:
- Конфиг haproxy для задания 1: [тут](haproxy.cfg)
- <img width="705" height="884" alt="Screenshot_1" src="https://github.com/user-attachments/assets/5b349458-39f7-4a96-841b-71a760c7cce5" />
- <img width="286" height="144" alt="Screenshot_2" src="https://github.com/user-attachments/assets/8f68f02b-abc9-4fc2-aee5-eca4ff7b3e18" />
- <img width="272" height="150" alt="Screenshot_3" src="https://github.com/user-attachments/assets/69102287-a702-4c51-8070-c56246a401b7" />

## Задание 2
Запустите три simple python сервера на своей виртуальной машине на разных портах
Настройте балансировку Weighted Round Robin на 7 уровне, чтобы первый сервер имел вес 2, второй - 3, а третий - 4
HAproxy должен балансировать только тот http-трафик, который адресован домену example.local
На проверку направьте конфигурационный файл haproxy, скриншоты, где видно перенаправление запросов на разные серверы при обращении к HAProxy c использованием домена example.local и без него.

### Выполнение:

- Исправленный конфиг для доработки haproxy для задания 2: [тут](haproxy_v2.cfg)
- на скриншоте видно ответы от разных серверов при запросе на доменно имя и статус 403 при запросе на ip адрес в терминале 
- <img width="591" height="456" alt="Screenshot_9" src="https://github.com/user-attachments/assets/332ea0af-8304-4331-bbfc-20a4f12bc82b" />
- настройка в файле hosts хостовой машины:
- <img width="269" height="22" alt="Screenshot_7" src="https://github.com/user-attachments/assets/2fc55ffd-e3ed-42b6-b39b-7d1ef07ce24f" /> 
-  запрос на доменное имя через браузер хостовой машины:
- <img width="443" height="125" alt="Screenshot_5" src="https://github.com/user-attachments/assets/ec0b9c54-4e5c-41df-b05c-78550619839a" />
- запрос на ip адрес через браузер хостовой машины:
- <img width="444" height="183" alt="Screenshot_6" src="https://github.com/user-attachments/assets/f6b1c312-3d32-490e-b371-19a1d67e1c33" />
