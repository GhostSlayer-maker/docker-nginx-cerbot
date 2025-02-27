
# Docker nginx y certbot
by Angel

Descargar repositorio
```
git clone https://github.com/GhostSlayer-maker/docker-nginx-cerbot.git
```

Entrar al directorio
```
cd docker-nginx-cerbot
```

Crear certificados de los dominios sin no existen
```
docker-compose run --rm certbot certonly --webroot --webroot-path /data/certbot/certificate -d bstockmanager.com -d test.bstockmanager.com --email angel.belephantit@gmail.com --agree-tos --non-interactive
```

Iniciar servicio en segundo plano
```
docker compose up -d
```

verificar que funciona accediendo a los sitios
```
https://bstockmanager.com https://test.bstockmanager.com
```

revisar los log de nginx paulatinamente
