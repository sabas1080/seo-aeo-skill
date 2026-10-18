---
name: seo-aeo
description: Use when an agent plans, audits, briefs or reports on a brand's visibility in Google search or in AI answers (ChatGPT, Gemini, Perplexity, Claude, Google AI Overviews or AI Mode) — choosing keywords or prompts, briefing content meant to rank or be cited, reading SEO or AI-answer data, brand-gap or mention audits, YouTube SEO, crawlability for AI bots, or AI referral traffic. Complements ai-seo and seo-audit and wins when they disagree.
metadata:
  version: 2.3.0
---

# seo-aeo — SEO y visibilidad en IA

Destilada de los videos de Ahrefs en español (curso de AEO y afines). El SEO es la base del AEO: lo que posiciona en
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
| Brief de contenido | Sin meta de palabras (la longitud no correlaciona con la cita). Respuesta primero (BLUF), secciones que se entienden solas, entidades concretas, frescura **real** |
| Schema, `llms.txt` | No son palancas para la IA (sin efecto medible / nadie lee `llms.txt`). El schema se mantiene por sus otros usos; no venderlo como forma de salir en IA |
| Entrar a otro país o idioma | Validar la demanda **por mercado** con datos y entrar a uno a la vez; **localizar, no traducir** (keywords nativas, moneda, pagos); subdirectorios + hreflang; medir cada mercado por separado |
| Datos que no tenemos (backlinks, AI Mode, bots, YouTube por fuente…) | Decirlo; no suponer el valor. Lista en la capa del proyecto |
| Cifra de un estudio | Citarla como de Ahrefs, con el número de la referencia; no inventar ni redondear a conveniencia |

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
