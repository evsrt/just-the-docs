---
layout: default
title: terminal
parent: kb
---
{:toc}
# netstat
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