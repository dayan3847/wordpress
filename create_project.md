```shell
dir="../wp_0"
count=0
while [[ -d $dir ]]; do
  dir="../wp_$((++count))"
done
mkdir $dir
echo "Created directory: $dir"
```

```shell
cp .gitignore $dir
cp docker-compose.yml $dir
mkdir -p $dir/db
cp ./db/.gitignore $dir/db/.gitignore
cp README.md $dir
```
