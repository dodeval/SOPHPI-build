1. если CONFIG\_BUILDROOT\_FS=y, то порядок следующий:
   1.1 cd buildroot
   1.2 make menuconfig
   1.3 make savedefconfig
   1.4 build\_all



2\. Для отладка

&nbsp;  2.1 # Запускаем с выводом в файл /var/log/messages и логом в кольцевой буфер (shm)

&nbsp;	syslogd -O /var/log/messages -S

&nbsp;  2.2  # Проверяем, что файл создался

&nbsp;	touch /var/log/messages

&nbsp;  2.3 export CVI\_LOG\_LEVEL=7

&nbsp;      export CVI\_DBG\_LEVEL=7

&nbsp;  2.4 grep -i "VI-" /var/log/messages | tail -n 20



