# Product Strategy — COR

Repositorio de contexto de producto de **COR** ("Product Brain"): la base documental que usamos —personas y AI— para entender el producto, el mercado, la estrategia y la evidencia detrás de las decisiones.

> **Owner:** Product Manager, área de Producto
> **Última actualización:** 2026-08-21

## Qué es esto

Nueve archivos Markdown que documentan de forma viva el contexto de producto de COR: qué es el producto, quién lo usa, en qué mercado compite, hacia dónde apunta la estrategia, cómo se mide el éxito, qué dice la evidencia de discovery y qué hay en el roadmap.

Estos archivos alimentan el contexto de un **Proyecto de Claude ("COR – Product Context")**: al actualizar un archivo acá, hay que subir la nueva versión también al proyecto.

## Cómo usar este contexto

1. Leé siempre primero [`00-index.md`](00-index.md) para saber qué hay disponible y cuándo aplica cada archivo.
2. Identificá qué archivos son relevantes para la pregunta puntual — no hace falta cargar los 9 de una.
3. Respondé basándote solo en lo que está en los archivos. Si algo no está, decilo explícitamente — no inventar contexto de COR.
4. Si hay información contradictoria entre archivos, señalarlo en vez de elegir en silencio.
5. **La sección de AI de `06-kpi-tree` usa etiquetas de evidencia** (`[HECHO]` / `[HALLAZGO]` / `[HIPÓTESIS]` / `[BAJA]`). Respetá la etiqueta al citar un número, y no vuelvas a circular una afirmación dada de baja.
6. **Esa sección tiene además una convención de fuentes** (2026-08-18): **Amplitude** para alcance y penetración, el **log de conversaciones** para calidad y contenido, y el **backend de cálculo** para detección y umbrales. Son **tres fuentes, no dos**, con **ocho reglas**. Las dos que más se rompen: **regla 4 — no dividir una fuente por otra** (nada de tasas "detección → click") y **regla 8 — toda serie declara evento, filtro y valores incluidos**. No cruces Amplitude con Metabase sin leerla.

## Mapa de archivos

| Archivo | Qué contiene | Cuándo usarlo |
|---|---|---|
| [`00-index.md`](00-index.md) | Mapa de todo el contexto | Siempre primero |
| [`01-producto.md`](01-producto.md) | Qué es COR, propuesta de valor, funcionalidades, MAIA | Para entender qué hace el producto |
| [`02-equipos.md`](02-equipos.md) | Estructura de squads, roles, responsabilidades | Para saber quién hace qué |
| [`03-personas.md`](03-personas.md) | Segmentos, perfiles de usuario, comportamientos | Al diseñar features o evaluar impacto |
| [`04-mercado.md`](04-mercado.md) | Competidores, posicionamiento, oportunidades y amenazas | Al evaluar oportunidades o riesgos de mercado |
| [`05-estrategia-okrs.md`](05-estrategia-okrs.md) | Visión, pilares estratégicos, OKRs del trimestre | Al priorizar o alinear iniciativas |
| [`06-kpi-tree.md`](06-kpi-tree.md) | Árbol de métricas: de North Star a métricas operativas | Al definir éxito de una feature o analizar resultados |
| [`07-discovery.md`](07-discovery.md) | Insights curados de entrevistas, encuestas y datos | Al buscar evidencia para una decisión |
| [`08-roadmap.md`](08-roadmap.md) | Qué construimos, por qué y cuándo | Al evaluar prioridades o explicar la dirección |

## Estado de completitud

