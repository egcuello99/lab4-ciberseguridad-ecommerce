# Plan de Contención de Incidentes

Este documento describe las acciones inmediatas para controlar y minimizar el impacto de un incidente de ciberseguridad en la empresa de comercio electrónico.

## Objetivo
Reducir el alcance del incidente, evitar daños mayores y preservar la evidencia necesaria para el análisis forense.

## Pasos de Contención

| Paso | Acción                                                                 | Responsable / Equipo          | Tiempo estimado |
|------|------------------------------------------------------------------------|-------------------------------|-----------------|
| 1    | **Identificar el incidente**: confirmar alcance y sistemas afectados.   | Líder de Incidentes + Especialista TI | Inmediato |
| 2    | **Aislar sistemas comprometidos**: desconectar de la red o mover a VLAN aislada. | Especialista TI / Redes      | <30 min |
| 3    | **Cambiar credenciales críticas y rotar claves API** para evitar accesos posteriores. | Equipo de TI / Seguridad     | 1 hora |
| 4    | **Bloquear tráfico malicioso** en firewall/WAF (IPs, puertos, dominios).| Especialista TI / Redes      | Inmediato |
| 5    | **Preservar evidencia**: respaldar logs, capturas de memoria y estado del sistema para análisis forense. | Analista Forense            | Durante todo el proceso |
| 6    | **Notificar a las partes internas**: líder, gerencia, equipo de comunicaciones. | Líder de Incidentes         | Inmediato |
| 7    | **Comunicación externa (si aplica)**: clientes, proveedores, autoridades. | Responsable de Comunicaciones / Legal | Según necesidad |
| 8    | **Evaluar continuidad del negocio**: decidir si servicios críticos se ponen en modo solo lectura o se suspenden temporalmente. | Gerencia / Líder de Incidentes | Según gravedad |

## Consideraciones
- Mantener un registro detallado de cada acción, hora y responsable.
- Asegurar que los backups más recientes estén intactos antes de cualquier restauración.
- Coordinar con el Plan de Recuperación una vez el incidente esté bajo control.

