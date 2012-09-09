--- 
layout: post 
title: Migrate MySQL Database to a New Server 
author: hrafn 
published: true 
date: 2009-06-08T17:01:41+0400 
permalink: /2009/06/migrate-mysql-database-to-a-new-server
tags:
- tips
- database
--- 

Опять-таки огромная благодарность сайту[ shell -fu](http://www.shell-fu.org/lister.php?id=766)

Следующая команда скопирует базу данных `old_db` с локального хоста в `new_db`
на указанном удаленном хосте:

		mysqldump --add-drop-table --extended-insert --force \
		--log-error=err.log -u[user] -p[pass] old_db | ssh -C user@host "mysql -u[user] -p[pass] new_db"