| Archivo | Estado |
|---|---|
| `01-producto.md` | Casi completo — suma la **arquitectura de orquestación** de MAIA (punto de entrada único, deploy 22-jul-26) y la **salvedad de proactividad** (no disponible hoy), ago-2026. **Actualizado 2026-08-18:** suma la **tabla del portafolio de la vertical de AI** (MAIA es un miembro, no el portafolio), Marketplace descrito como **feature hermana** y catálogo de modelos al día. **Entró Risk Management (2026-08-18):** resuelto como **pilar de MAIA con activación separada**, retirada la afirmación de que "opera con tres riesgos", reforzada la salvedad de proactividad. **Actualizado 2026-08-19:** base propia de **119 companies** (no "la misma de MAIA") y penetración **⏸️ en pausa** — pendiente confirmar anti-scope y si el custom prompt del banner entra por el Orquestador. **Actualizado 2026-08-19:** MAIA **sale de beta cerrada** — release a toda la base la semana del 24-ago-26 (128 → ~300 companies, entra el Colaborador), decidido fuera de Producto |
| `02-equipos.md` | Completo |
| `03-personas.md` | Casi completo. **Actualizado 2026-08-18:** banners de riesgo por rol (**segundo caso del sesgo de denominador de `[BAJA-01]`**), refuerzo del hallazgo de Presupuestos y la anomalía de agosto del C-Level como pendiente de verificación. **Actualizado 2026-08-19:** los porcentajes por rol quedan **⏸️ en pausa** y se **cierra el denominador de Director** (923, dato duro) — pendiente personas por vertical nuevo y detalle de rollout/champion. **Actualizado 2026-08-19:** **ficha propia del Colaborador y MAIA** (0,27% sobre 5.605 asientos, denominador separado); su primer paso es discovery, no un KR |
| `04-mercado.md` | Competidores confirmados — pendiente vertical nuevo, precio y cruce con churn |
| `05-estrategia-okrs.md` | Marco de priorización confirmado + laddering de "Deploy de AI" con baseline y **cinco anti-metas** (la quinta, del 2026-08-18: no leer el alcance de Risk Management como alcance de MAIA). **Actualizado 2026-08-19:** el KR de penetración pasa de **dos bloqueos a uno**, y se carga la **spec del evento de acción aplicada** (IDs de entidades; sin evento de "acción revertida") — pendientes OKRs de producto por eje. **Actualizado 2026-08-19 — entran los primeros OKRs de producto de COR:** **O1 confiabilidad** (5 KRs, su Q4 produce baselines y no mejoras) y **O2 adopción validada en Enterprise + Midmarket** (alcance →25%, retorno ≤25%, activación de cohorte 40%, 6 de 8 cuentas dormidas); **O3 ⏸️ en revisión** por pricing. **Actualizado 2026-08-21 — O1 reescrito:** ahora es **"Ejecución confiable"** con **4 KRs** (cobertura de respuesta **75%** · éxito de ejecución **80% Q4 → 95% Q1** · flujo de archivos **80%** · performance **≥95% con primer token <3s**); se retiraron **precisión verificada, conversión de apertura y tickets por 100 usuarios**. ⚠️ **Las cuatro metas son provisorias: ninguna se fijó contra una medición.** Y queda declarado que **ningún KR mide si MAIA dice la verdad** |
| `06-kpi-tree.md` | North Star de negocio y engagement con baseline real; **sección de AI reescrita (ago-2026)**: penetración sobre asientos elegibles + etiquetado de evidencia. **Actualizado 2026-08-18:** cubre **tres features medidas** (MAIA, Marketplace y **Risk Management**, esta última adentro de MAIA con corte por origen), suma la **convención de tres fuentes con ocho reglas de lectura** y la **calibración de umbrales**. **Actualizado 2026-08-19:** el baseline de MAIA sube a `[HECHO]` y **piso conservador**, y la **penetración de Risk Management queda ⏸️ en pausa** (denominador propio: 119 companies, no 128). **Ajustes de criterios del 2026-08-19 (ningún número cambia):** se cierra el 🔴 del filtro `agent_type` —MAIA y Marketplace son series independientes y la brecha 1,40% vs. 11,6% es real—, el "Pedido a Data" pasa a **"Consultas pendientes de correr"** (los exports los arma el owner) y se especifica el evento de acción aplicada con IDs de entidades — pendiente North Star de producto y calidad de servicio. **Actualizado 2026-08-19:** **mapa de instrumentación de los 9 KRs**, **corte de serie por el release del 24-ago** (el denominador oficial pasa al panel Enterprise + Midmarket) y tres pedidos promovidos a 🔴, dos con fecha límite antes del release. **Actualizado 2026-08-21:** la tabla de O1 se reemplaza (**4 KRs, renumerados**) y suma los **cortes obligatorios por KR**; entran el **Corte H** (distribución de TTFT partida en el deploy del Orquestador) y el **Corte I** (flujo de archivos, más una spec inexistente que una consulta); `option = header` y la serie de tickets **bajan de 🔴** al retirarse sus KRs, sin borrarse |
| `07-discovery.md` | Repositorio estructurado con research primario (Retently). **Actualizado 2026-08-18:** el target de Crowe cambia de pregunta y entran dos targets nuevos de Risk Management. **Actualizado 2026-08-19:** el de no-retorno queda recortado a la cohorte de mayo y entra el más urgente — **las 79 companies de julio que no movieron el conteo de usuarios** — pendiente corte por segmento/vertical. **Actualizado 2026-08-19:** target nuevo de **~15 Colaboradores** con ventana antes del release; las 8 dormidas ahora sostienen un KR con meta. **Actualizado 2026-08-21:** targets del **flujo de archivos** y de la **percepción de velocidad**, más la salvedad de que las 25 menciones de archivos de I-07 son de **adjuntos en tareas de COR, no de MAIA** |
| `08-roadmap.md` | Estructura y temas candidatos (suma activación de la base de MAIA, ago-2026). **Actualizado 2026-08-18:** Risk Management como **caso a favor del eje capacidad vs. superficie**, evidencia de calibración al tema 0 y **recomendación de no ir a GA** todavía. **Actualizado 2026-08-19:** confounder de mayo marcado (Risk Management se habilitó el 14-may-26) — el roadmap real todavía no está cargado. **Actualizado 2026-08-19:** el **release del 24-ago reordena los temas** y hay **dos instrumentaciones con fecha de vencimiento**; lo que no lleva KR queda como iniciativa que necesita dueño. **Actualizado 2026-08-21:** performance de MAIA ya tiene KR (TTFT <3s) **pero la plataforma no**; el hueco de "nadie mide si MAIA dice la verdad" queda junto a la deuda de cálculos; y el eje capacidad vs. superficie gana una cuarta vía de test — **el costo en latencia del Orquestador** |

## Cómo se mantiene

- Cada archivo es un **repositorio vivo**: se actualiza a medida que llega research, decisiones o datos nuevos.
- Los pendientes de cada archivo están marcados al final, en su propia sección "Pendientes — input interno".
- Al resolver un pendiente o cargar información nueva, actualizar el archivo correspondiente y reflejar el cambio en la sección de estado de completitud de [`00-index.md`](00-index.md).
- Evidencia y fuentes van siempre citadas — sobre todo en `07-discovery.md`, donde cada insight debe tener evidencia, fuente y nivel de confianza.
