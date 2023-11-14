# qianli.chat TLS Proxy

To run a qianli.chat TLS proxy, you only need the following steps :

1. Get a host server that has ports 80 and 443 available and a domain name that points to the host.
1. Install docker and docker-compose (`apt update && apt install docker docker-compose`)
1. Ensure your current user has access to docker (`adduser $USER docker`)
1. Clone this repository
1. `./init-certificate.sh`
1. `docker-compose up --detach`

Your proxy is now running! You can share your domain with qianli.chat users.

## Updating from a previous version

If you've previously run a proxy, please update to the most recent version by pulling the most recent changes from `main`, then restarting your Docker containers:

```shell
git pull
docker-compose down
docker-compose up --detach
```
