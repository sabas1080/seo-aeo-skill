# Cómo funciona la búsqueda con IA y en qué se diferencian las plataformas

Origen: notas 01, 04, 05 y 06 (`research/`).

## De dónde saca la IA lo que dice

| Fuente | Qué es | Cómo se influye |
|---|---|---|
| Datos de entrenamiento | Foto fija de la web (libros, sitios, PDFs, redes, transcripciones de YouTube); se renueva cada ~6 meses | Que la marca aparezca ligada a sus temas en muchos sitios con autoridad. Un producto recién lanzado **no existe** aquí |
| Recuperación en vivo (RAG) | La IA busca, lee unas páginas y responde con eso; se usa en preguntas recientes o específicas | SEO de siempre: posicionar, enlaces, contenido útil, rastreable y rápido |

## Query fan-out

- Una pregunta se abre en muchas subconsultas long tail que corren en paralelo y se combinan: de media **9-11 por
  prompt** (hasta 28); un *deep research* llegó a **420** búsquedas para una sola consulta de compra.
- Consecuencia: hay que ser relevante en **todo el tema** (subtemas incluidos), no en una keyword.
- Las subconsultas son sintéticas, cambian en cada corrida y **>95 % tienen volumen cero**: sirven como lista de
  subtemas a cubrir, **no** como keywords a perseguir ni a meter en el universo de palabras.

## Las citas son probabilísticas

- La misma pregunta cinco veces cita distinto (patrones de entrenamiento + señales de recuperación + temperatura).
  Se habla de **visibilidad** (una distribución), no de posición.
- Lo que sube la probabilidad de cita: **consenso** (muchas fuentes diciendo lo mismo de la marca), **frescura** (lo
  citado es ~25 % más reciente que lo de la SERP clásica) y **autoridad** (Google usa los mismos sistemas de calidad).
- No es sólo Google: ~14 % de las páginas citadas en AI Overviews no están ni en el top 100.

## Tres estados de visibilidad

1. **Citado con enlace** — tráfico medible.
2. **Mencionado sin enlace** — boca a boca a escala; la señal es orgánico plano/bajando con directo y búsquedas de
   marca subiendo.
3. **Invisible**.

Sólo ~**28 %** de las menciones llevan enlace. Ponderado por volumen, los enlaces se concentran en las preguntas con
más audiencia (Perplexity: enlaces en 78 % de las impresiones vs 51 % de las menciones; Gemini: 71 % vs 16,8 %). Las
menciones sin enlace también construyen presencia en el modelo: en un estudio de 75 mil marcas, las **menciones de
marca** fueron el factor más correlacionado con aparecer en IA, por encima de backlinks y domain rating.

## Cada plataforma es otro canal

| Plataforma | Qué cita | Solape con top 10 de Google | Menciones con enlace |
|---|---|---|---|
| Google AI Overviews | Autoridad; cada vez más **YouTube y Reddit** | Bajó de ~76 % a ~38 % | ~10,7 % |
| Google AI Mode | YouTube muy por delante, Instagram, TikTok, Reddit | — (sólo ~13,7 % de citas compartidas con AI Overviews pese a respuestas ~86 % parecidas) | ~36,8 % |
| ChatGPT | Editores, medios, Reddit, Wikipedia, reseñas de nicho | 8-10 % | ~26,9 % |
| Perplexity | La más parecida a Google; nicho y regionales | ~28,6 % | ~51,6 % |
| Gemini | — | — | ~16,8 % |

- De los 50 dominios más citados en AI Overviews, ChatGPT y Perplexity sólo 7 coinciden (~14 %).
- Prioridad por cuota: AI Overviews y ChatGPT concentran casi todo el tráfico de búsqueda con IA.
- Táctica: si ChatGPT pesa en el nicho → menciones en medios y reseñas; si AI Overviews → YouTube y Reddit.
- Las listas de dominios de Ahrefs son de España: compararlas con datos propios de los mercados donde se vende.

## Qué consecuencias tiene para leer datos

- Reportar **por plataforma**; un promedio entre plataformas esconde que somos invisibles en una.
- Juzgar «no nos enlaza» contra la tasa normal de esa plataforma: AI Overviews casi nunca enlaza; Perplexity, la mitad
  de las veces.
- Que el AI Overview cite una **reseña de YouTube de un tercero o un hilo de Reddit** sobre nuestro producto es lo
  esperable en Google y es una **mención valiosa** (nivel 1 o 2, ver `menciones.md`), no un fallo a «arreglar».
