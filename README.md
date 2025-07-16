# Домашнее задание к занятию "`«Кластеризация и балансировка нагрузки»`" - `Лоскутов Вячеслав`


## Задание 1:
### >Запустите два simple python сервера на своей виртуальной машине на разных портах
### >Установите и настройте HAProxy, воспользуйтесь материалами к лекции по ссылке
### >Настройте балансировку Round-robin на 4 уровне.
### >На проверку направьте конфигурационный файл haproxy, скриншоты, где видно перенаправление запросов на разные серверы при обращении к HAProxy.

## Ответ:
### Установил и запустил на виртуальной машине 2 python сервера:
![python](https://github.com/NightWalkerZ488/balancing-loskutovvv/blob/main/pythonservers1.PNG)

### Настроил конфигурационный файл ![haproxy.cfg](https://github.com/NightWalkerZ488/balancing-loskutovvv/blob/main/haproxy.cfg)

### Проверил работу балансировки:
![balancing](https://github.com/NightWalkerZ488/balancing-loskutovvv/blob/main/haproxlevel4.PNG)


## Задание 2:

### >Запустите три simple python сервера на своей виртуальной машине на разных портах
### >Настройте балансировку Weighted Round Robin на 7 уровне, чтобы первый сервер имел вес 2, второй - 3, а третий - 4
### >HAproxy должен балансировать только тот http-трафик, который адресован домену example.local
### >На проверку направьте конфигурационный файл haproxy, скриншоты, где видно перенаправление запросов на разные серверы при обращении к HAProxy c использованием домена example.local и без него.

## Ответ:
Запуск 3-х python серверов на разных портах:
![3py](https://github.com/NightWalkerZ488/balancing-loskutovvv/blob/main/3python.PNG)
Настройка веса и адреса example.local в ![конфигурационном файле](https://github.com/NightWalkerZ488/balancing-loskutovvv/blob/main/haproxy2.cfg)
Тест получившихся настроек: без указания example.local ответа нет, с указнием работает механизм round robin с весами.
![noanswer](https://github.com/NightWalkerZ488/balancing-loskutovvv/blob/main/norobin.PNG)
![roundrobin](https://github.com/NightWalkerZ488/balancing-loskutovvv/blob/main/robinround.PNG)
