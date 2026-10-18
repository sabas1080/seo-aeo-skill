---
name: seo-aeo
description: Use when an agent plans, audits, briefs or reports on a brand's visibility in Google search or in AI answers (ChatGPT, Gemini, Perplexity, Claude, Google AI Overviews or AI Mode) — choosing keywords or prompts, briefing content meant to rank or be cited, reading SEO or AI-answer data, brand-gap or mention audits, YouTube SEO, crawlability for AI bots, or AI referral traffic. Complements ai-seo and seo-audit and wins when they disagree.
metadata:
  version: 2.6.0
---

# seo-aeo — SEO y visibilidad en IA

Destilada de los videos de Ahrefs en español (curso de AEO y afines) y de DataForSEO (en inglés, sobre medición de
la visibilidad en IA). El SEO es la base del AEO: lo que posiciona en
Google alimenta a la IA, pero la IA cita por probabilidad, por plataforma y sobre todo por **menciones de marca en
sitios de otros**. Esta skill propone y mide; **nada se publica, envía ni cambia en el sitio sin el OK del responsable**.

**Capa del proyecto:** si existe una skill `seo-aeo-<proyecto>` (por ejemplo `seo-aeo-miempresa`), cárgala: dice qué
tabla mide cada cosa, qué no se puede medir y las reglas de la casa. Si `ai-seo` o `seo-audit` dicen otra cosa,
manda esta skill.

## Reglas que cambian la respuesta

| Situación | Lo correcto |
|---|---|
| Resultados de IA de varias plataformas | Reportar **cada plataforma por separado** (solo ~14 % de fuentes en común); nunca un promedio entre plataformas |
| Una pregunta o una ronda cambió | Es una **muestra**, no una tendencia: las citas son probabilísticas y las de AI Overviews cambian cada ~2 días. Tendencia = varias rondas, agregado por grupo de prompts |
| «Nos menciona pero no nos enlaza» | Usar los tres estados (citado / mencionado / invisible) y comparar con la tasa de enlace normal de la plataforma (AI Overviews ~11 %, ChatGPT ~27 %, Perplexity ~52 %) antes de llamarlo problema |
| El AI Overview cita una reseña de YouTube o un hilo de Reddit de terceros sobre nuestro producto | Es lo esperable en Google y una **mención valiosa**: apoyarla y multiplicarla, no «reemplazarla» con la ficha |
| Keyword con AI Overview que resuelve la duda | El objetivo es la **mención**, no el clic. Sin AI Overview y con intención de compra: objetivo clic con la **ficha** primero |
| «best X», «X vs Y», «alternative» | Entrar en las **listas y comparativas de terceros** que la IA cita (~44 % de lo citado); la comparativa propia complementa. El volumen ~0 de una A vs B no la descarta |
| «best X» cuando el sitio es un medio, blog o afiliado (no vende el producto) | Su lista **es** la lista de terceros que la IA cita: hacerla la mejor de la SERP (pruebas propias, datos, frescura). Shopping no aplica |
| Brief de contenido | Sin meta de palabras (la longitud no correlaciona con la cita). Respuesta primero (BLUF), secciones que se entienden solas, entidades concretas, frescura **real** |
| Schema, `llms.txt` | No son palancas para la IA (sin efecto medible / nadie lee `llms.txt`). El schema se mantiene por sus otros usos; no venderlo como forma de salir en IA |
| Caída tras una migración, un cambio de plataforma o una carga masiva de productos | Primero comparar antes/después (301 de las URLs viejas, `noindex`/`robots.txt` heredados, canonical, contenido y JS) y descartar una acción manual; dejar un rastreo con alertas de lo que empeora. La IA no explica una caída en Google |
| Entrar a otro país o idioma | Validar la demanda **por mercado** con datos y entrar a uno a la vez; **localizar, no traducir** (keywords nativas, moneda, pagos); subdirectorios + hreflang; medir cada mercado por separado |
| Datos que no tenemos (backlinks, AI Mode, bots, YouTube por fuente…) | Decirlo; no suponer el valor. Lista en la capa del proyecto |
| Cuántas búsquedas hace la IA por detrás (fan-out) | Depende de la plataforma: ChatGPT abre subconsultas en ~la mitad de los prompts y casi siempre son dos (DataForSEO); el «9-11 por prompt» que cita Ahrefs no es de ChatGPT. Citar la cifra de la plataforma en cuestión |
| La visibilidad en IA «sigue igual» entre dos fechas | El neto esconde el movimiento: reportar menciones **ganadas y perdidas** y leerlas junto al volumen de búsqueda en IA de esas preguntas |
| Brechas frente a competidores en respuestas de IA | Separar los tres tipos: de **mención** (texto), de **entidad** (marca reconocida) y de **fuente** (dominio citado); revisar quién enlaza la página del competidor que la IA cita |
| Cifra de un estudio | Citarla con su fuente (Ahrefs, DataForSEO…) y el número de la referencia; no inventar ni redondear a conveniencia |

## Forma de la respuesta

1. La recomendación o el veredicto en la primera línea.
2. Los pasos en orden de prioridad, cada uno con su porqué en una frase.
3. Qué dato falta y cómo se consigue.
4. La compuerta del responsable, una sola vez, al final.

Dentro del límite de palabras del encargo; sin límite, lo más corto que cubra los pasos.

## Referencias por tema

| Tarea | Leer |
|---|---|
| Entender cómo cita la IA y qué prefiere cada plataforma | `references/busqueda-ia.md` |
| Elegir keywords, slots y prompts; objetivo clic vs mención | `references/keywords-y-prompts.md` |
| Escribir o actualizar fichas, guías, posts, FAQ | `references/contenido.md` |
| Menciones fuera del sitio, outreach, Reddit, desinformación | `references/menciones.md` |
| Videos y canal de YouTube | `references/youtube.md` |
| Auditoría técnica / on-page, bots de IA, URLs alucinadas | `references/auditoria-tecnica.md` |
| Auditoría de marca, brechas, progreso, cadencia | `references/auditoria-de-marca.md` |
| Medir tráfico de IA, bots, atribución; leer datos de IA; ROI | `references/medicion.md` |
| Vender en otros países o idiomas: demanda por mercado, URLs, hreflang, localización | `references/internacional.md` |

## Errores frecuentes

- Recomendar «arreglar la página de marca» cuando el AI Overview ya cita a terceros que hablan bien de nosotros.
- Proponer guías de 2.000+ palabras «para la IA».
- Tratar las subconsultas del fan-out (volumen cero, cambian cada vez) como keywords a perseguir.
- Confundir los enlaces de campañas (UTM) con los enlaces internos al buscar páginas que nadie enlaza.
- Proponer respuestas en Reddit o outreach sin pasar por el responsable.
