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
