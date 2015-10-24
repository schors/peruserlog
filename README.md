Программа парсинга логов сервисов и раскладывания их пользователям
==================================================================

Программа представляет собой демона написанного на языке Perl. Основная цель - дать
пользователям shared-хостинга возможность иметь доступ к логам основных сервисов, относящихся
к этим пользователям. Таким сервисам как ssh, ftp, почта от скриптов, cron.

Возможности
-----------

* Чтение журналов OpenSSH, ProFTPD, sendmail, Vixie cron
* Раскладывание по каталогам пользователя строк, имеющих к этому пользователю отношение
* Дублирование попользовательских журналов в отдельном хранилище
* Переоткрытие логов пользователя по SIGHUP, что позволяет использовать стандартные программы ротации логов

Особенности
-----------

Для работы с OpenSSH в конфигурации /etc/ssh/sshd_config должна быть опция:
LogLevel DEBUG

Использование
-------------

Данная программа благополучно используется на хостинге http://diphost.ru

TODO
----

* Сделать проверку на существование файла - и не вываливаться, и не забить этим лог
* Сделать чтение authorized_keys более корректным, чтобы не сделали "бомбу"

--
[![LICENSE WTFPL](wtfpl-badge-1.png)](LICENSE)

