# Gestionar un evento (editar descripción)

**Soporte:** Guía CampusFest p. 8, reto 6; fecha/hora modificadas (p. 1); secuencia propuesta.
**Estado de evidencia:** DERIVADO del reto 6 y de la regla de clase: Organizador → Pantalla → GestiónEvento → Evento.

## Participantes

- Organizador (actor).
- PantallaEventoOrganizador (frontera).
- GestiónEvento (control).
- Evento (entidad).

## Relaciones en la colaboración (sin mensajes)

- `Organizador` — `PantallaEventoOrganizador`
- `PantallaEventoOrganizador` — `GestiónEvento`
- `GestiónEvento` — `Evento`

## Mensajes

1. `Organizador` → `PantallaEventoOrganizador`: Modificar descripción del concierto.
2. `PantallaEventoOrganizador` → `GestiónEvento`: Solicitar actualización del evento.
3. `GestiónEvento` → `Evento`: Guardar nueva descripción y fecha/hora de última modificación.
4. `Evento` → `GestiónEvento`: Devolver actualización realizada.
5. `GestiónEvento` → `PantallaEventoOrganizador`: Notificar que fue actualizado.
6. `PantallaEventoOrganizador` → `Organizador`: Mostrar confirmación de edición.

## Consideraciones

- Toda actualización cambia la fecha/hora de la última modificación.
- En el reto 6, el uso de GestiónEvento es una decisión explícita del enfoque de clase; el enunciado dice que no hay otras validaciones.

**Archivo editable:** `07_Gestionar_Evento.drawio` (tres páginas).
