# n8n Docker compose setup

Starts n8n with MongoDB as database and directs traffic through Nginx
for authentication.

## Setup

Replace "example.com" in `data/nginx/app.conf` with correct domain

Set correct values in `docker-compose.yml` for:
 - N8N_BASIC_AUTH_USER
 - N8N_BASIC_AUTH_PASSWORD
 - N8N_HOST
 - VUE_APP_URL_BASE_API
 - GENERIC_TIMEZONE

Adjust email and domain in `init-letsencrypt.sh`

Make sure that the folder `/data/n8n` exists.

To create initial SSH certificate execute first:

```
./init-letsencrypt.sh
```


## Start

To start n8n simply start the docker-compose by executing the following
command in the current folder.

```
docker-compose up -d
```

It can be stopped with:

```
docker-compose stop
```