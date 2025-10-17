# Email Service

Microservicio dedicado al **envío de correos electrónicos** y **notificaciones**.  
Su función principal es enviar mensajes automáticos (como confirmaciones, restablecimiento de contraseña o formularios de contacto).

## Funcionalidades previstas
- Envío de correos transaccionales
- Procesamiento de colas de mensajes (en Kafka o Redis)
- API REST para contacto

## Dependencias base
- Django
- Librería `smtplib` o `django.core.mail`
- Configuración SMTP externa (por ejemplo, Gmail o Mailtrap)

## Variables de entorno (ejemplo)
```env
EMAIL_HOST=smtp.gmail.com
EMAIL_PORT=587
EMAIL_HOST_USER=tu_correo@gmail.com
EMAIL_HOST_PASSWORD=tu_contraseña