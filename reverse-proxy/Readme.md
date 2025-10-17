# Reverse Proxy

Servicio encargado de enrutar las peticiones HTTP hacia los microservicios correspondientes.  
Permite que todo el sistema sea accesible bajo un único dominio o puerto.

## Funcionalidades previstas
- Redirección de tráfico (`/api/auth`, `/api/blog`, `/api/email`, etc.)
- Balanceo de carga (en fases más avanzadas)
- Manejo de HTTPS y cabeceras CORS

## Dependencias base
- Nginx (imagen oficial de Docker)
- Archivos de configuración personalizados en `/etc/nginx/conf.d/`

## Ejemplo de configuración (`default.conf`)
```nginx
server {
    listen 80;

    location /api/auth/ {
        proxy_pass http://auth-service:8000/;
    }

    location /api/blog/ {
        proxy_pass http://blog-service:8000/;
    }

    location /api/email/ {
        proxy_pass http://email-service:8000/;
    }

    location / {
        proxy_pass http://frontend:3000/;
    }
}