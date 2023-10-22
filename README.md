# observability-learning
1) Подготовлен docker-compose для развертывания Wordpress на базе nginx и mysql, сайт доступен на домене boyanchuk.com
2) Подготовлен docker-compose для поднятия node_exporter, blackbox_exporter, docker_exporter, nginx_exporter, mysql_exporter, cadvisor.
3) blackbox_exporter настроен для проверки сайта boyanchuk.com
4) В компоуз добавлены сервисы prometheus и alertmanager, alertmanager настроен на отправку уведомлений в телеграм канал
5) Для node_exporter и prometheus выпущены ssl сертификаты (self-signed для localhost в node_exporter и let's encrypt для prometheus) и включены tls и аутентификация.
6) Все экспортеры опубликованы в рамках локалхоста для доступа к ним prometheus, prometheus опубликован в интернет и дополнительно проксируется через nginx.

##second homework
Добавлен инстанс victoriametrics с параметром retentionPeriod=14d
В prometheus настроен remote_write

##third homework
настроены алерты с разными severity и для каждого свой receiver в alertmanager
