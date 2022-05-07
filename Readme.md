1. Устанавливаем Grafana в соответствии с  https://grafana.com/docs/grafana/latest/installation/
2. Создаем директории New dashboard folder - Infra и App
3. Добавляем Data Source "Prometheus"
4. Импортируем dashboard "Prometheus Blackbox Exporter" https://grafana.com/grafana/dashboards/7587
5. Импортируем dashboard "Node Exporter Full" https://grafana.com/grafana/dashboards/1860


Алертинг:
1. Добавляем Alerting -> Contact Point "Telegram"
2. Заполняем поля токена и chatID
3. создаем правило - Create alert rule - 'probe_success{instance="http://5.188.150.105/index.php", job="blackbox"}'
4. Проверяем, когда probe_success ниже 1