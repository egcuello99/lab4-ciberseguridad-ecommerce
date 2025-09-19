# Plan de Recuperación y Continuidad del Negocio

Este documento describe las acciones para restaurar los sistemas de la empresa de comercio electrónico después de un incidente de ciberseguridad, garantizando la continuidad de las operaciones.

## Objetivo
Restaurar los servicios críticos en el menor tiempo posible, asegurando la integridad de los datos y minimizando el impacto en clientes y operaciones.

## Pasos de Recuperación

| Paso | Acción                                                                                      | Responsable / Equipo            | Tiempo Estimado |
|------|---------------------------------------------------------------------------------------------|----------------------------------|-----------------|
| 1    | **Confirmar que el incidente está contenido** antes de iniciar la restauración.              | Líder de Incidentes             | Inmediato |
| 2    | **Verificar la integridad de los backups** (hashes, pruebas de lectura).                     | Equipo de TI / Analista Forense | 30 min |
| 3    | **Restaurar en un entorno de pruebas/sandbox** para validar que el backup es seguro.         | Equipo de TI                    | 1–2 horas |
| 4    | **Aplicar parches y corregir la vulnerabilidad raíz** identificada durante el análisis.      | Especialista TI / Seguridad     | Según necesidad |
| 5    | **Promover a producción** una vez que el entorno de pruebas esté validado.                   | Equipo de TI                    | 1 hora |
| 6    | **Monitorear continuamente** el sistema restaurado para confirmar estabilidad.               | Equipo de Monitoreo             | 24 horas posteriores |
| 7    | **Comunicar a clientes y proveedores** el restablecimiento seguro del servicio.              | Responsable de Comunicaciones   | Según plan |

## Objetivos de Continuidad

- **RTO (Recovery Time Objective):** máximo 4 horas para restablecer servicios esenciales (servidor web, base de datos).
- **RPO (Recovery Point Objective):** máximo 1 hora de pérdida de datos, gracias a respaldos incrementales.

## Post-Incidente
1. **Revisión de causa raíz:** documento detallado con hallazgos y lecciones aprendidas.  
2. **Actualización de planes:** incorporar mejoras en detección, contención y recuperación.  
3. **Capacitación al personal** sobre las nuevas medidas adoptadas.

