## nocoDB Installation Instructions 

### Start nocoDB

In the first time login you can generate the super admin.

### Test the e-mail configuration


configuration of the email parameters can be tricky. if you need to test several configuration you can just edit the docker-compose.yml file, and restart the App. Finnaly this worked with mailjet. 

```
      NC_SMTP_FROM: test@bibbox.org
      NC_SMTP_HOST: in-v3.mailjet.com
      NC_SMTP_IGNORE_TLS: 'false'
      NC_SMTP_PASSWORD: ************************************
      NC_SMTP_PORT: 587
      NC_SMTP_SECURE: 'false'
      NC_SMTP_USERNAME: ************************************
```

