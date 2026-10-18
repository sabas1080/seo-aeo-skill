# Medir el AEO: tráfico, bots, atribución y valor

Origen: notas 04, 06, 13, 14, 15, 16, 19, 20, 23, 26, 27 y 33.

## Tres pilares + prompts propios

| Pilar | Qué dice | Trampa |
|---|---|---|
| Tráfico de referencia de IA | Qué plataformas mandan visitas y a qué páginas | **Subestima**: ChatGPT de pago en enlaces del texto (`noreferrer`), app de escritorio de Perplexity, Copilot en Windows y Grok no pasan referente → caen en «directo». Usarlo para tendencias |
| Actividad de bots de IA | A qué contenido presta atención la IA | Bots de **entrenamiento** (GPTBot, Google-Extended) ≠ bots de **búsqueda/cita** (ChatGPT-User, OAI-SearchBot); sólo los segundos traen tráfico |
| Atribución autodeclarada | Qué genera ingreso | Hay que **preguntar** («¿cómo nos conociste?» con opciones de IA); sin preguntar no aparece |
| Prompts propios | Presencia en las preguntas que importan al negocio | La base general de prompts de una herramienta incluye mucho irrelevante; agrupar por categoría con varias formulaciones |

**Search Console sólo guarda 16 meses**: comparar contra hace dos años exige haber acumulado la serie propia (o
una herramienta conectada) desde antes; si no existe, decirlo y empezar a guardarla.

Lecturas útiles: páginas que ya reciben tráfico de IA (mantenerlas al día con CTA clara) y páginas clave con cero
tráfico de IA (investigar contenido, rastreo o tema).

## Plan de seguimiento: de la pregunta al dato

1. **Empezar por la pregunta de negocio** («¿dónde nos gana el competidor en la IA?»), no por las métricas.
2. **Alcance**: marca y dominio, competidores, prompts prioritarios (casos de uso, comparativas, problemas del cliente,
   decisiones de compra) con su tema, mercado e intención, plataformas y **cadencia** (quincenal o mensual para
   empezar). Set fijo y chico; se amplía después.
3. **Cuatro KPIs**, cada uno con su acción (ver `auditoria-de-marca.md`):
   - **Frecuencia de mención**: en cuántas respuestas del set salimos (25 de 100 = línea base).
   - **Cuota de voz**: nosotros frente a cada competidor sobre las mismas respuestas; el conteo solo engaña.
   - **Contexto y sentimiento**: cómo nos describe la IA.
   - **Exactitud**: si los hechos son correctos.
   - De apoyo: **frecuencia de cita** (fuente con enlace) y **cobertura del set** (qué parte de los prompts nos da
     visibilidad).
4. Comparar con los competidores **en la misma respuesta** (buscar todas las marcas en cada respuesta), no con
   corridas distintas.

## Reglas para leer los datos de IA

1. **Una ronda es una muestra.** Las citas son probabilísticas y las de AI Overviews cambian cada ~2 días: no declarar
   caída o subida con una sola ronda o una sola pregunta; tendencias con varias rondas (4-6 capturas semanales).
2. **Por plataforma, nunca promediado entre plataformas.** Con ~14 % de solape de fuentes, un promedio esconde la
   plataforma donde somos invisibles.
3. **Tres estados, siempre**: citado con enlace / mencionado sin enlace / invisible. Comparar la tasa de enlace con la
   normal de esa plataforma (AI Overviews ~10,7 %, Gemini ~16,8 %, ChatGPT ~26,9 %, AI Mode ~36,8 %, Perplexity
   ~51,6 %) antes de llamarlo problema.
4. **Agregado por grupo de prompts**, no pregunta por pregunta.
5. **El neto esconde el movimiento**: 50 menciones un mes y 51 el siguiente puede ser 20 ganadas y 19 perdidas.
   Reportar **ganadas y perdidas**, no sólo el neto.
6. **Menciones con su demanda**: leer las menciones junto al volumen de búsqueda en IA de esas preguntas; más
   menciones en preguntas poco buscadas pueden valer menos que menos menciones en preguntas muy buscadas.
7. **Si la visibilidad baja**, ver qué URLs se citan ahora en esos temas y clasificarlas (editorial, ficha,
   documentación, reseñas, comunidad): dice si la IA se movió a contenido más fresco, a editores con más autoridad, a
   discusiones de usuarios o a otro formato.
8. **Señal de mención sin enlace**: búsquedas de marca y tráfico directo subiendo con orgánico genérico plano.

## Vigilancia con un agente programado

Un agente que corre solo cada semana (o cada día) y cruza posiciones, Search Console, analítica y enlaces:

- **Lista corta de consultas imprescindibles** (~20) con su posición; explica caídas (qué cambió, quién subió).
- **Avisa de lo que se rompe**: pico de errores en la auditoría técnica, páginas que dejan de indexarse.
- **Avisa de lo bueno que nadie ve**: enlaces o menciones nuevas de medios con autoridad.
- **Guía de lo que ya se probó y no funcionó**, que el agente lee antes de proponer, para no repetir ideas descartadas.

Entrega lecturas con accionables cuando son evidentes; decidir sigue siendo del responsable.

## Reportar a dirección cuando el tráfico no sigue a la visibilidad

- Reportar **trabajo + contexto + ingreso**: impresiones, clics, keywords en top 3 y top 10 **e ingreso** del canal, en
  el mismo informe. El tráfico solo ya no basta: un sitio puede perder clics y vender más.
- Keywords que crecen y clics que no tienen dos explicaciones posibles, que hay que separar: (1) las keywords ganadas no
  son las que venden (revisar por intención y por página), o (2) Google cambió las reglas: con AI Overviews los clics caen
  **~58 %** (Ahrefs, 2026; antes medían ~34 %), y los **anuncios que parecen orgánicos** se llevan clics incluso en
  búsquedas de marca.
- **Paciencia con método**: no cambiar de estrategia cada dos meses porque un dato bajó; medir con constancia y cambiar
  de rumbo sólo tras darle tiempo.

## ¿Vale la pena? (para explicarlo)

- Volumen todavía chico: referencia de IA ~0,25 % del tráfico de un sitio; Google manda ~210× más que todas las IA
  juntas y ~190× más que ChatGPT (dato de 2026).
- Calidad alta: en Ahrefs, los visitantes de IA convierten ~23× más que orgánico; ~3 % de sus conversiones declaradas
  vinieron de IA.
- Crecimiento: ×9,7 en un año; ChatGPT ya manda más que Reddit o LinkedIn.
- El valor principal es la notoriedad dentro de la conversación (impresiones sin clic). AEO es una capa sobre el SEO,
  no un reemplazo; se mide como brand marketing, no venta por venta.

## En un proyecto concreto

La capa del proyecto (p. ej. `seo-aeo-<proyecto>`) dice con qué datos y reglas propias se aplica esto.
