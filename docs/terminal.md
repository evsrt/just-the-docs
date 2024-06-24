---
layout: default
title: terminal
parent: kb
has_toc: true
---
<details close markdown="block">
  <summary>
    Содержание
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>
# netstat
<https://en.wikipedia.org/wiki/Netstat>
  
```
    -a: Показывает все активные подключения и прослушивающие порты.
    -t: Показывает только TCP подключения и порты.
    -u: Показывает только UDP подключения и порты.
    -n: Выводит адреса и порты в числовом формате, а не в виде имен.
    -l: в состоянии LISTEN
    -p: Показывает имя программы или процесса, связанного с каждым подключением.
    -r: Показывает таблицу маршрутизации.
    -s: Показывает статистику по протоколам.
    -c: Показывает результаты через регулярные интервалы времени.
    -e: Выводит расширенную информацию, такую как UID и PID.
    -g: Показывает групповые политики.
    -i: Показывает информацию об интерфейсах.
    -W: Показывает широкие выводы, позволяя увидеть длинные имена и адреса без усечения.
```
 - Часто используемые ключи
```
sudo netstat -tunlp
```
# lsof
<https://en.wikipedia.org/wiki/Lsof>

Команда lsof -iTCP -sTCP:LISTEN -n -P выводит список всех открытых файлов (List Open Files) в системе, фильтруя результаты по сокетам TCP, и показывает только прослушиваемые (LISTEN) соединения. Расшифровка опций в команде:

    -iTCP: Фильтрация результатов для сокетов TCP.
    -sTCP:LISTEN: Показывает только прослушиваемые (LISTEN) соединения.
    -n: Показывает числовые адреса вместо их разрешения в имена.
    -P: Отключает разрешение портов на имена (выводит числовые значения портов).
 - Пример
```bash
sudo lsof -iTCP -sTCP:LISTEN -n -P
```

 - Вывод:
```bash
COMMAND      PID   USER   FD   TYPE    DEVICE SIZE/OFF NODE NAME
sshd         964   root    3u  IPv4     25055      0t0  TCP *:22 (LISTEN)
sshd         964   root    4u  IPv6     25057      0t0  TCP *:22 (LISTEN)
```
В этом примере видно, что процесс с именем "sshd" слушает порт 22 (SSH) на всех интерфейсах.

# dig
<https://en.wikipedia.org/wiki/Dig_(command)>

## Узнать свой публичный адрес
Google DNS Service
IPv4
```
dig -4 TXT +short o-o.myaddr.l.google.com @ns1.google.com
```
IPv6
```
dig -6 TXT +short o-o.myaddr.l.google.com @ns1.google.com
```
Cloudflare DNS Service
```
dig TXT CH +short whoami.cloudflare @1.0.0.1
```

OpenDNS Service
```
dig +short myip.opendns.com @resolver1.opendns.com
```
- Пример
```
dig +short myip.opendns.com @resolver1.opendns.com
77.77.7.7
```
