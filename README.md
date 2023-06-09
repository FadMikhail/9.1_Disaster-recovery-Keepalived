# Домашнее задание к занятию 1 «Disaster recovery и Keepalived» Фадеев михаил

### Задание 1
- Дана [схема](1/hsrp_advanced.pkt) для Cisco Packet Tracer, рассматриваемая в лекции.
- На данной схеме уже настроено отслеживание интерфейсов маршрутизаторов Gi0/1 (для нулевой группы)
- Необходимо аналогично настроить отслеживание состояния интерфейсов Gi0/0 (для первой группы).
- Для проверки корректности настройки, разорвите один из кабелей между одним из маршрутизаторов и Switch0 и запустите ping между PC0 и Server0.
- На проверку отправьте получившуюся схему в формате pkt и скриншот, где виден процесс настройки маршрутизатора.

![image](https://github.com/FadMikhail/9.1_Disaster-recovery-Keepalived/assets/132131230/b26dd70c-0f38-4577-bcf7-1a0200d96b85)
![image](https://github.com/FadMikhail/9.1_Disaster-recovery-Keepalived/assets/132131230/939e49b2-b7e8-4b84-a870-64864e90ac97)


------


### Задание 2
- Запустите две виртуальные машины Linux, установите и настройте сервис Keepalived как в лекции, используя пример конфигурационного [файла](1/keepalived-simple.conf).
- Настройте любой веб-сервер (например, nginx или simple python server) на двух виртуальных машинах
- Напишите Bash-скрипт, который будет проверять доступность порта данного веб-сервера и существование файла index.html в root-директории данного веб-сервера.
- Настройте Keepalived так, чтобы он запускал данный скрипт каждые 3 секунды и переносил виртуальный IP на другой сервер, если bash-скрипт завершался с кодом, отличным от нуля (то есть порт веб-сервера был недоступен или отсутствовал index.html). Используйте для этого секцию vrrp_script
- На проверку отправьте получившейся bash-скрипт и конфигурационный файл keepalived, а также скриншот с демонстрацией переезда плавающего ip на другой сервер в случае недоступности порта или файла index.html

![image](https://github.com/FadMikhail/9.1_Disaster-recovery-Keepalived/assets/132131230/8abcd0eb-586e-4b9f-9aa8-bf0181747847)

![image](https://github.com/FadMikhail/9.1_Disaster-recovery-Keepalived/assets/132131230/b70a8dd2-826e-4e48-ac90-27b588d5281d)

![image](https://github.com/FadMikhail/9.1_Disaster-recovery-Keepalived/assets/132131230/e4ba006c-7f33-4891-a3a2-ca6a5410f599)

![image](https://github.com/FadMikhail/9.1_Disaster-recovery-Keepalived/assets/132131230/e07dc94e-3845-4dd0-bb6e-a91902156afe)


------

### Критерии оценки

- Зачет - выполнены все задания, ответы даны в развернутой форме, приложены требуемые скриншоты, конфигурационные файлы, скрипты. В выполненных заданиях нет противоречий и нарушения логики
- На доработку - задание выполнено частично или не выполнено, в логике выполнения заданий есть противоречия, существенные недостатки, приложены не все требуемые материалы.
