# Generar reporte de reservas

**Soporte:** Pizarra «Reservas», reto 7; guía 11 hojas, p. 9. Mensajes fieles al texto suministrado.
**Estado de evidencia:** MENSAJES 1–11.a/11.b de la pizarra (algunas direcciones de retorno reconstruidas).

## Participantes

- Organizador (actor).
- PantallaEventos (frontera).
- GestiónReserva (control).
- Evento (entidad).
- Reserva (entidad).
- ReporteReservas (frontera).

## Relaciones en la colaboración (sin mensajes)

- `Organizador` — `PantallaEventos`
- `PantallaEventos` — `GestiónReserva`
- `GestiónReserva` — `Evento`
- `GestiónReserva` — `Reserva`
- `GestiónReserva` — `ReporteReservas`
- `ReporteReservas` — `Organizador`

## Mensajes

1. `Organizador` → `PantallaEventos`: Organizador selecciona evento.
2. `PantallaEventos` → `GestiónReserva`: Solicitar lista de reservas.
3. `GestiónReserva` → `Evento`: Solicitar información del evento.
4. `Evento` → `GestiónReserva`: Devolver información del evento.
5. `GestiónReserva` → `Reserva`: Solicitar información de Reserva.
6. `Reserva` → `GestiónReserva`: Devolver información de Reserva.
7. `GestiónReserva` → `GestiónReserva`: Calcular listado de reservas (operación interna).
8. `GestiónReserva` → `ReporteReservas`: Generar reporte de reservas.
9. `ReporteReservas` → `GestiónReserva`: Notificar «Reporte generado».
10. `GestiónReserva` → `PantallaEventos`: Notificar «Reporte generado».
11.a. `PantallaEventos` → `Organizador`: Mostrar «OK».
11.b. `ReporteReservas` → `Organizador`: Entregar reporte de reservas.

## Consideraciones

- El informe es una frontera de salida, no entidad persistente.
- Los últimos pasos con sufijos `.a` y `.b` siguen la notación de la pizarra; no deben confundirse con dos números consecutivos.

**Archivo editable:** `08_Reporte_Reservas.drawio` (tres páginas).
