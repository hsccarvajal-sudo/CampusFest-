# CampusFest — Ingeniería de Software I

Entrega de análisis orientado a objetos basada en Stephen Schach, capítulo 13, la guía CampusFest de Unillanos y fotografías de las pizarras de clase.

## Organización solicitada por el profesor

```text
CampusFest/
├── README.md
└── docs/
    ├── CdU/
    │   ├── CampusFest_Casos_De_Uso.drawio
    │   └── 01_...md a 09_...md
    ├── Analisis/
    │   ├── 00_Colaboracion_General.drawio
    │   ├── 01_Consultar_Eventos/              [3 diagramas]
    │   ├── 02_Consultar_Cupos/                [3 diagramas]
    │   ├── 03_Reservar/                      [3 diagramas]
    │   ├── 04_Confirmar_Reserva/             [3 diagramas]
    │   ├── 05_Cancelar_Reserva/              [3 diagramas]
    │   ├── 06_Registrar_Asistencia/          [3 diagramas]
    │   ├── 07_Gestionar_Evento/              [3 diagramas]
    │   ├── 08_Reporte_Reservas/              [3 diagramas]
    │   ├── 09_Reporte_Asistencia/            [3 diagramas]
    │   ├── 10_Clases_Entidad/
    │   ├── 11_Estados_Reserva.drawio
    │   └── CampusFest_Todos_Los_Diagramas.drawio
    └── TRAZABILIDAD.md
```

La división **CdU** (casos de uso) y **Analisis** (diagramas de análisis ordenados por caso de uso) replica el encargo escrito en la pizarra.

Cada Draw.io de un caso de uso contiene colaboración (sin mensajes), comunicación (con mensajes) y secuencia. El caso 05 incluye dos escenarios: cancelación manual y vencimiento automático (seis páginas), sin actores sobrantes en las secuencias. El general se conserva sin mensajes. Las clases entidad se muestran con estereotipos y sin ellos (con atributos y métodos).

## Trabajo basado en fuentes

- Los nueve mensajes de consulta de cupos están transcritos del taller.
- Los pasos de ambos reportes se basan en la pizarra.
- Donde no existían mensajes enumerados, las secuencias son reconstrucciones justificadas por las reglas de negocio, señaladas como **propuestas**.
- Los cupos libres del concierto de bienvenida son **20**, no 13: las siete canceladas son solo historial.

Consulte `docs/TRAZABILIDAD.md` para diferenciar evidencias de inferencias.

## Abrir los diagramas

1. Ir a https://app.diagrams.net/.
2. Archivo → Abrir desde → Dispositivo.
3. Seleccionar cualquier archivo `.drawio` (el consolidado permite ver todas las páginas).

## Publicar en GitHub (pendiente de acción personal)

1. Cree desde GitHub un repositorio **CampusFest**, vacío.
2. Abra una terminal dentro de esta carpeta `CampusFest`.
3. Ejecute:

```bash
git init
git add .
git commit -m "Entrega de análisis OO CampusFest — Schach capítulo 13"
git branch -M main
git remote add origin https://github.com/TU_USUARIO/CampusFest.git
git push -u origin main
```

Reemplace `TU_USUARIO` por su usuario real y configure su autenticación de GitHub. Esta entrega **no ha sido publicada** en la cuenta del usuario.

## Limitación de fuente

Las páginas de UML con atributos/métodos contienen propuestas mínimas de análisis; la guía no define una interfaz de métodos completa. No se añaden bases de datos, APIs, framework, clases técnicas o diagramas de implementación.
