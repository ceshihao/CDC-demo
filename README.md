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