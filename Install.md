
### install
Download latest offline installer from:
https://github.com/goharbor/harbor/releases
```sh
wget https://github.com/goharbor/harbor/releases/download/v2.14.0/harbor-offline-installer-v2.14.0.tgz
tar xf harbor-offline-installer-v2.14.0.tgz
cd harbor
cp harbor.yml.tmpl harbor.yml
vi harbor.yml
./prepare
docker compose up -d
```


harbor.yaml
```yaml
hostname: registry.site.info
http:
  port: 8009
#https:
#
external_url: https://registry.site.info
harbor_admin_password: SET_A_PASSWORD
database:
  password: SET_A_PASSWORD
data_volume: /docker_data/harbor/data
log:
    location: /docker_data/harbor/log
proxy:
  http_proxy: IP:PORT
  https_proxy: IP:PORT
  no_proxy: .quay.io,quay.io,.microsoft.com,127.0.0.1,localhost
```
