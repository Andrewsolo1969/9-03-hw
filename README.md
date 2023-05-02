# Домашнее задание к занятию "9.3 «Система мониторинга Zabbix. Часть 2»" - Соловьёв Андрей SYS-18

При выполнении задания в  использована домашняя машина c Ubuntu 22.04

Zabbix-server установлен на  виртуальную машину 192.168.122.104 

Zabbix-agent установлен на localhost-192.168.122.104, 192.168.122.199 и debian 11 - 192.168.122.53

---

## Задание 1

Создайте свой шаблон, в котором будут элементы данных, мониторящие загрузку CPU и RAM хоста.

### Процесс выполнения

1. Выполняя ДЗ сверяйтесь с процессом отражённым в записи лекции.
2. В веб-интерфейсе Zabbix Servera в разделе Templates создайте новый шаблон
3. Создайте Item который будет собирать информацию об загрузке CPU в процентах
4. Создайте Item который будет собирать информацию об загрузке RAM в процентах

Templates

![Templates](https://github.com/Andrewsolo1969/9-03-hw/blob/main/img/Templates.png)

Элементы данных

Стандартные элементы данных - CPU utilization - system.cpu.util 

![CPU utilization.png](https://github.com/Andrewsolo1969/9-03-hw/blob/main/img/CPU_utilization.png)

Параметры vm.memory.size - (https://www.zabbix.com/documentation/5.2/ru/manual/appendix/items/vm.memory.size_params)
vm.memory.size [pused] - pused - 'used' память в процентах по отношению к 'total' (рассчитывается как used/total*100)

![Memory_used.png](https://github.com/Andrewsolo1969/9-03-hw/blob/main/img/Memory_used.png)


## Задание 2

Создайте свой шаблон, в котором будут элементы данных, мониторящие загрузку CPU и RAM хоста.

Процесс выполнения

1. Выполняя ДЗ сверяйтесь с процессом отражённым в записи лекции.
2. Установите Zabbix Agent на 2 виртмашины, одной из них может быть ваш Zabbix Server

Выполнено в задании 9-02, дополнительно добавлена вирт.машина Debian 11 = 192.168.122.53

3. Добавьте Zabbix Server в список разрешенных серверов ваших Zabbix Agentов
4. Добавьте Zabbix Agentов в раздел Configuration > Hosts вашего Zabbix Servera
5. Прикрепите за каждым хостом шаблон Linux by Zabbix Agent
6. Проверьте что в разделе Latest Data начали появляться данные с добавленных агентов

Zabbix-agent установлен на localhost-192.168.122.104, 192.168.122.199 и debian 11 - 192.168.122.53

![task_2.png](https://github.com/Andrewsolo1969/9-03-hw/blob/main/img/task_2.png)

![104.png](https://github.com/Andrewsolo1969/9-03-hw/blob/main/img/104.png)

![198.png](https://github.com/Andrewsolo1969/9-03-hw/blob/main/img/198.png)

![53.png](https://github.com/Andrewsolo1969/9-03-hw/blob/main/img/53.png)

## Задание 3

Привяжите созданный шаблон к двум хостам. Также привяжите к обоим хостам шаблон Linux by Zabbix Agent.

Процесс выполнения

1. Выполняя ДЗ сверяйтесь с процессом отражённым в записи лекции.
2. Зайдите в настройки каждого хоста и в разделе Templates прикрепите к этому хосту ваш шаблон
3. Так же к каждому хосту привяжите шаблон Linux by Zabbix Agent
4. Проверьте что в раздел Latest Data начали поступать необходимые данные из вашего шаблона

Требования к результату

 Прикрепите в файл README.md скриншот страницы хостов, где будут видны привязки шаблонов с названиями «Задание 2-3». Хосты должны иметь зелёный статус подключения

![Templates_Task_3.png](https://github.com/Andrewsolo1969/9-03-hw/blob/main/img/Templates_Task_3.png)


 ![199_Latest_Date.png](https://github.com/Andrewsolo1969/9-04-hw/blob/main/img/199_Latest_Date.png)

 ![Debian_11_Latast_Date.png](https://github.com/Andrewsolo1969/9-04-hw/blob/main/img/Debian_11_Latast_Date.png)

 ## Задание 4

Создайте свой кастомный дашборд.

1. Выполняя ДЗ сверяйтесь с процессом отражённым в записи лекции.
2. В разделе Dashboards создайте новый дашборд
3. Разместите на нём несколько графиков на ваше усмотрение.

Требования к результату

 Прикрепите в файл README.md скриншот дашборда с названием «Задание 4»

 ![Grafana](https://github.com/Andrewsolo1969/9-04-hw/blob/main/img/Grafana.png)



 