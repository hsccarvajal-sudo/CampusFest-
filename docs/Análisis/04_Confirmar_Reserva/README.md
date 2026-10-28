# Confirmar reserva

**Soporte:** Guía 11 hojas pp. 1 y 7; interacciones propuestas a partir de los estados.
**Estado de evidencia:** DERIVADO del estado Pendiente, la confirmación antes de 10 minutos y el reto 5.

## Participantes

- Estudiante (actor).
- PantallaEventos (frontera).
- GestiónReserva (control).
- Reserva (entidad).

## Relaciones en la colaboración (sin mensajes)

- `Estudiante` — `PantallaEventos`
- `PantallaEventos` — `GestiónReserva`
- `GestiónReserva` — `Reserva`

## Mensajes

1. `Estudiante` → `PantallaEventos`: Solicitar confirmación de reserva.
2. `PantallaEventos` → `GestiónReserva`: Solicitar validación y confirmación.
3. `GestiónReserva` → `Reserva`: Verificar que esté Pendiente y vigente.
4. `Reserva` → `GestiónReserva`: Devolver estado y tiempo de creación.
5. `GestiónReserva` → `Reserva`: Cambiar estado a Confirmada si está vigente.
6. `Reserva` → `GestiónReserva`: Devolver estado Confirmada.
7. `GestiónReserva` → `PantallaEventos`: Notificar confirmación.
8. `PantallaEventos` → `Estudiante`: Mostrar confirmación.

## Consideraciones


**Archivo editable:** `04_Confirmar_Reserva.drawio` (tres páginas).
