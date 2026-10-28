# Consultar eventos

**Soporte:** Guía CampusFest, p. 2; desglose de interacción propuesto (no aparece numerado en pizarras).
**Estado de evidencia:** DERIVADO de la página 2 (caso incluido) y de las responsabilidades de Evento.

## Participantes

- Estudiante (actor).
- InterfazCampusFest (frontera).
- GestiónEvento (control).
- Evento (entidad).

## Relaciones en la colaboración (sin mensajes)

- `Estudiante` — `InterfazCampusFest`
- `InterfazCampusFest` — `GestiónEvento`
- `GestiónEvento` — `Evento`

## Mensajes

1. `Estudiante` → `InterfazCampusFest`: Solicitar consulta de eventos.
2. `InterfazCampusFest` → `GestiónEvento`: Solicitar listado de eventos.
3. `GestiónEvento` → `Evento`: Consultar información de eventos.
4. `Evento` → `GestiónEvento`: Devolver información de eventos.
5. `GestiónEvento` → `InterfazCampusFest`: Devolver listado de eventos.
6. `InterfazCampusFest` → `Estudiante`: Mostrar eventos disponibles.

## Consideraciones


**Archivo editable:** `01_Consultar_Eventos.drawio` (tres páginas).
