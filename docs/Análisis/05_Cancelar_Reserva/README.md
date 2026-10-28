# Cancelar reserva / vencimiento

**Soporte:** Guía p. 2 (actor Tiempo y Cancelar reserva), p. 1 (estado Vencida); secuencia propuesta.
**Estado de evidencia:** CASO DEL ACTOR TIEMPO: muestra específicamente el vencimiento automático a los 10 minutos; la cancelación manual figura también en la colaboración sin mensajes.

## Participantes

- Estudiante (actor).
- 10 minutos (actor temporal).
- PantallaEventos (frontera).
- GestiónReserva (control).
- Reserva (entidad).

## Relaciones en la colaboración (sin mensajes)

- `Estudiante` — `PantallaEventos`
- `PantallaEventos` — `GestiónReserva`
- `10 minutos` — `GestiónReserva`
- `GestiónReserva` — `Reserva`

## Mensajes

1. `10 minutos` → `GestiónReserva`: Transcurren 10 minutos desde crear la reserva.
2. `GestiónReserva` → `Reserva`: Consultar si la reserva sigue Pendiente.
3. `Reserva` → `GestiónReserva`: Devolver estado Pendiente.
4. `GestiónReserva` → `Reserva`: Cambiar a Vencida y liberar el cupo.
5. `Reserva` → `GestiónReserva`: Confirmar vencimiento y liberación.

## Consideraciones

- La secuencia representa exclusivamente el vencimiento automático originado por el actor Tiempo.
- En el caso manual, Estudiante → PantallaEventos → GestiónReserva → Reserva (Cancelada).
- La guía representa el caso con el nombre «Cancelar reserva» aunque el vencimiento tiene estado **Vencida**, no Cancelada.

**Archivo editable:** `05_Cancelar_Reserva.drawio` (tres páginas).

## Segundo escenario: cancelación manual
El actor **Estudiante** puede iniciar Cancelar reserva; el actor **Tiempo** causa el estado **Vencida**, no **Cancelada**.
Archivo adicional `05b_Cancelacion_Manual.drawio`: tres páginas editables. Mensajes propuestos, no transcritos de la pizarra.
