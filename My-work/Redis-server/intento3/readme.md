# Redis server

Servidores de redis creados a travez de docker

Al hacer

```bash
docker-compose -f redis_server.yaml up
```

Levantara dos contenedores

- redis:6379 (Persistencia)
- redis-commander:8081 (UI)

---

Para agregar tu configuracion y aun ser capaz de conectarte en redis.conf
busca

```bash
 bind 127.0.0.1
```

y cambiala por

```bash
 bind redis
```
