# Auth Service

Microservicio responsable de la **autenticación de usuarios** y la gestión de **tokens JWT**.

## Funcionalidades previstas
- Registro de usuarios
- Inicio de sesión (login)
- Renovación de tokens (refresh)
- Recuperación y cambio de contraseña
- Exposición de API REST para el frontend

## Dependencias base
- Django REST Framework
- djangorestframework-simplejwt
- PostgreSQL (para almacenar usuarios)
- Redis (para manejo de sesiones y cacheo)

## Variables de entorno (ejemplo)
```env
POSTGRES_DB=main_db
POSTGRES_USER=devuser
POSTGRES_PASSWORD=devpass
POSTGRES_HOST=postgres
REDIS_HOST=redis
