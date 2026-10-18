# 30 — «Query Fan-Out in LLMs: Key Findings from 100,000 ChatGPT Prompts» (DataForSEO)

Fuente: https://www.youtube.com/watch?v=oe5YbdosUsw (publicado 4-ago-2026, 12:54) · notas destiladas (paráfrasis, no transcripción) de un video público de DataForSEO (proveedor de APIs de datos SEO y de IA); subtítulos automáticos en inglés. Las demostraciones de su API quedan fuera salvo cuando dicen qué dato hace falta. Estudio de DataForSEO
sobre 100 mil prompts de ChatGPT y más de 100 mil subconsultas; las cifras son de **ChatGPT**, no de Google.

## Ideas clave

1. **Frecuencia**: ChatGPT abrió subconsultas en el **47,5 %** de los prompts. Cuando lo hace, en el **93 %** genera
   **exactamente dos**; tres o cuatro, ~6 %; más de cinco, casi nunca; una sola, casi nunca.
2. **Longitud**: ~80 % de las subconsultas miden 31-90 caracteres (9-14 palabras); son **más largas** que los prompts del
   usuario (la mayoría de los prompts, 31-60 caracteres; ~51 % de las subconsultas, 61-90).
3. **Más demanda, más subconsultas**: por deciles de volumen de búsqueda en IA, los prompts poco buscados abren
   subconsultas ~44 % de las veces y los muy buscados, 51-55 % (correlación, no causa).
4. **Intención**: 64,5 % informacionales y ~1/3 comerciales o transaccionales. Las comerciales abren algo más que las
   informacionales y las transaccionales, menos (navegacionales 53 %, muestra chica). Influye, pero poco.
5. **La palabra de la pregunta importa más que el formato de pregunta**: preguntar con qué/quién/cómo no cambia la tasa,
   pero **dónde** llega a 67 %, **quién** 60 %, **cuál** 56 % y **qué** queda en 44 % (las definiciones se resuelven
   sin buscar).
6. **Comida, viajes y local** son los temas con más subconsultas (palabras como menú, restaurante, hoy, hotel, popular).
7. **Qué añade ChatGPT a la subconsulta**: conectores, alternativas o contrastes (y, o, vs), aclaración (qué, cuál,
   cómo), evaluación (mejor, top, reseñas) y términos comerciales (costo, precio). No parafrasea: reestructura.
8. **Solapamiento de palabras**: subconsulta y prompt, 54 %; con títulos de los resultados recuperados, 53 %; con sus
   descripciones, 59 %; con los títulos de las **fuentes citadas**, 47 %; con sus descripciones, sólo 8 %. La subconsulta
   sirve para recuperar; la cita depende de que la fuente sirva para la respuesta.
9. **Dominios recuperados ≠ citados**: lo más recuperado fue Yahoo, Fandom y Alibaba; lo más citado, Wikipedia, Reddit,
   Alibaba, Forbes y Yahoo.
