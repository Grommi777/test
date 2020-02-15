Playbooks launch stages

1. Проверка доступности удалённых хостов эхо-запросом для ansible
   ping.yml

2. Отключение firewalld
   firewalld_disable.yml
   
3. Отключение SElinux
   selinux_disable.yml
   
4. Рестарт после отключения SElinux
   reboot.yml
   
5. Инсталяция и запуск docker
   docker_install.yml

6. Инсталяция и запуск jenkins
   jenkins_install.yml
   
7. Т.к. тестовый запуск docker выполнен с правами root,
   устанавливаем доступ на чтение/запись для jenkins на сокет docker.sock
   chmod.yml

-------------------------------------------------------------------------

Файл pipeline для Jenkins'а: pipeline-script/jenkins_pipeline.txt

Итогом выполнения python скрипта будет создание файла test.txt,
содержащего текст "Hello World!" внутри контейнера python-script.
