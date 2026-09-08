# Cleanup

![Stopped service containers leave a PostgreSQL volume intact in one outcome and remove the volume in the other](images/13-cleanup-volume-imagegen.png)

*`docker compose down` removes the services while preserving the volume; adding `-v` removes the persisted database data too.*

Stop and remove all containers:

```bash
docker compose down
```

To also remove the PostgreSQL data volume:

```bash
docker compose down -v
```
