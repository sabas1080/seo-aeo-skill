# Evaluación inicial: la primera vez en un proyecto

Origen: notas 02, 07, 13, 14, 16, 23 y 26; el orden y los casos sin regla, de una corrida en frío de la skill sobre un
proyecto real sin capa (oct-2026).

Para «evalúa el SEO / la visibilidad en IA de este proyecto», un proyecto nuevo o uno **sin capa**
`seo-aeo-<proyecto>`. Con capa, empezar por lo que ella dice y saltar lo que ya resuelve (paso 1 casi entero).

## 0. Reglas de la corrida

- **Sólo lectura**: consultas de lectura con la conexión de sólo lectura del proyecto (la que su documentación indique;
  si hay dos, la de menos permisos); nada de colectores, migraciones ni envíos.
- **Nada que cueste**: no llamar APIs de pago (proveedores de SEO, LLM) sin el OK del responsable; usar lo ya guardado.
- **Web con mesura**: pocas peticiones al sitio y espaciadas; los firewalls bloquean ráfagas y un 403 propio no dice
  nada del acceso de los bots.

## 1. Inventario de datos

Antes de cualquier cifra, ubicar qué hay. Buscar en la documentación del proyecto (y en su esquema si es una base):

| Pregunta | Fuente típica |
|---|---|
| Tráfico de Google, consultas, CTR, posición | Search Console (export o tabla propia) |
| Sesiones por fuente, referencia de IA | Analítica (GA4 u otra) |
| Ventas por canal | La tienda o una tabla de atribución; la analítica suele ver sólo parte de las compras |
| Posiciones, SERP, AI Overviews, competidores | Proveedor de SEO (DataForSEO, Ahrefs…) |
| Respuestas de IA a prompts propios | Corridas propias contra cada plataforma |
| Menciones en IA a escala (base del proveedor) | Proveedor de SEO/IA |
| Técnico: errores, velocidad, páginas sin enlaces | Rastreo propio o del proveedor |
| Bots de IA reales | Panel de bots del CDN o logs del servidor |

Anotar también las **trampas de lectura** que aparezcan (unidades, ventanas, filas viejas sin grupo, fotos que no se
suman) y lo que **no existe**: eso es la mitad de la capa del proyecto (paso 8).

## 2. Ventanas fijas

Dos, siempre las mismas, dichas en el informe:

- **Últimos 90 días**: el negocio de hoy (qué páginas y canales venden).
- **Últimos 12 meses contra los 12 anteriores** (o el mismo periodo del año anterior): la tendencia. Search Console
  guarda 16 meses; si no hay serie propia más larga, decirlo.

Cortar todas las fuentes en las mismas fechas o declarar el corte de cada una; no dividir datos de ventanas distintas.

## 3. Técnico rápido

Lo mínimo de `auditoria-tecnica.md`, en su orden: acción manual (si hay acceso a Search Console), `robots.txt` con los
bots de IA, una sola versión del sitio (301), una ficha o página clave leída **sin JavaScript**, errores HTTP y páginas
sin enlaces internos si hay rastreo, velocidad móvil si hay medición. El acceso de los bots se confirma en el panel o
los logs; si no hay, es dato faltante.

## 4. Google: demanda o posición

Ante cualquier subida o caída, separar primero:

- **Demanda**: impresiones de la consulta con la posición estable → cambió cuánta gente busca (temporada, un pico que
  pasó, un mercado que se fue). No es un problema técnico ni se arregla en el sitio.
- **Posición**: la posición empeoró con la demanda estable → técnico, competencia o actualización de Google
  (`auditoria-tecnica.md`, «Caídas de tráfico»).

Después, las oportunidades baratas: páginas con **buena posición y CTR bajo** (título y meta primero) y keywords en
posiciones 2-5.

## 5. IA: línea base

- **Por plataforma**, con los tres estados (citado / mencionado / invisible), separando preguntas **con** nuestro nombre
  (¿nos reconoce como entidad?) de las **sin** nombre (¿nos recomienda?).
- Es **una ronda**: línea base, no tendencia. Lo que dependa de la tendencia se pospone a la 2.ª ronda.
- **No mezclar las dos fuentes de IA**: las respuestas a prompts propios y la base de menciones del proveedor miden
  cosas distintas (set propio y chico frente a muestra amplia del proveedor); se reportan por separado.
- Antes de contar una mención, **leer el texto** si el nombre de la marca o del producto es también una palabra común
  o se parece a otra marca.

## 6. Tráfico de IA

Sesiones y ventas con referente de IA, de los 90 días y de los 12 meses. Es un **piso**: buena parte llega sin
referente y cae en «directo» (`medicion.md`). Compararlo con el ~0,25 % típico sólo como orden de magnitud.

## 7. Competidores y brechas

- Clasificar a cada dominio que gana en la SERP o en la IA: **rival** (vende otra cosa para lo mismo), **revendedor o
  distribuidor** (vende nuestro producto), **medio** (lista, reseña, comunidad). Un revendedor citado es una mención
  nuestra que se apoya (su ficha completa y correcta), no alguien a quien ganarle.
- Brechas por tipo (mención, entidad, fuente) y las seis de `auditoria-de-marca.md`, sólo donde haya dato.
- Victorias rápidas: página que ya posiciona y pide actualización, comparativa de terceros donde están todos menos
  nosotros, ficha de revendedor incompleta.

## 8. Cuándo parar y qué entregar

- **Un dato por paso** (3-7) y el antes/después de cualquier caída. Si una pregunta necesita más de unas pocas
  consultas, es dato faltante o trabajo de otra sesión.
- **El informe**, con la forma de `SKILL.md`: veredicto, pasos por prioridad (el «Plan de arranque» de
  `auditoria-de-marca.md` como esqueleto: robots, métricas, 5-10 páginas, brechas, diez objetivos de menciones), una
  tabla de **datos que faltan** y cómo conseguirlos, y la compuerta del responsable una vez. Una página más esa tabla.
- **El borrador de la capa** `seo-aeo-<proyecto>` con lo que costó descubrir: mapa de datos y sus trampas, lo que no se
  puede medir, entidades (y los nombres que chocan), competidores clasificados, calendario de rondas, conexión correcta,
  qué no correr y quién aprueba. Se propone al responsable; no se crea sin su OK.
