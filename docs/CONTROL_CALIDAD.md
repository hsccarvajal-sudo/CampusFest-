# Control de calidad — CampusFest (versión corregida)

## Controles efectuados

- Diagramas editables en el archivo consolidado: **37 páginas** (9 casos de uso; cancelación manual y vencimiento automático son dos escenarios del mismo caso).
- Páginas generales: **27 enlaces originales** y **28 enlaces en el refinamiento QR**. El segundo enlace a Reserva es **inferido de requisitos**, no aparece en la exportación inicial.
- Colores de las relaciones: fucsia **#FF00FF**; fondo blanco y actores negros, conforme a los ejemplos gráficos aportados.
- Reorganización de las páginas de comunicación: mensajes en carriles independientes, sin duplicar encima el enlace básico; listas de mensajes fuera de los nodos de reportes.
- El escenario temporal y el de cancelación manual se han separado para evitar participantes sin intervención y distinguir los estados **Vencida** y **Cancelada**.
- Comprobación programática: páginas XML parseables, identificadores únicos, referencias existentes, formas dentro del lienzo y flechas de comunicación que no atraviesan otros participantes.

## Trazabilidad documental

| Elemento | Fuente auténtica | Tratamiento |
|---|---|---|
| Negocio, aforo, estados, QR y hora de modificación | Guía CampusFest 11 hojas, página 1; guía 6 hojas, página 1 | Literal |
| Casos de uso | Guía CampusFest 6 hojas, página 2 | Literal, preservado |
| Consultar cupos, nueve tarjetas E-C-B-F-G-D-H-I-A | Guía 11 hojas, páginas 4-6; pizarra de consulta | Literal |
| Reservar: participantes y enlaces | Pizarra «Reservar cupo»; guía 11 hojas, página 7 | Topología; mensajes derivados |
| Edición de evento y fecha de modificación | Guía 11 hojas, página 8 | Escenario; secuencia derivada |
| Reportes de reservas y asistencias | Pizarra del reto 7; guía 11 hojas, página 9 | Mensajes enumerados; direcciones de algunos retornos interpretadas |
| Categorización entidad/frontera/control | Schach, cap. 13, §13.1, fig. 13.1 | Notación |
| Fucsia y diseño de un modelo integrado | Schach, cap. 13, fig. 13.63 | Referencia visual. Esta figura es un diagrama iterado de clases, **no** una regla de que toda comunicación siga una cadena rígida |
| Original de colaboración general | PDF de exportación Draw.io adjunto | Estructura conservada |

## Advertencias académicas

1. El nombre **CalculoDisponibilidad** se conserva en la exportación original del general; en los diagramas por caso se usa **CalcularDisponibilidad** según la tabla del reto 1. Se refieren a la misma responsabilidad, no a dos clases distintas.
2. La guía asigna al reloj el caso **Cancelar reserva**, pero define **Vencida** como estado que resulta por agotarse diez minutos. Para conservar ambas evidencias hay dos escenarios.
3. La diagramación sin estereotipos (atributos/métodos) incorpora propuestas explícitas; no se afirma que la guía contenga esos métodos.
4. La comprobación geométrica y previsualización independiente no equivalen a una inspección nativa en la aplicación Draw.io. Se debe abrir el archivo para verificar las formas y las fuentes tipográficas del sistema.
