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

````shell
su www-data -s /bin/bash
````

```shell
sudo chown -R www-data:www-data ./volumes/wordpress/my_plugins/
```

```shell
docker compose exec -it -u www-data wordpress bash
```

```shell
docker compose exec -it -u www-data wordpress wp --info
```

## Install WordPress

```shell
docker compose exec -it -u www-data wordpress wp core install --url="http://localhost/" --title="My New Site" --admin_user="admin" --admin_email="admin@admin.com" --admin_password="admin"
```

## Plugins

### Install WooCommerce

```shell
docker compose exec -it -u www-data wordpress wp plugin install woocommerce --activate
```

### Install JWT Auth

```shell
docker compose exec -it -u www-data wordpress wp plugin install jwt-auth --activate
```

### Activate My Plugin

```shell
docker compose exec -it -u www-data wordpress wp plugin activate my_plugin
```
