# ДЗ №32 LDAP. Централизованная авторизация и аутентификация
--------------------------------------------------------------------------------------------
### Домашнее задание
```
LDAP
1. Установить FreeIPA;
2. Написать Ansible playbook для конфигурации клиента;
3*. Настроить аутентификацию по ssh-ключам
4**. Firewall должен быть включен на сервере и на клиенте.

В git - результирующий playbook 
```
 - Для запуска стенда клонируем репозиторий в локальное хранилище, переходим в папку репозитория и запускаем стенд - vagrant up

 - После выполнения vagrant up, заходим в /etc/hosts на нашем хостовом ПК и добавляем запись 192.168.50.10 server.test.local.

 - Делается это для того, чтобы можно было перейти по ссылке в веб интерфейс нашего FreeIPA - https://server.test.local/ipa/ui/  (user: admin; password: qwe!23asd) и проверить настройки.

 - Далее необходимо выполнить команду в директории с проектом ```ssh-add id_rsa``` (т.е. добавить сгенерированный закрытый ключ). Чтобы потом его удалить после проверки можно использовать команду ```ssh-add -d id-rsa```

 - В результате на сервер client1.test.local получиться войти без ввода пароля. ```ssh andy@192.168.50.11```
