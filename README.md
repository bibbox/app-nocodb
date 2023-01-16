# nocoDB BIBBOX application

nocoDB can be installed as [BIBBOX APP](https://bibbox.readthedocs.io/en/latest/ "BIBBOX App Store") or standalone. 

* initial user/password will be created at first login/signup
* After the installation follow these [instructions](https://github.com/bibbox/app-nocodb/blob/master/INSTALL-APP.md)

## Standalone Installation

Clone the github repository. If necessary change the ports and volume mounts in `docker-compose.yml`.  

```
git clone https://github.com/bibbox/app-nocodb
cd app-nocodb
mkdir data
docker-compose up -d
```

The main app can be opened at 

```
http://localhost:8010
```
