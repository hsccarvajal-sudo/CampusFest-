# Consultar cupos

**Soporte:** Guía de 6 hojas, retos 2–4, pp. 4–6; pizarras de consulta de cupos.
**Estado de evidencia:** LITERAL: el orden de tarjetas E-C-B-F-G-D-H-I-A está expresamente documentado.

## Participantes

- Estudiante (actor).
- PantallaEventos (frontera).
- CalcularDisponibilidad (control).
- Evento (entidad).
- Reserva (entidad).

## Relaciones en la colaboración (sin mensajes)

- `Estudiante` — `PantallaEventos`
- `PantallaEventos` — `CalcularDisponibilidad`
- `CalcularDisponibilidad` — `Evento`
- `CalcularDisponibilidad` — `Reserva`

## Mensajes

1. E. `Estudiante` → `PantallaEventos`: Seleccionar el evento para consultar cupos.
2. C. `PantallaEventos` → `CalcularDisponibilidad`: Solicitar cálculo de disponibilidad.
3. B. `CalcularDisponibilidad` → `Evento`: Solicitar aforo y cupos bloqueados.
4. F. `Evento` → `CalcularDisponibilidad`: Devolver 120 cupos y 5 bloqueados.
5. G. `CalcularDisponibilidad` → `Reserva`: Solicitar reservas confirmadas y pendientes vigentes.
6. D. `Reserva` → `CalcularDisponibilidad`: Devolver 83 confirmadas y 12 pendientes.
7. H. `CalcularDisponibilidad` → `CalcularDisponibilidad`: Calcular: 120 - 83 - 12 - 5 = 20 (operación interna).
8. I. `CalcularDisponibilidad` → `PantallaEventos`: Devolver el resultado de 20 cupos.
9. A. `PantallaEventos` → `Estudiante`: Mostrar que quedan 20 cupos.

## Consideraciones

- Disponibles = 120 − 83 − 12 − 5 = **20**.
- Las 7 canceladas son historial y **no** se descuentan de nuevo.
- Orden literal de tarjetas: **E → C → B → F → G → D → H → I → A**.

**Archivo editable:** `02_Consultar_Cupos.drawio` (tres páginas).
