# mephi-session-project-2026

Сессионный проект по курсу "Операционные системы семейства Unix".

## Выполнено

- Установлена Fedora на диск, не Live-режим
- Настроен hostname mephi-2026.domain.local
- Настроена сеть через nmcli
- Установлены nginx, tcpdump, libcap-ng-utils
- Скачан RPM-пакет tcpdump через dnf download
- Создан раздел /dev/sdb1
- Создана файловая система ext4 с меткой MEPHI_DATA
- Настроено монтирование /data/mephi-web через /etc/fstab
- Запущен и включён nginx
- Создан пользователь mephi-admin
- Создана группа mephi-devs
- Настроены права 2775 на /data/mephi-web
- Настроен SELinux-контекст httpd_sys_content_t
- Настроены capabilities для tcpdump
- Запрещён вход root через PAM pam_listfile.so
- Создана web-страница index.html
- Проверена доступность nginx через curl

## Примечание по сети

В задании указан IP 192.168.1.100/24 и шлюз 192.168.1.1.
В фактической сети хостовой машины шлюз был 192.168.0.1, поэтому для рабочей проверки использовался адрес 192.168.0.150/24.

## Проверка

```
curl http://192.168.0.150
```

Ожидаемый результат:

```
Hello from Student: 370551
```
