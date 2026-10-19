# seo-aeo — SEO y visibilidad en IA (AEO)

Skill para agentes (Claude Code y compatibles) que planean, auditan o reportan la visibilidad de una marca en Google y
en las respuestas de IA: ChatGPT, Gemini, Perplexity, Claude, AI Overviews y AI Mode. Es **genérica**: trae el método
y las reglas; lo propio de cada proyecto va en una **capa del proyecto** aparte (ver abajo).

Destilada de videos públicos del canal de Ahrefs en español (https://ahrefs.com/es) y del canal de DataForSEO (en
inglés; proveedor de APIs de datos SEO y de IA: sus demos de producto quedan fuera, su método y sus estudios entran).

## Qué hace y qué no

**Se activa** cuando el agente elige keywords o prompts, escribe un brief de contenido para posicionar o salir citado,
lee datos de SEO o de respuestas de IA, hace una auditoría técnica o de marca, trabaja YouTube, revisa el acceso de
los bots de IA o mide el tráfico que llega desde la IA. Lo decide el `description` de `SKILL.md`.

**Cambia la respuesta** del agente en los casos donde, sin ella, se equivoca: promediar plataformas de IA, leer una
ronda como tendencia, perseguir subconsultas del fan-out, pedir guías de 2.000 palabras «para la IA», vender schema o
`llms.txt` como palanca, etc. Esas reglas son la tabla de `SKILL.md`.

**No hace**:
- No trae datos: no se conecta a Search Console, Ahrefs, DataForSEO ni a ninguna API. Usa los que el proyecto tenga y
  dice cuáles faltan.
- No publica, envía ni cambia nada: propone, y todo pasa por el OK del responsable.
- No sabe nada del proyecto (marca, competidores, tablas, reglas de la casa): eso es la capa del proyecto.

Si en el mismo agente están `ai-seo` o `seo-audit` y dicen otra cosa, manda ésta.

## Instalación

Es una carpeta con `SKILL.md` y `references/`. El nombre de la carpeta debe ser `seo-aeo`.

**En un proyecto, como submódulo de git** (recomendado: todos los agentes del repo usan la misma versión):

```bash
git submodule add https://github.com/sabas1080/seo-aeo-skill.git .claude/skills/seo-aeo
git commit -m "seo-aeo como submódulo"
```

En un clon nuevo del proyecto: `git submodule update --init`.

**Para un solo usuario**, en todos sus proyectos:

```bash
git clone https://github.com/sabas1080/seo-aeo-skill.git ~/.claude/skills/seo-aeo
```

El repo es privado: hace falta acceso de lectura.

**Para otros agentes** (empaquetado propio, plataformas de agentes): copiar `SKILL.md`, `references/` y, si se quiere,
este README. **Dejar fuera `research/` y `.git`**: las notas son el origen de las referencias, no instrucciones.

### Actualizar

```bash
git -C .claude/skills/seo-aeo pull
git add .claude/skills/seo-aeo && git commit -m "seo-aeo X.Y.Z"
```

Y volver a empaquetarla donde se copie a otros agentes. La versión está en `metadata.version` de `SKILL.md`.

**Trampa:** el commit del proyecto puede apuntar a una versión mientras la carpeta tiene otra descargada (pasa tras
un `checkout` dentro del submódulo o al cambiar de rama). Los agentes leen la carpeta, no el puntero. Para revisarlo:

```bash
git submodule status .claude/skills/seo-aeo   # un «+» al inicio = la carpeta no coincide con el puntero
git submodule update .claude/skills/seo-aeo   # la deja en la versión del puntero
```

## Uso

No hace falta invocarla: el agente la carga cuando el encargo cae en su tema. Ejemplos de encargos:

- «¿Qué keywords atacamos este trimestre y con qué página?»
- «Escribe el brief de la guía de X para que la citen ChatGPT y los AI Overviews.»
- «Lee estos resultados de IA de cuatro plataformas y dime cómo vamos frente a los competidores.»
- «Bajó el tráfico orgánico después de la migración, ¿qué revisamos?»
- «¿Los bots de IA pueden leer el sitio?»
- «Queremos vender en Brasil: ¿por dónde empezamos?»

