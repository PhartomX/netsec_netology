Домашнее задание к занятию "`Защита сети`" - `Алексей Сидоров`
---

### Задание 1.

Задание 1
Проведите разведку системы и определите, какие сетевые службы запущены на защищаемой системе:

sudo nmap -sA < ip-адрес >

sudo nmap -sT < ip-адрес >

sudo nmap -sS < ip-адрес >

sudo nmap -sV < ip-адрес >

 Адрес сканируемого хоста - 10.0.2.4

Запускаем Suricata на сетевом интерфейсе enp0s3:

```
sudo suricata -c /etc/suricata/suricata.yaml -i enp0s3
```

Запускаем сканирование со стороны Kali-Linux и смотрим результат в логах Suricata:
```
sudo tail -f /var/log/suricata/fast.log
```

 - sudo nmap -sA 10.0.2.4

![img1](https://github.com/PhartomX/netsec_netology/blob/main/img/img1.png)
![img2](https://github.com/PhartomX/netsec_netology/blob/main/img/img2.png)

 - sudo nmap -sT 10.0.2.4

![img3](https://github.com/PhartomX/netsec_netology/blob/main/img/img3.png)
![img4](https://github.com/PhartomX/netsec_netology/blob/main/img/img4.png)

 - sudo nmap -sS 10.0.2.4

![img5](https://github.com/PhartomX/netsec_netology/blob/main/img/img5.png)
![img6](https://github.com/PhartomX/netsec_netology/blob/main/img/img6.png)

 - sudo nmap -sV 10.0.2.4

![img7](https://github.com/PhartomX/netsec_netology/blob/main/img/img7.png)
![img8](https://github.com/PhartomX/netsec_netology/blob/main/img/img8.png)


### Задание 2.
           
Проведите атаку на подбор пароля для службы SSH:

hydra -L users.txt -P pass.txt < ip-адрес > ssh