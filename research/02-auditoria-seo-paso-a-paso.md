# 02 — «Auditoría SEO al completo paso a paso» (Ahrefs en español)

Fuente: https://www.youtube.com/watch?v=lF587mOEVEM · notas destiladas (paráfrasis, no transcripción) de un video público de Ahrefs.

## Estructura de la auditoría

Tres partes que se pueden hacer por separado: **técnica → on-page → contenido**, más una cuarta que ya es
obligatoria: **presencia en respuestas de IA**. Orden importa: primero que robots y usuarios puedan llegar.

Advertencia de Ahrefs: con un rastreo de 170+ tipos de problema, querer arreglarlo todo de golpe es
contraproducente; priorizar en este orden.

## 1. Técnica

1. **Indexación primero** (lo más crítico: sin índice no hay posición). Buscar páginas con `noindex` que sí
   deberían indexarse; confirmar en el HTML (meta robots) y corregir en el plugin del CMS o en el código.
2. **Una sola versión del sitio**: https y con/sin www consistentes; todas las variantes redirigen (301) a la
   principal. Si no, duplicados. Comprobar con las cabeceras HTTP.
3. **Core Web Vitals** (carga, interactividad, estabilidad visual) con datos de campo de Chrome UX Report.
   Arreglos típicos: imágenes grandes y JavaScript innecesario.
4. **Móvil** (factor de ranking desde 2019): tema responsive, imágenes < 1 MB comprimidas sin perder calidad,
   probar en varios dispositivos y navegadores.

## 2. On-page (más tráfico con lo que ya existe)

1. **¿Hubo caída?** Cruzar la curva de tráfico orgánico con las fechas de actualizaciones de Google
   (calidad de contenido, spam de enlaces…). Luego bajar al detalle: comparar páginas antes/después de la
   fecha del update, filtrar las que empeoraron, ordenar por mayor pérdida.
2. **Reoptimizar las páginas que cayeron**: identificar la intención de búsqueda que deberían atender y
   compararlas contra las que mejor posicionan **por subtemas**; rellenar los subtemas que faltan.
3. **Básicos**: title, meta description, H1 (vacíos, demasiado largos, faltantes).
   Dato: Google reescribe la meta description ~63 % de las veces → no vale la pena redactar a mano decenas;
   generarlas en lote es aceptable (priorizar title y H1).
4. **Enlazado interno** — dos funciones: navegación de usuarios/rastreadores y reparto de autoridad
   (PageRank) de páginas fuertes a las que lo necesitan.
   - Oportunidades: desde qué página, con qué contexto de keyword, hacia qué página enlazar.
   - Enlaces internos rotos (404) → redirigir o arreglar.
   - **Páginas huérfanas** (ningún enlace interno las apunta) → reconectarlas.

## 3. Contenido (oportunidades nuevas)

- **Content gap**: keywords donde algún competidor está en top 10 y nosotros no. Afinar exigiendo que
  **más de un competidor** posicione → señal de demanda real → calendario editorial.

## 4. Presencia en IA

- Listar las keywords donde ya salimos en AI Overviews y **ver qué otras fuentes usó la respuesta** (p. ej. un
  video de YouTube, un comparador): dice qué páginas nuestras funcionan en IA y qué menciones externas nos
  están ayudando.
- Comparar contra competidores también en ChatGPT, Gemini, Perplexity: en qué temas nos mencionan o enlazan a
  nosotros y a ellos.
