# CDC Demos

## Canal Demo

```bash
cd canal
docker-compose up -d
```

## Debezium Demo

```bash
cd debezium
docker-compose up -d
curl -i -X POST -H "Accept:application/json" -H "Content-Type:application/json" http://localhost:8083/connectors/ -d @connect.json
```

## Comparison Between Debezium And Canal

|  | Debezium | Canal |
|  ----  | ----  | ---- |
| Open Source | Y https://github.com/debezium/debezium | Y https://github.com/alibaba/canal |
| Language | Java | Java |
| Website | https://debezium.io/ | NA |
| Sponsor Company | RedHat | Alibaba |
| License | Apache 2.0 | Apache 2.0 |
| Initial Date | Mar 18, 2016 | Sep 23, 2014 |
| Latest Stable Version | v0.9.5.Final (May 2, 2019) | v1.1.3 (Apr 4, 2019) |
| Support Database | MySQL, MongoDB, PostgreSQL Preview: Oracle, SQL Server | MySQL |
| Support Aurora | Y | Not Mention |
| Support Kafka as Broker | Y | Y |
| Message Serialize | Protobuf https://github.com/blueapron/kafka-connect-protobuf-converter | Protobuf https://github.com/alibaba/canal/tree/master/protocol |
| Performance | TPS 174k/sec (pg with a protobuf converter) https://gitter.im/debezium/dev?at=5a2a6de4ba39a53f1a360424 | TPS 60w ~ 200w (binlog only) https://github.com/alibaba/canal/wiki/Performance |
| Monitor | JMX https://debezium.io/docs/monitoring/ Prometheus Metrics https://github.com/prometheus/jmx_exporter | Prometheus Metrics https://github.com/alibaba/canal/wiki/Prometheus-QuickStart |
