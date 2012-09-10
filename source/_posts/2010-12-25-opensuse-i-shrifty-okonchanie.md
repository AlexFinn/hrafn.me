---
layout: post
title: openSUSE и шрифты. Окончание
author: hrafn
published: true
date: 2010-12-25T14:01:59+0000
permalink: /2010/12/opensuse-i-shrifty-okonchanie
categories:
- suse
- fonts
---

Что ж, похоже я получил максимум того, чего можно было добиться на данный
момент, без самостоятельного накладывания патчей и пересборки пакетов. Тот,
кто читал мои предыдущие сообщения о разборках со шрифтами, должен знать, что
мне очень полюбились патчи от [infinality.net](http://www.infinality.net/blog/)[ ](infinality.net):)
Поскольку дают максимально комфортный для меня результат. Для openSUSE
доступен пакет freetype именно с этими патчами. Итак, приступим.

<!--more-->

Открываем консоль и пишем от рута:

		# cd /etc/zypp/repos.d
		# wget http://download.opensuse.org/repositories/home:/anshuljain:/infinality/openSUSE_11.3/home:anshuljain:infinality.repo
		# zypper in freetype2-feature-subpixel-hinting

После установки пакетов скачиваем файл local.conf ([http://www.infinality.net/files/local.conf](http://www.infinality.net/files/local.conf)) и помещаем его
в /etc/fonts/. Перегружаемся.

Результат установки пакетов можно видеть ниже. Первый скриншот - шрифты по
умолчанию, второй - после установки пропатченного freetype2.

[![](/media/images/2010/12/25/1.png)](/media/images/2010/12/25/1.png)

[![](/media/images/2010/12/25/2.png)](/media/images/2010/12/25/2.png)

После загрузки поиграйтесь со шрифтами. Ранее использованный мною Droid в
данной случае оказался не самым удачным вариантом. Лучше всех выглядел
Liberation :)

