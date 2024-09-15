# env
```env
EMAIL='example@gmail.com'
HTTP_BASIC_USER='user'
HTTP_BASIC_PWD='$apr1$qtamuxse$XIWAWKgaBUG03ONJNZ3N80'
TRAEFIK_DIR='/mnt/media/traefik'
DOMAINNAME='domain.com' 

GRAFANA_DOMAIN='grafana.domain.com' 
JAEGER_DOMAIN='jaeger.domain.com'
```
## create credentials
you can user a https://wtools.io/generate-htpasswd-online

`HTTP_BASIC_USER='your_username'`

`HTTP_BASIC_PWD='$apr1$qtamuxse$XIWAWKgaBUG03ONJNZ3N80'`


# Prepare folders
create traefikdir 
```sh
mkdir -p /mnt/media/traefik
touch /mnt/media/traefik/acme.json
chmod 600 /mnt/media/traefik/acme.json
```

create  grafana_data
```sh
mkdir ./grafana_data
sudo chmod 777 ./grafana_data
```

create  prometheus_data
```sh
mkdir ./prometheus_data
sudo chmod 777 ./prometheus_data
```

# starting 

```sh
docker compose up -d
```