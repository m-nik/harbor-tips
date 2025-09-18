
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


