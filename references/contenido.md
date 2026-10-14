# Crear y actualizar contenido que la IA cite (y que posicione)

Origen: notas 03, 09 y 12 (estructura HTML).

## Lo que dicen los datos

| Factor | Evidencia | Regla |
|---|---|---|
| Longitud | Correlación con la cita **0,04** (≈ nula) sobre 174 mil páginas; 53,4 % de las citadas < 1.000 palabras | **No fijar metas de palabras.** La medida es si responde la pregunta completa |
| Frescura | Lo citado es ~25,7 % más reciente que lo que posiciona; en ChatGPT 89,7 % de lo más citado se actualizó en el año y 76 % en los últimos 30 días | Actualizaciones **reales** (datos, ejemplos, versiones); cambiar sólo la fecha no sirve, Google lo detecta |
| Formato | ~43,8 % de lo citado por ChatGPT son listas, comparativas, reseñas; se cita mucho el contenido con **datos propios** y las comparativas **A vs B** | Usar esos formatos cuando encajen con la intención |
| Cobertura | La IA arma la respuesta con varias páginas por subtema (fan-out) | Cubrir el tema y sus subtemas; si falta un subtema, la IA toma la página de otro |

No existe un «formato para robots»: lo que funciona para personas es lo que la IA prefiere citar.

## Cómo escribir (manda sobre otras guías de estilo)

1. **BLUF**: cada sección abre con la respuesta, no con contexto. Personas y LLM pesan más el principio y el final de
   un fragmento; una idea en el tercer párrafo se pierde. Después, contexto y ejemplos.
2. **Atómico**: cada sección (H2) se entiende sola, porque la IA trocea y cada modelo corta distinto. Prueba: leer el
   H2 fuera de contexto; si no se entiende, reescribirlo.
3. **Rico en entidades**: nombres concretos de producto, chip, protocolo, versión, persona y relaciones. «El sniffer X
   v3 con radio CC1352 captura Zigbee, Thread y BLE», no «esta placa ayuda con IoT».
4. **Simple y declarativo**: sujeto-verbo-objeto, una idea por frase; si pide dos lecturas, partirla.
5. **Jerarquía limpia**: un H1, H2 para secciones, H3 para subsecciones, párrafos de una idea.

## Palancas extra

- **Ponerle marca a las ideas propias**: un marco o método original se diluye como conocimiento general si no lleva
  nombre; nombrarlo con la marca, definirlo claro y repetirlo en blog, YouTube, redes, Reddit.
- **Reactivar páginas dormidas**: páginas que posicionaban y fueron cayendo **y que tienen enlaces**; actualizarlas
  es de lo más rápido para ganar visibilidad en IA. Sin dominios de referencia, actualizar no basta.
- **FAQ oficial con datos concretos**: la IA prefiere lo específico y estructurado, aunque sea falso, frente a una
  verdad ambigua. Cubrir cada hueco de información de la marca y del producto con respuestas con cifras, fechas y
  hechos (ver `menciones.md`, desinformación).

## Ecommerce (de la entrevista a Mercado Libre)

- **PDP antes que categoría**: Google prefiere cada vez más la ficha de producto y los agentes de compra aterrizan
  ahí. Luego el **feed de Merchant Center** (títulos, descripciones propias, fotos de uso real) y su automatización.
- **Indexar lo que genera negocio**, no todo; el enlazado interno es el arma para forzar rastreo de lo que vale.
- **IA para escalar, con revisión humana**: lo hecho sólo con IA pega rápido y no se sostiene (golpeado por updates);
  humanizado rindió ~31× más visitas en su prueba. Revisar a mano lo que paga el negocio y mantenerlo fresco.

## En un proyecto concreto

La capa del proyecto (p. ej. `seo-aeo-<proyecto>`) dice con qué datos y reglas propias se aplica esto.
