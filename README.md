Плейбук предназначен для автоматизированной установки веб-сервера с wordpress на Ubuntu Server хост Ubuntu 16.04.1 и выше.

Перед запуском плейбука необходимо подготовить удаленный хост. Установить на него Phyton-minimal. Сгенерировать ключи для доступа по SSH без пароля.
$ apt-get update 
$ apt-get install python-minimal

Настройка SSH:
$ sudo apt install openssh-server
$ sudo systemctl enable sshd

Создание SSH ключа:
$ ssh-keygen
$ ssh-copy-id user@remote_host

Проверка подключения по SSH:
$ ssh user@remote_host

Установка WP:
ansible-vault decrypt /etc/ansible/playbook.yml
