# sec1_hw

### Задание 1

Скачайте и установите виртуальную машину Metasploitable: https://sourceforge.net/projects/metasploitable/.

Это типовая ОС для экспериментов в области информационной безопасности, с которой следует начать при анализе уязвимостей.

Просканируйте эту виртуальную машину, используя **nmap**.

Попробуйте найти уязвимости, которым подвержена эта виртуальная машина.

Сами уязвимости можно поискать на сайте https://www.exploit-db.com/.

Для этого нужно в поиске ввести название сетевой службы, обнаруженной на атакуемой машине, и выбрать подходящие по версии уязвимости.

Ответьте на следующие вопросы:

- Какие сетевые службы в ней разрешены?
- Какие уязвимости были вами обнаружены? (список со ссылками: достаточно трёх уязвимостей)
  
*Приведите ответ в свободной форме.*  

### Решение 1

Вывод nmap со списком открытых портов и запущенных служб тут: https://github.com/valery-dubinin/sec1_hw/blob/main/img/sec1_hw.txt

Уязвимости по базе https://www.exploit-db.com/:

1. vsftpd 2.3.4 - Backdoor Command Execution
2. vsftpd 2.3.4 - Backdoor Command Execution (Metasploit)
3. TelnetD encrypt_keyid - Function Pointer Overwrite
4. BIND 9.4.1 < 9.4.2 - Remote DNS Cache Poisoning (Metasploit)
5. RPCBind / libtirpc - Denial of Service
6. Samba 3.5.0 - Remote Code Execution
7. ProFTPd IAC 1.3.x - Remote Command Execution
8. Xorg X11 Server - Local Privilege Escalation (Metasploit)
9. UnrealIRCd 3.2.8.1 - Backdoor Command Execution (Metasploit)
10. UnrealIRCd 3.2.8.1 - Remote Downloader/Execute
11. Apache Tomcat < 5.5.17 - Remote Directory Listing

### Задание 2

Проведите сканирование Metasploitable в режимах SYN, FIN, Xmas, UDP.

Запишите сеансы сканирования в Wireshark.

Ответьте на следующие вопросы:

- Чем отличаются эти режимы сканирования с точки зрения сетевого трафика?
- Как отвечает сервер?

*Приведите ответ в свободной форме.*

### Решение 2

Режимы сканирования отличаются запросами, посылаемыми сканером. Ниже приведены картинки результатов запросов и поведения обменивающихся ими машин:

SYN - сканирование:

Результат выполнения:

![img](https://github.com/valery-dubinin/sec1_hw/blob/main/img/1.png)

Как работает:

![img](https://github.com/valery-dubinin/sec1_hw/blob/main/img/2.png)

FIN - сканирование (взято из перзентации занятия):

Результат выполнения:

![img](https://github.com/valery-dubinin/sec1_hw/blob/main/img/3.png)

Как работает:

![img](https://github.com/valery-dubinin/sec1_hw/blob/main/img/4.png)

Xmas - сканирование (взято из перзентации занятия):

Результат выполнения:

![img](https://github.com/valery-dubinin/sec1_hw/blob/main/img/5.png)

Как работает:

![img](https://github.com/valery-dubinin/sec1_hw/blob/main/img/6.png)

UDP - сканирование (долго!!):

Результат выполнения:

![img](https://github.com/valery-dubinin/sec1_hw/blob/main/img/7.png)

Как работает:

![img](https://github.com/valery-dubinin/sec1_hw/blob/main/img/8.png)

![img](https://github.com/valery-dubinin/sec1_hw/blob/main/img/9.png)

![img](https://github.com/valery-dubinin/sec1_hw/blob/main/img/10.png)


