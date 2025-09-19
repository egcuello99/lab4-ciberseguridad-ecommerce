# Procedimientos de Detección de Incidentes

Este documento describe las fuentes de información, las reglas de monitoreo y el proceso para identificar incidentes de ciberseguridad en la empresa de comercio electrónico.

## Fuentes de Monitoreo
- **Logs del servidor web (Nginx/Apache):** registros de accesos, errores y patrones de ataque.
- **Logs de la aplicación / API:** excepciones, intentos de inyección SQL, actividad sospechosa de usuarios.
- **Logs de la base de datos:** consultas anómalas, accesos fuera de horario.
- **Firewall/WAF:** intentos de intrusión, tráfico inusual o picos de conexiones.
- **Pasarela de pagos:** alertas de fraude o transacciones sospechosas.
- **Monitoreo de integridad de archivos:** cambios inesperados en archivos críticos.

## Reglas y Umbrales de Alerta

| Regla de Detección                                      | Fuente                 | Descripción / Riesgo                              | Acción de Alerta                                    |
|---------------------------------------------------------|------------------------|---------------------------------------------------|-----------------------------------------------------|
| Más de 10 intentos de inicio de sesión fallidos en 5 min| Logs de aplicación     | Posible ataque de fuerza bruta                    | Alerta crítica y bloqueo temporal de la IP          |
| Más de 100 errores 5xx en 1 minuto                      | Servidor web          | Posible DDoS o falla grave                        | Alerta alta a equipo de TI                          |
| Consultas SQL con patrones anómalos                     | Base de datos         | Posible inyección SQL                              | Alerta inmediata y registro de la query             |
| Tráfico saliente inusualmente alto                      | Firewall/WAF          | Posible exfiltración de datos                      | Notificación crítica y aislamiento del host         |
| Cambio inesperado en archivos de sistema                | Monitoreo de integridad| Posible malware o ransomware                       | Alerta crítica y verificación forense               |

## Procedimiento de Detección
1. **Monitoreo continuo:** las herramientas de logging envían registros en tiempo real al sistema de monitoreo/SIEM.
2. **Generación de alerta:** cuando se cumple alguna regla, se dispara una notificación automática al correo o sistema de tickets del Equipo de Respuesta a Incidentes.
3. **Escalamiento:** el Líder del equipo evalúa la alerta y decide si se activa el plan de contención.
4. **Registro:** cada alerta se documenta con fecha, hora, fuente, descripción y acción tomada.

## Pruebas y Verificación
- Simular varios intentos de inicio de sesión fallidos para confirmar el disparo de la alerta.
- Ejecutar consultas SQL maliciosas en entorno de pruebas para validar la detección.
- Revisar los logs y comprobar que las alertas lleguen al canal designado.

