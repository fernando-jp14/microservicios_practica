# Blog Service

Microservicio encargado de **publicaciones, autores y categorías**.  
Permite administrar el contenido del blog y se conecta al servicio de autenticación.

## Funcionalidades previstas
- CRUD de posts
- CRUD de categorías
- Asociación de autores con usuarios autenticados
- API REST para listar y filtrar posts

## Dependencias base
- Django REST Framework
- PostgreSQL (base de datos de publicaciones)
- Redis (cacheo de vistas)
- Comunicación con `auth-service` mediante API REST o mensajes Kafka (en fases posteriores)

## Variables de entorno (ejemplo)
```env
POSTGRES_DB=main_db
POSTGRES_USER=devuser
POSTGRES_PASSWORD=devpass
POSTGRES_HOST=postgres