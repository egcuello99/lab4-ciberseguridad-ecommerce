# Análisis de Amenazas y Riesgos  
Este documento identifica las amenazas principales para los activos críticos de la empresa de comercio electrónico, su probabilidad, impacto y plan de mitigación.

| Amenaza / Vulnerabilidad        | Activo afectado             | Probabilidad (1-5) | Impacto (1-5) | Riesgo (P×I) | Medidas de mitigación recomendadas                                      |
|---------------------------------|-----------------------------|-------------------|--------------|------------|-------------------------------------------------------------------------|
| Robo de datos o fuga de información | Base de datos de clientes    | 4 | 5 | 20 | **Cifrado AES**, control estricto de accesos, monitoreo continuo de logs, pruebas de penetración. |
| Ataque DDoS                     | Servidor web / aplicación   | 3 | 4 | 12 | Uso de **CDN**, balanceador de carga, reglas de limitación de tasa y WAF. |
| Inyección SQL                   | Servidor web / aplicación   | 3 | 5 | 15 | Consultas parametrizadas, validación de entradas, escaneo de vulnerabilidades. |
| Fraude o intercepción de transacciones | Pasarela/servicio de pago | 3 | 5 | 15 | Protocolo **HTTPS/TLS**, autenticación fuerte, monitoreo de transacciones. |
| Eliminación o cifrado de backups (ransomware) | Sistema de backups         | 3 | 5 | 15 | Backups offline y en la nube con versionado, verificación y pruebas de restauración. |
| Acceso no autorizado al panel administrativo | Panel administrativo       | 4 | 4 | 16 | Autenticación multifactor, contraseñas robustas, revisión de roles y permisos. |
| Phishing / robo de credenciales | Credenciales y claves API   | 4 | 4 | 16 | MFA, rotación periódica de claves, capacitación a usuarios, filtrado de correos maliciosos. |
| Compromiso de red o equipos     | Red y equipos de comunicación | 3 | 4 | 12 | Firewall bien configurado, VPN segura, segmentación de red, actualizaciones periódicas. |

> **Escala de evaluación:**  
> - **Probabilidad (P):** 1 (Muy baja) a 5 (Muy alta)  
> - **Impacto (I):** 1 (Leve) a 5 (Crítico)  
> - **Riesgo = P × I**. Se considera **alto** todo valor ≥12.
