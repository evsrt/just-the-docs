---
layout: default
title: astra linux
has_children: false
permalink: /docs/kb/linux/astra
parent: linux
grand_parent: kb
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

# Уровни защищенности операционной системы 
[Уровни защищенности операционной системы](https://wiki.astralinux.ru/pages/viewpage.action?pageId=153485983#AstraLinuxSpecialEdition(%D0%BE%D1%87%D0%B5%D1%80%D0%B5%D0%B4%D0%BD%D0%BE%D0%B5%D0%BE%D0%B1%D0%BD%D0%BE%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5x.7):%D0%9A%D0%BB%D1%8E%D1%87%D0%B5%D0%B2%D1%8B%D0%B5%D0%B8%D0%B7%D0%BC%D0%B5%D0%BD%D0%B5%D0%BD%D0%B8%D1%8F%D0%B2%D0%BA%D0%BE%D0%BC%D0%BF%D0%BB%D0%B5%D0%BA%D1%81%D0%B5%D1%81%D1%80%D0%B5%D0%B4%D1%81%D1%82%D0%B2%D0%B7%D0%B0%D1%89%D0%B8%D1%82%D1%8B%D0%B8%D0%BD%D1%84%D0%BE%D1%80%D0%BC%D0%B0%D1%86%D0%B8%D0%B8-%D0%A3%D1%80%D0%BE%D0%B2%D0%BD%D0%B8%D0%B7%D0%B0%D1%89%D0%B8%D1%89%D0%B5%D0%BD%D0%BD%D0%BE%D1%81%D1%82%D0%B8%D0%BE%D0%BF%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D0%BE%D0%BD%D0%BD%D0%BE%D0%B9%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D1%8B)

# Red Book: Astra Linux Special Edition (очередное обновление x.7)
Настройка безопасной конфигурации компьютера для работы с ОС Astra Linux

<https://wiki.astralinux.ru/pages/viewpage.action?pageId=153486034>

# Инструменты командной строки astra-safepolicy
Управление блокировкой

<https://wiki.astralinux.ru/pages/viewpage.action?pageId=109020865>

# Изменение МКЦ для пользователя
```bash
sudo pdpl-user -i 63 username
```
# Проверить функционирование МКЦ на файловой системе
```bash
sudo set-fs-ilev -v
```
# Средства управления мандатными ПРД в режиме командной строки
## pdpl-user
Управление допустимыми мандатными уровнями (МУ) и мандатными категориями (МК) пользователей ОС
```bash
pdpl-user
```
## pdp-init-fs
Скрипт инициализации мандатных атрибутов ФС
```bash
pdp-init-fs
```
## pdp-ls
Вывод информации о файлах с отображением МА
```bash
pdp-ls
```
## pdpl-ps
Управление мандатными атрибутами процессов
```bash
pdpl-ps
```
## pdp-id
Отображение мандатных атрибутов сессии пользователя
```bash
pdp-id
```
## sumac
Запуск процесса с заданными МУ и категорией
```bash
sumac
```
## userlev
Изменение БД МУ
```bash
userlev --help
```
## usercat
Изменение БД МК
```bash
usercat
```
