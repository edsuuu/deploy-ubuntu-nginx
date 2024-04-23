
# Configuracão Nginx 

```bash
sudo apt install nginx -y && sudo systemctl start nginx
```
- Verificar se o NGINX está funcionando

```bash
sudo systemctl status nginx
```

- Ou

```bash
curl 127.0.0.1
```

###
### Veriricar o IP da maquina para ver se ja está renderizando "Welcome to NGINX"
###

```bash
cd /etc/nginx/sites-enabled/ && sudo rm -rf default
```

- Gerar um novo arquivo para substituir o default

```bash
sudo nano seudominio.com.br
```
- Colar o script de sua preferencia 
- Alterar os arquivos antes de colar trocar "seudominio.com.br" para o seu dominio de preferencia

1. [Nginx HTTP](nginx-HTTP.md)
 
- Para HTTPS gerar os certificado SSL antes

2. [Nginx HTTPS](nginx-HTTPS.md)

```bash
sudo nano seudominio.com.br
```
-
```bash
sudo nginx -t && sudo systemctl restart nginx 
```
2. [Certificado SSL](certificado_ssl.md)

