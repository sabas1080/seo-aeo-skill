# Elegir keywords y prompts: objetivo clic u objetivo mención

Origen: notas 01, 03, 08, 13, 15, 16 y 17.

## 1. Armar la lista

- **Semillas** (1-2 palabras del nicho) + **modificadores** («best», «vs», «how to», «alternative», «for <uso>»);
  expandir con datos reales (términos coincidentes que contengan los modificadores).
- Si el proyecto ya tiene un universo de palabras (semillas, alias de productos, Search Console), partir de él; la capa
  del proyecto dice dónde está y cómo pedir palabras nuevas.
- **Brecha de contenido**: palabras donde todos los competidores posicionan y nosotros no; da el foco de qué cubrir.
- **Lo que ya posiciona** es lo más barato de subir: palabras donde ya salimos cerca del primer puesto (posiciones
  2-5) y **fragmentos destacados** que se pueden ganar; se actualiza la página que ya existe en vez de crear otra.
- **Herramientas gratuitas con demanda sin atender** (calculadoras, convertidores, comprobadores): si mucha gente busca
  una herramienta y las que hay no sirven, construirla puede ser el primer motor de tráfico (caso Roomix: ×5 en un mes).

## 2. Pruebas antes de comprometerse

0. **¿Es un subtema?** Comparar el volumen de la keyword con el **tráfico potencial total** de la página que posiciona
   primero: si esa página trae mucho más que el volumen (posiciona por cientos de palabras del tema padre), lo que
   conviene es la página del **tema padre**, que cubra la keyword como sección. No es una hipótesis: es la regla.
1. **Negocio**, en puntos: **3** = el producto es la solución directa; **2** = se relaciona fácil; **1** = se puede
   mencionar; **0** = no encaja. Priorizar por puntos antes que por volumen. Una definición («what is Zigbee») tiene
   volumen y 0 puntos.
2. **Intención según la SERP**: buscarla y ver qué posiciona. Si son tiendas, un post no entra; si son tutoriales, una
   ficha tampoco.
3. **Dificultad**: autoridad y dominios de referencia del top 10; sitios débiles en el top 10 = buena señal. Los
   backlinks siguen siendo factor de posicionamiento: cuanto más difícil la keyword, más enlaces hacen falta, y el
   motivo para que enlacen es el enfoque único de la página (ver `contenido.md`).

## 3. Filtro de IA

Pregunta: **¿la IA puede resolver por completo lo que busca el usuario?**

- AI Overviews aparece en ~21 % de todas las keywords, ~58 % de las formuladas como pregunta, ~46 % de las de 7+
  palabras; 99,9 % de las que lo disparan son informacionales.
- En búsquedas de **herramienta, servicio o producto para comprar** casi nunca aparece: ahí el clic orgánico sigue.

## 4. Decidir el objetivo de cada keyword

| Señales | Objetivo | Activo |
|---|---|---|
| Transaccional/comercial, **sin** AI Overview | **Clic** (SEO clásico) | Ficha de producto (PDP primero), luego colección |
| Comercial **con** AI Overview («best X», «X vs Y», «X alternative») | **Mención** en la respuesta **y** clic | Entrar en las listas y comparativas **de terceros** que la IA cita (~43,8 % de lo citado son listas/comparativas); una comparativa propia honesta como complemento. Si el sitio es un medio, blog o afiliado que no vende el producto, su propia lista **es** la de terceros: hacerla la mejor de la SERP |
| Informacional con AI Overview que la resuelve | **Mención** (no tráfico) | Guía o tutorial que cubra el tema completo; YouTube; menciones externas |
| Informacional que la IA no resuelve (pasos, código, troubleshooting) | Clic | Tutorial/guía con la ficha enlazada |
| Volumen ~0 pero frase típica de pregunta a IA («ProductoA vs dongle genérico») | **Mención** | Sección o página de comparativa; el volumen de Google no mide cuánto se pregunta a la IA |

- No descartar una keyword de comparativa A vs B por volumen bajo: es el formato que más encaja con cómo la gente
  le pregunta a la IA.
- Las keywords que la IA resuelve no se ignoran: cambian de objetivo (mención en lugar de clic).

## 5. Slots: si no ganas por la puerta, entra por la ventana

La SERP tiene muchos espacios: enlaces azules, **Shopping/Merchant Center** (sólo para quien vende el producto), imágenes, videos cortos, YouTube,
People Also Ask, respuestas de IA. Contra un dominio más fuerte, buscar el slot donde sí cabes y apuntar a
**reemplazar** un resultado del mismo tipo (si sale un video, otro video mejor). Lo que entra por otro slot es venta
incremental.

## 6. Volatilidad

>45 % de las citas de AI Overviews cambian en cada actualización, que ocurre cada ~2 días. Una captura semanal es una
muestra: tendencias con 4-6 capturas, revisión periódica, nunca una semana suelta.

## 7. Prompts (preguntas a la IA)

- La gente conversa con contexto («soy pentester y busco…»); diez formulaciones dan diez respuestas con marcas
  distintas, más el fan-out invisible. **No se optimiza para un prompt exacto**: se construye visibilidad en el tema.
- Para **medir**, seguir un set propio de prompts agrupados por categoría:
  - **marca** (¿el modelo nos conoce?) — pocos, como control;
  - **cerca de la compra** («best tool for…», «X vs Y», «alternative to…»);
  - **por producto/tema** (protocolos, casos de uso).
  - 2-3 formulaciones por tema y con contexto de persona (pentester, estudiante, maker) para compensar la volatilidad.
- Cambiar el texto de un prompt empieza otra serie: mantener un grupo fijo de control para comparar entre rondas.
- Los prompts también sirven para **descubrir**: preguntar como lo haría un cliente revela por qué la IA recomienda a
  los rivales y preguntas sin buena respuesta en ningún sitio, que se vuelven contenido.
