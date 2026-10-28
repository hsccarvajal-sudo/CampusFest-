# Matriz de trazabilidad y decisiones

| Elemento | Evidencia suministrada | Carácter |
|---|---|---|
| Diagrama de casos de uso Estudiante/Organización | Guía de 6 hojas p. 2 | Transcrito |
| Consulta de cupos — mensajes E→C→B→F→G→D→H→I→A | Guía pp. 4–6 y pizarra | Literal |
| 120 aforo, 83 confirmadas, 12 pendientes, 5 bloqueadas, 7 canceladas históricas | Guía p. 1 | Literal |
| Reserva: PantallaEventos/CalculoDisponibilidad/GestiónReserva/Evento/Reserva | Pizarra «Reservar cupo» y reto 5 | Topología literal; mensajes propuestos |
| Reporte de reservas — pasos 1–11.a/11.b | Pizarra «Reservas» y reto 7 | Texto de mensajes; direcciones de respuestas interpretadas |
| Reporte de asistencia — pasos 1–13.a/13.b | Pizarra «Asistencia» y reto 7 | Texto de mensajes; direcciones de respuestas interpretadas |
| Actor temporal (10 min) interactúa con GestiónReserva | Guía p. 2 y base proporcionada | Literal / regla de clase |
| QR válido, Confirmada e ingreso único | Guía p. 1 | Literal; validación en flujo propuesta |
| Evento: descripción y fecha/hora última edición | Guía p. 1 y reto 6 p. 8 | Literal; mensajes propuestos |
| 27 enlaces de modelo general | PDF exportación Draw.io proporcionada | Reconstrucción exacta de lista original |
| Enlace GestiónAsistencia — Reserva para QR | Requisitos de validación QR | Inferencia coherente, no aparece en original |
| Estereotipos frontera/control/entidad y fucsia | Stephen Schach cap. 13, figs. 13.1 y 13.63 | Referencia gráfica y conceptual |
| Composición Evento–Reserva y Evento–Asistencia | Base suministrada / esquema pizarras | Decisión didáctica; no demostración de ciclo de vida completo |
| Multiplicidades y atributos/métodos conceptuales | Requisitos, más diseño de análisis | Propuestas de modelado |

## Aclaraciones técnicas

- Colaboración y Comunicación son nombres históricamente vinculados en UML. Se entregan páginas separadas porque la tarea explícitamente distingue **sin mensajes** y **con mensajes**.
- El esquema `Actor → Frontera → Control → Entidad` se adopta según la convención de clase proporcionada. El capítulo de Schach por sí solo no establece que toda interacción simple deba contener obligatoriamente una clase control.
- La etiqueta `Cancelar reserva` para el reloj se conserva de la guía de casos de uso; semánticamente el resultado temporal se llama **Vencida**, no Cancelada.
- El documento de CampusFest es un análisis conceptual, **no** un modelo de base de datos ni implementación de software.

## Divergencias terminológicas de los originales

- La guía escribe **CalcularDisponibilidad** y la exportación general escribe **CalculoDisponibilidad**. Ambos se conservan con el nombre de su respectiva fuente.
- La guía asocia al actor **Tiempo** con el caso «Cancelar reserva», pero el requisito define estado **Vencida** tras 10 minutos. Se ofrecen dos escenarios diferentes.
- La secuencia de cancelación manual es una **propuesta**, no está numerada en la guía.
