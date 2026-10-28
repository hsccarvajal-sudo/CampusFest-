# Generar reporte de asistencia

**Soporte:** Pizarra «Asistencia», reto 7; guía 11 hojas, p. 9. Mensajes fieles al texto suministrado.
**Estado de evidencia:** MENSAJES 1–13.a/13.b de la pizarra (algunas direcciones de retorno reconstruidas).

## Participantes

- Organizador (actor).
- PantallaEventoOrganizador (frontera).
- GestiónAsistencia (control).
- Evento (entidad).
- Asistencia (entidad).
- Estudiante (entidad).
- ReporteAsistencias (frontera).

## Relaciones en la colaboración (sin mensajes)

- `Organizador` — `PantallaEventoOrganizador`
- `PantallaEventoOrganizador` — `GestiónAsistencia`
- `GestiónAsistencia` — `Evento`
- `GestiónAsistencia` — `Asistencia`
- `GestiónAsistencia` — `Estudiante`
- `GestiónAsistencia` — `ReporteAsistencias`
- `ReporteAsistencias` — `Organizador`

## Mensajes

1. `Organizador` → `PantallaEventoOrganizador`: Organizador selecciona reporte de asistencia de un evento.
2. `PantallaEventoOrganizador` → `GestiónAsistencia`: Solicitar reporte de asistencia de un evento.
3. `GestiónAsistencia` → `Evento`: Solicitar información del evento.
4. `Evento` → `GestiónAsistencia`: Retornar información del evento.
5. `GestiónAsistencia` → `Asistencia`: Solicitar información de la asistencia.
6. `Asistencia` → `GestiónAsistencia`: Retornar información de la asistencia.
7. `GestiónAsistencia` → `Estudiante`: Solicitar información de estudiantes.
8. `Estudiante` → `GestiónAsistencia`: Retornar información de estudiantes.
9. `GestiónAsistencia` → `GestiónAsistencia`: Calcular listado de asistencias (operación interna).
10. `GestiónAsistencia` → `ReporteAsistencias`: Generar reporte de asistencia.
11. `ReporteAsistencias` → `GestiónAsistencia`: Notificar «Reporte generado».
12. `GestiónAsistencia` → `PantallaEventoOrganizador`: Notificar «Reporte generado».
13.a. `PantallaEventoOrganizador` → `Organizador`: Mostrar «OK».
13.b. `ReporteAsistencias` → `Organizador`: Entregar reporte de asistencia.

## Consideraciones

- El informe es una frontera de salida, no entidad persistente.
- Los últimos pasos con sufijos `.a` y `.b` siguen la notación de la pizarra; no deben confundirse con dos números consecutivos.

**Archivo editable:** `09_Reporte_Asistencia.drawio` (tres páginas).
