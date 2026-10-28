# Reservar cupo

**Soporte:** Pizarra «Reservar Cupo», guía pp. 1 y 7; mensajes propuestos (no numerados por el docente).
**Estado de evidencia:** TOPOLOGÍA LITERAL de la pizarra «Reservar cupo»; el detalle de mensajes es DERIVADO de las reglas.

## Participantes

- Estudiante (actor).
- PantallaEventos (frontera).
- CalcularDisponibilidad (control).
- GestiónReserva (control).
- Evento (entidad).
- Reserva (entidad).

## Relaciones en la colaboración (sin mensajes)

- `Estudiante` — `PantallaEventos`
- `PantallaEventos` — `CalcularDisponibilidad`
- `PantallaEventos` — `GestiónReserva`
- `CalcularDisponibilidad` — `Evento`
- `CalcularDisponibilidad` — `Reserva`
- `GestiónReserva` — `Reserva`

## Mensajes

1. `Estudiante` → `PantallaEventos`: Seleccionar evento y solicitar reserva.
2. `PantallaEventos` → `CalcularDisponibilidad`: Solicitar disponibilidad del evento.
3. `CalcularDisponibilidad` → `Evento`: Consultar aforo y bloqueados.
4. `Evento` → `CalcularDisponibilidad`: Devolver aforo y bloqueados.
5. `CalcularDisponibilidad` → `Reserva`: Consultar reservas que ocupan cupos.
6. `Reserva` → `CalcularDisponibilidad`: Devolver reservas vigentes.
7. `CalcularDisponibilidad` → `PantallaEventos`: Indicar si existen cupos disponibles.
8. `PantallaEventos` → `GestiónReserva`: Solicitar creación de reserva.
9. `GestiónReserva` → `Reserva`: Crear reserva Pendiente con vencimiento de 10 minutos.
10. `Reserva` → `GestiónReserva`: Devolver identificación y estado Pendiente.
11. `GestiónReserva` → `PantallaEventos`: Devolver reserva creada.
12. `PantallaEventos` → `Estudiante`: Mostrar reserva Pendiente y plazo de 10 minutos.

## Consideraciones

- Una reserva nueva queda en **Pendiente** y ocupa cupo provisional por hasta 10 minutos.
- No debe crearse si excede aforo. La confirmación es otro caso de uso.

**Archivo editable:** `03_Reservar.drawio` (tres páginas).
