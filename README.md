**Nginx + LetsEncrypt configuration for docker-compose usage**

assume you have already created a certificate 

```
1. sudo ufw allow 80 && sudo ufw allow 443
2. sudo apt install letsencrypt
3. sudo certbot certonly --standalone --agree-tos --preferred-challenges http -d [example.org]
```

***The `certonly` option means that the certificate will only be obtained without installation on any web server, `standalone` allows you to start your own web server for authentication, `agree-tos` means acceptance of the ACME server subscription agreement, which is a prerequisite, and `preferred-challenges http` means performing authorization using HTTP***

Useful links:

LetsEncrypt SSL on Ubuntu [link](https://serverspace.io/support/help/how-to-get-lets-encrypt-ssl-on-ubuntu/?attempt=1)

Nginx + SSL + Docker [link](https://pentacent.medium.com/nginx-and-lets-encrypt-with-docker-in-less-than-5-minutes-b4b8a60d3a71)
