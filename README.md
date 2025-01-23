# spring-boot-actuator-docker-prometheus-grafana
spring-boot-actuator-docker-prometheus-grafana

Sample API Produtos 

http://localhost:8082/produtos

http://localhost:8082/produtos/1

Link Actuator + Metrics 

http://localhost:8082/actuator

http://localhost:8082/actuator/health

http://localhost:8082/actuator/metrics/http.server.requests

http://localhost:8082/actuator/metrics/http.client.requests


Para onde o Actuator pode Exportar as métricas

https://docs.spring.io/spring-boot/reference/actuator/metrics.html

https://micrometer.io/

criar  o docker compose 

podman run -d --name prometheus  --network aw-network  -p 9090:9090 -v ./config/prometheus.yml:/etc/prometheus/prometheus.yml -v prometheus_data:/prometheus prom/prometheus:latest

podman run -d --name grafana --network aw-network -p 3000:3000 grafana/grafana:latest

http://localhost:9090/query

localhost:3000

To get gateway
podman network inspect podman 


Em graph buscar por jvm_gc_max_data_size_bytes

Acesso Grafana 

http://localhost:3000/login 

admin
admin 

http://localhost:3000/connections/datasources

Dentro do Grafana criar um novo Data Source com http://10.88.0.1:9090 

depois de OK 

ir em Explorer 

http://localhost:3000/explore?schemaVersion=1&panes=%7B%22bgc%22%3A%7B%22datasource%22%3A%22grafana%22%2C%22queries%22%3A%5B%7B%22queryType%22%3A%22randomWalk%22%2C%22refId%22%3A%22A%22%2C%22datasource%22%3A%7B%22type%22%3A%22datasource%22%2C%22uid%22%3A%22grafana%22%7D%7D%5D%2C%22range%22%3A%7B%22from%22%3A%22now-1h%22%2C%22to%22%3A%22now%22%7D%7D%7D&orgId=1


https://grafana.com/grafana/dashboards/


https://grafana.com/grafana/dashboards/14430-spring-boot-statistics-endpoint-metrics/

Grafana wirth Resilience4J 

https://github.com/resilience4j/resilience4j/blob/master/grafana_dashboard.json