# nocodb BIBBOX application

This container can be installed as [BIBBOX APP](https://bibbox.readthedocs.io/en/latest/ "BIBBOX App Store") or standalone. 

After the docker installation follow these [instructions](INSTALL-APP.md).

Initial user/password will be created at first login/signup.

## Standalone Installation 

Clone the github repository. If necessary change the ports in the environment file `.env` and the volume mounts in `docker-compose.yml`.

```
git clone https://github.com/bibbox/app-nocodb
cd app-nocodb
docker network create bibbox-default-network
docker-compose up -d
```

The main App can be opened and set up at:
```
http://localhost:8010
```

## Install within BIBBOX

Visit the BIBBOX page and find the App by its name in the store. Click on the symbol and select install. Then fill the parameters below and name your App, click install again.

## Docker Images used
  - [nocodb/nocodb](https://hub.docker.com/r/nocodb/nocodb) 
  - [adminer](https://hub.docker.com/r/adminer) 
  - [postgres](https://hub.docker.com/r/postgres) 


 
## Install Environment Variables
  - POSTGRES_DATABASE_USER = The User of the postgres DB created for NOCODB
  - POSTGRES_DATABASE_PASSWORD = The Password of the postgres DB created for NOCODB
  - NC_SMTP_FROM = Email sender address
  - NC_SMTP_HOST = SMTP host value
  - NC_SMTP_PORT = SMTP port
  - NC_SMTP_USERNAME = SMTP username for authentication
  - NC_SMTP_PASSWORD = SMTP password for authentication
  - NC_SMTP_SECURE = To enable secure set  as true any other value treated as false
  - NC_SMTP_IGNORE_TLS = To ignore tls set  as true any other value treated as false.

  
The default values for the standalone installation are:
  - POSTGRES_DATABASE_USER = admin
  - POSTGRES_DATABASE_PASSWORD = changethispasswordinproductionenvironments
  - NC_SMTP_FROM = master@bibbox.org
  - NC_SMTP_HOST = smtp.your-smtp-host.org
  - NC_SMTP_PORT = 587
  - NC_SMTP_USERNAME = master@bibbox.org
  - NC_SMTP_PASSWORD = changethissmtppasswordinproductionenvironments
  - NC_SMTP_SECURE = true
  - NC_SMTP_IGNORE_TLS = true

  
## Mounted Volumes
### nocodb/nocodb Container
  - *./data/nocodb/data:/usr/app/data*
### postgres Container
  - *./data/pgsql/data:/var/lib/postgresql/data*

