PostgresSQL を docker で起動
```
docker run -d -p 5432:5432 --env-file=env_list.txt --name postgres postgres:latest
```

node を docker で起動
```
docker run -it --rm -e POSTGRES_HOST=host.docker.internal -e POSTGRES_PORT=5432 -v ${PWD}:/usr/app node:latest /bin/bash
```

環境変数を設定
```
export POSTGRES_HOST=host.docker.internal
export POSTGRES_PORT=5432
```
