# seo-aeo — de dónde sale y cómo se mantiene

Skill de SEO y visibilidad en IA (AEO) destilada de videos públicos del canal de Ahrefs en español
(https://ahrefs.com/es). Es **genérica**: método y reglas. Lo propio de cada proyecto (qué datos tiene, qué no puede
medir, reglas de la casa) va en una skill aparte del proyecto, p. ej. `seo-aeo-<proyecto>`, que se carga junto a ésta.

Cada video tiene una **nota** (paráfrasis, no transcripción) en `research/NN-*.md`. Las notas son el origen de las
referencias, no instrucciones para el agente: al empaquetar la skill para agentes se puede dejar fuera `research/`.

## Estructura

- `SKILL.md` — reglas que cambian la respuesta + índice. Corta a propósito.
- `references/` — **por tema, no por video**. Cada archivo cita en su cabecera (`Origen: notas …`) las notas de las
  que sale.
- `research/` — las notas por video y su índice (`research/README.md`).

| Referencia | Notas de origen |
|---|---|
| `busqueda-ia.md` | 01, 04, 05, 06 |
| `keywords-y-prompts.md` | 01, 03, 08, 13 |
| `contenido.md` | 03, 09, 12 |
| `menciones.md` | 01, 03, 10, 14 |
| `youtube.md` | 03, 11 |
| `auditoria-tecnica.md` | 02, 12 |
| `auditoria-de-marca.md` | 07, 14 |
| `medicion.md` | 04, 06, 13, 14 |

## Cómo añadir un video

1. Transcribirlo y escribir la nota siguiente `research/NN-<slug>.md` con el mismo formato: fuente (URL), ideas
   clave y datos citados, en paráfrasis. Nada de un proyecto concreto: cómo se aplica en cada proyecto va a su capa.
   Sumarla a `research/README.md`.
2. Decidir a qué **temas** toca (normalmente 1-3 referencias). Si no encaja en ninguno, crear una referencia nueva de
   tema y sumarla al índice de `SKILL.md` y a la tabla de arriba.
3. Editar **sólo** esas referencias: integrar lo nuevo en su sección (no pegar un bloque «video NN»), actualizar las
   cifras si el video trae datos más recientes y añadir el número de nota a su línea `Origen:`.
4. Si cambia una regla de la tabla de `SKILL.md` (algo que altera la respuesta de un agente), editarla ahí también.
5. Subir `metadata.version` de `SKILL.md` (menor si sólo se enriquecen referencias; mayor si cambia una regla),
   commit y push.
6. En cada proyecto que la usa (p. ej. como submódulo de git): actualizar el puntero y volver a empaquetarla para sus
   agentes.

## Pruebas

La skill se probó con agentes sin ella y con ella en tres escenarios: leer resultados de IA de varias plataformas,
escribir un plan de contenido para salir en respuestas de IA, y priorizar keywords con y sin AI Overview. Las fallas
de la línea base son las filas de la tabla de `SKILL.md`.
