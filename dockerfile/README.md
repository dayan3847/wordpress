## Development Environment

```shell
docker pull wordpress:latest
```

```shell
docker build -t "dayan3847/wordpress:dev" ./wordpress_dev
```

```shell
docker build -t "dayan3847/wordpress:test" ./wordpress_dev
```

```shell
docker image rm "dayan3847/wordpress:test"
```

```shell
docker run --rm --user www-data -it dayan3847/wordpress:test sh
```

```shell
docker run --rm --user www-data dayan3847/wordpress:test php --version
```

```shell
docker run --rm --user www-data dayan3847/wordpress:test wp --version
```

```shell
docker run --rm --user www-data dayan3847/wordpress:test composer --version
```
