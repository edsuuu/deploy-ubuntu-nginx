
# Configuracão Nginx 


```bash
sudo apt install nginx -y
```
- 
```bash
cd /etc/nginx/sites-enabled/
```
```bash
sudo rm -rf default
```

- Gerar um novo arquivo para substituir o default

```bash
sudo nano seudominio.com.br
```
- Colar o script de sua preferencia 
- Alterar os arquivos antes de colar trocar "seudominio.com.br" para o seu dominio de preferencia

1. [Nginx HTTP](nginx-HTTP.txt)
 
- Para HTTPS gerar os certificado SSL antes

2. [Nginx HTTPS](nginx-HTTPS.txt)

```bash
sudo nano seudominio.com.br
```

```bash
sudo nginx -t
```

```bash
sudo systemctl restart nginx 
```

###
### Gerar Certificado SSL para o seu dominio
###

```bash
sudo openssl dhparam -out /etc/ssl/certs/dhparam.pem 2048
```

```bash
sudo apt-get install certbot -y
```
- Caso não funcione use o alternativo

```bash
sudo snap install certbot --classic
```
#
```bash
sudo service nginx stop
```

```bash
sudo certbot certonly --standalone -d seudominio.com.br
```

```bash
sudo service nginx start
```

- Para renovar caso o certificado expire

```bash
sudo certbot renew
```