# SEO internacional: entrar a otros países e idiomas

Origen: nota 18.

## 1. Validar la demanda antes de crear nada

Un mercado a la vez, y sólo si los datos lo respaldan. Tres lecturas:

| Lectura | Qué buscar |
|---|---|
| Dónde recibe tráfico la competencia | Tráfico orgánico de cada rival por país: si saca tráfico de un país donde no estamos, hay demanda y le dejamos el hueco |
| Dónde ya posicionamos sin saberlo | Nuestras keywords filtradas por país **y por idioma**: en un mismo país se busca en varios idiomas (países multilingües, expatriados) |
| Demanda por mercado | Cómo se busca la misma idea en cada idioma y país, con volumen real y crecimiento; da la keyword a apuntar en cada uno |

## 2. Estructura de URL

| Opción | A favor | En contra |
|---|---|---|
| Subdirectorios (`/fr/`, `/de/`) | La autoridad se acumula en un solo dominio; gestión sencilla | — |
| Dominio por país (ccTLD) | Reconocible para el usuario local; señal clara de país; alojamiento local | Caro y técnicamente complejo |
| Subdominios | Nombres personalizables; alojamiento local posible | Gestión parecida a la de los ccTLD |
| Parámetros de URL | — | **No usar**: confunden a usuarios y robots |

Google admite las tres primeras. Sin razón legal o de marca para otra cosa, subdirectorios.

## 3. Técnica propia de lo internacional

- **hreflang** en cada página con versiones: le dice a Google qué versión es para qué idioma o país. Sin él, las
  versiones pueden verse como **contenido duplicado** y Google indexa sólo una; las páginas de un mismo grupo
  hreflang **comparten señales**, así que un error pega al ranking de todas. Auditarlo con el rastreador, con alertas.
- **Velocidad desde lejos**: con un solo servidor, el visitante de otro continente carga lento y eso pesa en ese
  mercado; una **CDN** sirve desde un servidor cercano.
- **Enlazado interno por mercado**: cada versión enlaza a páginas de su mismo idioma o mercado.
- El resto de la auditoría técnica (`auditoria-tecnica.md`) va antes de replicar el sitio: los errores se multiplican
  por idioma.

## 4. Localizar, no traducir

- Keywords nativas de cada mercado, no la traducción de las propias: otras expresiones, otra intención, otro volumen.
- Cada mercado espera **su moneda, sus métodos de pago y sus referencias culturales**.
- Lo ideal es alguien que conozca el mercado. Para alinear equipos: una investigación general en el idioma principal
  como guía, adaptada por cada país.

## 5. Autoridad local

Enlaces y menciones **del propio mercado**: qué dominios de ese país e idioma enlazan a los competidores (medios,
blogs del sector) y cuáles nos faltan. Ver `menciones.md`.

## 6. Medir cada mercado por separado

Keywords, tráfico y competidores por país: igual que con las plataformas de IA, un agregado esconde el mercado que no
arranca.

## Cuatro errores

1. Lanzarse a varios mercados a la vez sin validar la demanda.
2. Traducir sin localizar.
3. Ignorar el SEO técnico (hreflang, velocidad, duplicados).
4. No monitorizar cada mercado de forma independiente.

## En un proyecto concreto

La capa del proyecto (p. ej. `seo-aeo-<proyecto>`) dice qué mercados e idiomas importan y con qué datos se miden.
