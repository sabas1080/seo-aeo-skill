# Auditoría técnica y on-page (Google y bots de IA)

Origen: notas 02, 12, 15, 16 y 20.

## Orden de prioridad

Con decenas de tipos de problema, arreglarlo todo de golpe es contraproducente. Este orden:

1. **Indexación**: páginas que deberían indexarse con `noindex` (sin índice no hay posición). Antes, revisar si hay
   una **acción manual** de Google (en Search Console: Seguridad y acciones manuales): explica caídas que nada técnico
   explica y trae cómo resolverla.
2. **Una sola versión del sitio**: http/https y con/sin www redirigen (301) a la principal; si no, duplicados.
3. **Acceso de bots de IA** en `robots.txt`: GPTBot y OAI-SearchBot (OpenAI), ChatGPT-User, ClaudeBot (Anthropic),
   Google-Extended, PerplexityBot. Un `Disallow` = esa plataforma no ve el contenido. Suele heredarse de plantillas o
   lo añaden CDNs (p. ej. la opción de Cloudflare de vetar entrenamiento).
   **Además del `robots.txt`, el proveedor** (CDN, firewall, captcha antibots) puede bloquear por defecto sin que nadie lo
   haya decidido. La evidencia de acceso es lo que vivieron **los bots reales**: el panel de bots/IA del CDN o los logs del
   servidor (peticiones por bot y su código). Un `curl` con el user-agent del bot desde tu IP **no es evidencia**: los
   CDN verifican la IP del bot y frenan al impostor (403/429) aunque al bot real lo dejen pasar; un 403/429 así es
   falso positivo hasta confirmarlo en el panel o los logs.
4. **Renderizado sin JavaScript**: Gemini y Copilot renderizan JS; **el bot de ChatGPT no**. Contenido que depende de
   JS = página vacía para ChatGPT. Prueba: pedir la página sin JS (navegador o `curl`) y buscar el texto.
5. **Velocidad / Core Web Vitals**: una página lenta puede descartarse antes de ser evaluada por la IA. Arreglos
   típicos: imágenes grandes (< 1 MB comprimidas) y JS innecesario.
6. **Móvil**: responsive, probar en varios dispositivos.
7. **On-page**: title y H1 (vacíos, largos, faltantes); un solo H1 y sin saltos de nivel; URLs legibles que digan qué
   hay en la página (sin IDs ni números sueltos). La meta description al final:
   Google la reescribe ~63 % de las veces, generarlas en lote es aceptable. Excepción: una página con **buena posición
   y CTR bajo** pide reescribir primero su título (y su meta).
8. **Enlazado interno**: oportunidades, enlaces internos rotos (404) y **páginas sin enlaces internos** (reconectarlas
   reparte autoridad).
9. **URLs alucinadas por la IA**: los asistentes mandan a 404 ~2,87× más que Google (ChatGPT ~1 % de sus URLs).
   Detectar URLs inventadas con tráfico de IA recurrente y redirigirlas a la página real más parecida.

## Vigilancia continua

Un rastreo programado con alertas de lo que **empeoró** detecta en horas lo que nadie ve: JavaScript roto tras un
**cambio de plataforma**, 404 tras **subir una tanda de productos**, bucles de redirección. Es lo que más vale tras
cualquier migración o carga masiva; el valor se cuenta también en lo que se dejó de perder.

## Lo que NO es palanca para la IA

| Cosa | Evidencia | Qué hacer |
|---|---|---|
| Schema / datos estructurados | Experimento con 1.885 páginas: sin cambio apreciable en citas de IA | Mantenerlo y ponerlo en páginas nuevas por sus otros usos (resultados enriquecidos, voz, knowledge graph); **no** presentarlo como forma de salir en la IA |
| `llms.txt` | ~28 % de 137 mil dominios lo publican; ~97 % de ésos no recibe ni una petición | No priorizarlo; nunca por delante de lo de arriba |

## Caídas de tráfico

Primero, acciones manuales y lo técnico de arriba. Luego cruzar la curva de orgánico con las fechas de actualizaciones
de Google; después bajar a página: comparar antes/después
del update, filtrar las que empeoraron y ordenar por mayor pérdida; reoptimizarlas por intención y subtemas.