La respuesta sigue siempre la misma forma: veredicto en la primera línea, pasos por prioridad con su porqué, qué dato
falta y cómo conseguirlo, y la compuerta del responsable al final.

## La capa del proyecto (`seo-aeo-<proyecto>`)

Sin capa, la skill funciona, pero el agente no sabe qué datos hay, de quién es la marca ni quién aprueba: lo dirá y
pedirá lo que falte. Con capa, responde con las tablas, entidades y reglas del proyecto.

La capa es **otra skill**, en `.claude/skills/seo-aeo-<proyecto>/`, que se carga junto a ésta. Si chocan: en método
manda `seo-aeo`; en datos y reglas de la casa manda la capa. No va dentro de este repo.

Qué lleva:

| Pieza | Qué contiene |
|---|---|
| Reglas de la casa | Quién aprueba; qué idioma o mercado vende; de dónde salen las afirmaciones sobre productos; dónde se anotan las tareas que salen (nunca en la skill) |
| Entidades y competidores | Marca y variantes, submarcas, productos, marcas personales; los competidores contra los que se compara |
| Mapa de datos | Cada idea de la skill → la tabla, reporte o herramienta que la mide, con sus trampas (unidades, ventanas, fotos que no se suman) |
| Lo que no se puede medir | La lista explícita (backlinks, AI Mode, bots, lo que sea): el agente lo dice en vez de suponer el valor |
| Aplicación por tema (opcional) | Cómo se aplica cada referencia de la skill en el proyecto, con un apartado por archivo de `references/` |

Esqueleto mínimo:

```markdown
---
name: seo-aeo-miempresa
description: Use together with seo-aeo whenever an agent works on MiEmpresa's visibility in Google or in AI answers — maps each seo-aeo idea to our data, lists what cannot be measured today and carries the house rules. Load seo-aeo first; this is its project layer.
---

# seo-aeo-miempresa — la capa de MiEmpresa de `seo-aeo`

En método manda `seo-aeo`; en datos y reglas de la casa manda ésta.

## Reglas de la casa
- Nada se publica, envía ni cambia sin el OK de <responsable>.
- …

## Referencias
| Tarea | Leer |
|---|---|
| Qué mide cada idea y qué NO se puede medir hoy | `references/datos.md` |
| Cómo se aplica cada tema de `seo-aeo` aquí | `references/aplicacion.md` |
```

Mantener en el archivo de datos lo atado a la herramienta (si se cambia de proveedor, sólo se reescribe ése).

## Estructura

- `SKILL.md` — reglas que cambian la respuesta, forma de la respuesta e índice. Corta a propósito.
- `references/` — **por tema, no por video**. Cada archivo cita en su cabecera (`Origen: notas …`) las notas de las
  que sale.
- `research/` — una **nota** por video (paráfrasis, no transcripción) y su índice (`research/README.md`). Es el origen
  de las referencias; no viaja a los agentes.

| Referencia | Notas de origen |
|---|---|
| `busqueda-ia.md` | 01, 04, 05, 06, 29, 30 |
| `keywords-y-prompts.md` | 01, 03, 08, 13, 15, 16, 17, 22, 23, 26, 29 |
| `contenido.md` | 03, 09, 12, 17, 19, 21, 29 |
| `menciones.md` | 01, 03, 10, 14, 15, 19, 20, 25, 29 |
| `youtube.md` | 03, 11, 19 |
| `auditoria-tecnica.md` | 02, 12, 15, 16, 20 |
| `auditoria-de-marca.md` | 07, 14, 25, 31, 32 |
| `medicion.md` | 04, 06, 13, 14, 15, 16, 19, 20, 23, 26, 27, 33 |
| `internacional.md` | 18, 20 |

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
6. En cada proyecto que la usa: actualizar el puntero del submódulo y volver a empaquetarla para sus agentes (ver
   «Actualizar»).

## Pruebas

La skill se probó con agentes sin ella y con ella en tres escenarios: leer resultados de IA de varias plataformas,
escribir un plan de contenido para salir en respuestas de IA, y priorizar keywords con y sin AI Overview. Las fallas
de la línea base son las filas de la tabla de `SKILL.md`.
