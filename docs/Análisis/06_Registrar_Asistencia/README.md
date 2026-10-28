# Registrarse (asistencia) mediante QR

**Soporte:** Guía CampusFest p. 1; diagrama del estudiante p. 2; secuencia propuesta.
**Estado de evidencia:** DERIVADO del requisito: QR válido, reserva Confirmada e ingreso único.

## Participantes

- Estudiante (actor).
- InterfazCampusFest (frontera).
- GestiónAsistencia (control).
- Reserva (entidad).
- Asistencia (entidad).

## Relaciones en la colaboración (sin mensajes)

- `Estudiante` — `InterfazCampusFest`
- `InterfazCampusFest` — `GestiónAsistencia`
- `GestiónAsistencia` — `Reserva`
- `GestiónAsistencia` — `Asistencia`

## Mensajes

1. `Estudiante` → `InterfazCampusFest`: Presentar código QR para registrar ingreso.
2. `InterfazCampusFest` → `GestiónAsistencia`: Solicitar validación de ingreso.
3. `GestiónAsistencia` → `Reserva`: Verificar QR y estado Confirmada.
4. `Reserva` → `GestiónAsistencia`: Devolver validez de QR y estado.
5. `GestiónAsistencia` → `Asistencia`: Comprobar que no existe ingreso previo.
6. `Asistencia` → `GestiónAsistencia`: Devolver condición sin ingreso.
7. `GestiónAsistencia` → `Asistencia`: Registrar una sola asistencia con fecha y hora.
8. `Asistencia` → `GestiónAsistencia`: Confirmar asistencia registrada.
9. `GestiónAsistencia` → `InterfazCampusFest`: Devolver confirmación de ingreso.
10. `InterfazCampusFest` → `Estudiante`: Mostrar ingreso registrado.

## Consideraciones

- Solo reserva **Confirmada**, QR válido, y **una asistencia por ingreso**.
- No se añade clase «QR» porque el enunciado no exige modelarla como entidad.

**Archivo editable:** `06_Registrar_Asistencia.drawio` (tres páginas).
