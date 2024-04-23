
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

# Verificar o IP da maquina para ver se ja está renderizando "Welcome to NGINX"

```bash
cd /etc/nginx/sites-enabled/ && sudo rm -rf default
```

- Gerar um novo arquivo para substituir o default

```bash
sudo nano seudominio.com.br
```
- Alterar os arquivos antes de colar de "seudominio.com.br" para o seu dominio de preferencia

Configuraçao [Nginx HTTP](nginx-HTTP.md)
 
- Para HTTPS gerar os certificado SSL antes

Certificado [Certificado SSL](certificado_ssl.md)

Configuraçao [Nginx HTTPS](nginx-HTTPS.md) 

```bash
sudo nano seudominio.com.br
```
- Após colar e salvar o script 
```bash
sudo nginx -t && sudo systemctl restart nginx 
```



