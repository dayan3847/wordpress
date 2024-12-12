```shell
docker pull mysql
docker pull wordpress
```

````shell
docker compose down -v && docker compose up -d
````

## Clear all

```shell
sudo ls
docker compose down -v
sudo rm -R ./volumes/mysql/data/
sudo rm -R ./volumes/wordpress/wp-content/
docker compose up -d
```
GENERATED ROOT PASSWORD: zWxWqpek/f7mXdKXafVW5r2/112MtsgB

````shell
su www-data -s /bin/bash
````


```shell
sudo chown -R 1000:1000 ./wp
```
