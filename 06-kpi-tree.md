# 06 — KPI Tree (COR)

> **Última actualización:** 2026-08-19
> **Owner:** Product Manager, área de Producto
> **Contexto para IA:** Árbol de métricas de COR, desde la North Star hasta las métricas operativas y de producto, para definir el éxito de una feature o analizar resultados. Las métricas de **negocio** vienen confirmadas del Business Plan 2026–2027 (`05`); las de **producto** están inferidas y marcadas como hipótesis hasta confirmarlas.
>
> ⚠️ **La sección de AI usa un etiquetado de evidencia propio** (`[HECHO]` / `[HALLAZGO]` / `[HIPÓTESIS]` / `[BAJA]`) definido dentro de esa sección. **Respetar la etiqueta al citar un número:** un `[HALLAZGO]` no se cita como si fuera un hecho, y un `[HIPÓTESIS]` no sirve para justificar reparto de capacidad. El resto del archivo todavía no está etiquetado.
>
> ⚠️ **La sección de AI también tiene una convención de fuentes** (2026-08-18): **Amplitude** para alcance, el **log de conversaciones** para calidad y el **backend de cálculo** para umbrales, con **ocho reglas de lectura** — la más importante es la **regla 4: no dividir una fuente por otra**, y la **regla 8** obliga a declarar el filtro de toda serie. Está definida dentro de la sección, junto al etiquetado. **No cruzar Amplitude con Metabase sin leerla.**

## Cómo leer este árbol

North Star (arriba) → palancas de negocio → métricas operativas → métricas de producto (drivers). Cada nivel debería "explicar" el de arriba.

## North Star

- **De negocio (confirmada):** **ARR** — meta $10.2M para cierre 2027.
- **De producto (pendiente):** todavía no hay una North Star de producto definida. Candidatas sin confirmar: **rentabilidad gestionada activamente** (clientes/proyectos usando COR para actuar sobre el margen) o **heavy users activos** (colaboradores + PMs con uso recurrente).

> _Pendiente: definir eventualmente la North Star de producto (y posiblemente otras métricas cabecera por eje/squad, ver `02-equipos`)._

## Nivel 1 — Métricas de negocio (confirmadas, del Business Plan)

- **ARR** — meta $10.2M (Exit 2027). Hoy ~$5.48M; goal 2026 $6.8M.
- **ARR Annual Growth:** 51%.
- **NRR (Net Revenue Retention):** 115%.
- **GRR (Gross Revenue Retention):** 90%.

## Nivel 2 — Palancas de negocio

### Adquisición (Net New — $2.38M plan 2027)
- New logos por **vertical** y **geografía** (Agencias LatAm/Brasil/EMEA, IT Consulting, Law & Accounting, Brands, Media).
- **Pipeline** por vertical y **conversion rate** por vertical *(desafío explícito del plan)*.
- **Whales** (cuentas grandes de ticket alto) y **ACV / ticket promedio**.

### Retención y expansión (sostiene NRR 115% / GRR 90% — Installed Base $1.02M plan 2027)
- **Churn** (de logos y de revenue) *(riesgo explícito del plan: "blindaje 2027")*.
- **Expansion revenue** (upsell / cross-sell en la base instalada).
- **Health score** de cuenta (uso, retrabajos, rentabilidad del cliente).
- **NPS / CSAT** como *leading indicators* de retención. **Baseline medido (Retently, ago-26):** NPS global **−27.8** (n=808); CSAT de soporte **4.67/5** (n=81). Ver `07-discovery`.

### Monetización
- **ACV**, estructura de **pricing** (por licencia).
- **Monetización de MAIA** — modelo aún no definido (beta).

## Nivel 3 — Métricas de producto (drivers)

> _Mayormente inferidas de `01` y `03`. Las que tienen **baseline** vienen medidas de Retently (`07`); el resto sigue como hipótesis a confirmar._

### 3.a — Satisfacción por rol (medida — baseline ago-2026)

Único bloque con datos reales hoy. Los **heavy users** son los peor rankeados, y ahí es donde la métrica debería moverse:

| Rol | NPS | n |
|---|---:|---:|
| Freelancer | +17.9 | 39 |
| Director | −11.7 | 77 |
| C-level | −11.9 | 42 |
| Colaborador | −29.0 | 390 |
| Cliente | −33.3 | 12 |
| **Project Manager** | **−40.7** | 248 |

- **NPS de heavy users (PM + Colaborador):** **−33.5** — candidata a métrica de seguimiento propia, por ser el 79% del volumen.
- **Delta onboarding → adopción:** hoy **negativo en Colaborador** (−15.2 → −34.5). Un producto sano debería mejorar con el uso; sirve como métrica de "el producto no desgasta".

### 3.b — Calidad de servicio (drivers de los dolores medidos)

> _Sugeridas a partir de los topics negativos dominantes (`07`): performance 95% neg, bugs 100% neg, mobile 96% neg. Confirmar si se trackean hoy._

- **Performance:** tiempos de carga (p50/p95), tasa de errores, disponibilidad/caídas.
- **Calidad:** bugs reportados y reabiertos, tickets por cuenta.
- **Mobile:** crash rate, uso mobile vs. web, satisfacción mobile.
- **Notificaciones:** ratio de notificaciones accionadas vs. ignoradas (señal/ruido).

### 3.c — Adopción y valor

**Engagement (medido — baseline ago-2026, fuente: Amplitude, evento "Any Active Event"):**

| Métrica | Valor | Detalle |
|---|---:|---|
| **DAU** (promedio días hábiles, jul-2026) | **~7.790** | Cae a ~670 en fin de semana — coherente con un producto B2B de uso en días hábiles. |
| **WAU** | **~11.000–11.900**, estable desde feb-2026 | Última semana completa (03-ago-2026): 11.879. |
| **MAU** | **13.048–14.484** | Pico en jul-2026 (14.484); ago-2026 parcial (13.048, mes en curso). |
| **Stickiness DAU/MAU** (jul-2026, DAU promedio días hábiles) | **~54%** | Alto para un producto B2B — indica uso recurrente, no esporádico. |
| **Stickiness WAU/MAU** (jul-2026) | **~79%** | La mayoría de los usuarios mensuales vuelve semana a semana. |

> _Nota: son valores agregados de toda la base ("All Users"), no cortados por rol/heavy user todavía — sería valioso cruzarlos con `03-personas` (Colaborador + PM) para ver si el engagement de los heavy users es distinto al agregado._

**Pendiente de cargar (compartido por el owner, en camino):** cobertura y precisión del time tracking, uso de features clave.

- **Activación / onboarding:** time-to-value, % de cuentas que llegan al "aha" (ej. primer proyecto con horas cargadas). _(hipótesis, sin baseline)_
- **Cobertura y precisión del time tracking:** % de horas esperadas efectivamente cargadas, y a tiempo (dato base de toda la rentabilidad). _Prioritaria: `07` (I-05) reporta horas que no computan o se pierden — riesgo directo sobre la confiabilidad del dato de rentabilidad._ _(pendiente — el owner va a compartir el dato)_
- **Uso de features de valor:** rentabilidad en tiempo real, Planner/capacity, dashboards por rol, portal de cliente. _(hipótesis, sin baseline — pendiente)_
- **Adopción por vertical** (a medida que se abren): activación y uso fuera del core de agencias. _(hipótesis, sin baseline)_

## Métricas de la vertical de AI — "Deploy de AI en clientes" (medida — baseline ago-2026; fuentes: Amplitude + Metabase, ver la convención de fuentes)

> **Reescrita el 2026-08-17** a partir de *MAIA — Análisis de adopción y penetración v3.0* (Producto, 2026-08-15). Reemplaza el baseline anterior, que estaba construido sobre conteos absolutos sin denominador. Dos afirmaciones de esa versión quedaron **dadas de baja** — ver el final de la sección.
>
> **Ampliada el 2026-08-18** con **Marketplace (agentes custom)**, que hasta ahora no estaba medido en este archivo.

### La vertical de AI es un portafolio de features — hoy hay tres medidas y dos denominadores

> _Confirmado por el owner el 2026-08-18: la vertical de AI es el conjunto de features con AI en las que COR apuesta. **MAIA es un miembro, no la vertical.** El "al menos dos" dejó de ser una sospecha inferida de los datos y pasó a ser la definición declarada. Ficha por feature en `01-producto`._

Todo lo que sigue se organiza en **dos bloques hermanos con denominadores distintos**. Confundirlos es el mismo error de denominador que produjo `[BAJA-01]`.

| | **MAIA** | **Marketplace (agentes custom)** |
|---|---|---|
| Qué es | Capa de orquestación, punto de entrada único | Agentes que la empresa arma a medida, elegidos a mano del selector |
| Feature Access | El único de MAIA | "Marketplace" + "Marketplace Maiaker" (dos, independientes) |
| Base habilitada | **128 companies** (13-ago-26) | **57 companies** (18-ago-26) |
| Universo de roles | PM + Director + C-Level (Colaborador excluido por scope) | Los cuatro: C-Level, Director, PM y Colaborador tienen Ver de fábrica |
| `agent_type` | `orchestrator`, `clone` | `custom` |

**Las dos penetraciones no son sumables ni directamente comparables.** No son la misma base ni el mismo universo de roles.

> ➕ **Risk Management es la tercera feature medida, y no es un tercer bloque** _(2026-08-18, corregido el 2026-08-19)_. Tiene Feature Access propio pero **exige además el de Chat de MAIA**, así que **se mide adentro del bloque de MAIA con corte propio por origen** (`option = risk_banner`). Sus usuarios **son un subconjunto de los de MAIA, no un sumando**.
> ⚠️ **Pero el denominador NO es el mismo.** Esta nota decía "corre sobre la misma base de 128 companies". El export de altas del 19-ago-26 muestra **119 companies y 3.444 asientos**, con fechas de alta propias. **Su penetración usa denominador propio y hoy está ⏸️ en pausa** — ver el bloque de Risk Management más abajo.

### Cómo etiquetamos la evidencia de esta sección

> _Convención local de la sección de AI. Cada afirmación lleva su estado **inline, pegado al claim** — no en nota al pie, para que nadie la cite sin la etiqueta._

**Los cinco tests.** **Denominador:** ¿está normalizado por la base que corresponde? · **Instrumentación:** ¿el evento mide lo que el claim dice que mide? · **n y cola:** ¿cuántas observaciones lo sostienen, y depende de la cola fina? · **Confounder:** ¿hay una explicación alternativa viva? · **Replicación:** ¿se sostiene por dos cortes independientes?

| Estado | Requisito | Para qué sirve |
|---|---|---|
| `[HECHO]` | Pasa los cinco tests | Puede sostener un KR o un reparto de capacidad |
| `[HALLAZGO]` | Pasa denominador, instrumentación y replicación; la magnitud es frágil | Prioriza, no fija meta. Se cita con rango o con "aprox." |
| `[HIPÓTESIS]` | Confounder abierto, o la interpretación excede al dato | Orienta discovery. Declara en una línea **qué la refutaría** |
| `[BAJA]` | Se daba por bueno y se cayó | Se registra con fecha y motivo. No se borra |

**Regla de separación.** La observación y su interpretación se clasifican por separado. "El C-Level lleva cinco meses en meseta" y "el C-Level está saturado" no son el mismo claim.

**Regla de carga.** La barra escala con lo que el claim sostiene. Reparto de capacidad del squad y KRs exigen `[HECHO]`; priorizar una entrevista se conforma con `[HIPÓTESIS]`.

### Convención de fuentes — son tres, no dos

> _Cargada el 2026-08-18 con el análisis de Risk Management. **Aplica a toda la sección de AI**, no solo a esa feature. Mezclar las tres fuentes es el error más fácil de cometer con estos datos: produce números que parecen tasas de conversión y no lo son._

| Fuente | Qué es | Para qué sirve | Qué **no** puede responder |
|---|---|---|---|
| **Amplitude** (eventos `AI_CHAT_*`, con sus `option` / `agent_type`) | Evento de front al interactuar | **Alcance y penetración**: usuarios únicos, interacciones, corte por rol y por origen | Qué respondió el producto, ni si la respuesta sirvió |
| **Log de conversaciones (Metabase)** — para Risk Management, **Q21883** | La conversación con la respuesta efectivamente generada | **Calidad y contenido**: qué se consultó, qué se respondió, si hubo repregunta | Alcance — no trae denominador de asientos |
| **Backend de cálculo (Metabase)** — para Risk Management, **Q21879** | El motor que detecta desvíos y dispara la señal | **Detección y calibración de umbrales** | Alcance (no hay usuario) ni calidad (no hay respuesta) |

_Cada bloque de métricas declara la **ventana temporal** de sus tres cortes: no coinciden entre sí, y esa es una de las razones por las que no se dividen._

**Las ocho reglas de lectura** _(1 a 7 confirmadas con el owner el 2026-08-18; la 8 se sumó el 2026-08-18 tras detectar el mismo agujero en dos features)_:

1. **Amplitude para alcance y penetración.** Usuarios únicos sobre denominador de asientos elegibles.
2. **El log para calidad y contenido.** Engagement por tipo, texto de las respuestas, repregunta.
3. **El backend de detección para umbrales.** Nunca para alcance ni para calidad.
4. **No dividir una fuente por otra.** Nada de tasas detección→click: unidades y ventanas distintas. **La asimetría entre lo que se detecta y lo que se consulta se lee comparando rankings, no dividiendo.**
5. **La unidad de detección es el `proyecto`, no la `vez`.** Cada proyecto redispara la misma métrica 7 a 9 veces, consistente con un cálculo on-demand en cada apertura del dashboard. `Veces` mide aperturas, no incidentes.
6. **La unidad de consulta es la consulta distinta, no la fila del log.** En Risk Management el 33,4% de las filas es el mismo usuario repitiendo la misma pregunta sobre el mismo proyecto (58% de esas repeticiones dentro de la hora: reclick que regenera la respuesta). Sin deduplicar, el volumen queda inflado ~25%.
7. **Los funnels de Amplitude son a nivel usuario, no a nivel evento.** Amplitude deduplica — se ve en que las filas diarias del funnel de Risk Management suman 182 y el total marca 141. Por eso el 46,8% de abrir→enviar significa "de los usuarios que abrieron, cuántos enviaron al menos un mensaje", **no** "de cada click, cuántos generan mensaje".
8. **Toda serie declara evento, filtro y valores incluidos.** No alcanza con nombrar el evento. Si la consulta restringe por `option`, `agent_type` o cualquier otra propiedad, **el filtro va escrito junto a la serie**. Una serie sin filtro documentado **no es reproducible**: quien la re-pullee va a traer otro número sin manera de darse cuenta. _Cargada el 2026-08-18 después de que el mismo problema apareciera dos veces — el filtro de `AI_CHAT_OPEN` acá, y el 🔴 abierto de Marketplace sobre si la serie de MAIA se pulleó con o sin filtro `agent_type`._

### Definiciones

Sin estas tres definiciones los números de abajo no se pueden leer, y su ausencia es lo que produjo las dos bajas del final.

- **Asiento elegible.** Suma de asientos de **PM + Director + C-Level** de las companies con MAIA habilitada al inicio del mes. Al 13-ago-2026: **3.775 asientos en 128 companies**.
- **Penetración.** Usuarios únicos ÷ asientos elegibles, en el mismo período. **Es la métrica principal de la vertical de AI.** Reemplaza el conteo de usuarios únicos absolutos.
- **Intensidad.** Interacciones ÷ usuarios únicos.
- **Usuario único / interacción.** Métricas `Uniques` y `Totals` de Amplitude sobre el `OR` de cuatro eventos: `AI_CHAT_SEND` (con `agent_type` en orquestador / clone), `AI_CHAT_SELECT_FAQ`, `AI_CHAT_OPEN` **restringido a los valores de `option` que representan conversión** (`risk_banner` y equivalentes) y `AI_CHAT_SUGGESTED_ANSWER`. Se deduplica **dentro** de cada mes, no entre meses: las columnas mensuales **no son sumables**. La vara es una sola interacción.

  > 🔒 **Filtro obligatorio — sin esto la serie no se reproduce.** `AI_CHAT_OPEN` dispara también con `option = header` (abrir el chat sin enviar nada). **Esos eventos están excluidos de toda esta sección.** Quien re-pullee la serie sin el filtro va a obtener números más altos y no comparables. _(Regla 8 de la convención de fuentes.)_
  >
  > **Los cuatro eventos son conversación con respuesta generada** _(aclarado con el owner, 2026-08-18)_. FAQ y banner **no son "abrir el panel"**: construyen un custom prompt por detrás, lo envían y MAIA responde. La respuesta sugerida continúa una conversación en curso. **Ninguno de los cuatro es una apertura vacía.**
  >
  > | Evento | Qué representa | Quién formula la consulta |
  > |---|---|---|
  > | `AI_CHAT_SEND` | El usuario escribe y envía una consulta | **El usuario**, con sus palabras |
  > | `AI_CHAT_SELECT_FAQ` | Click en consulta frecuente → custom prompt e inicia conversación | COR (prompt prearmado) |
  > | `AI_CHAT_OPEN` (`option = risk_banner`) | Click en "Resolver con MAIA" → custom prompt con el contexto del riesgo | COR (prompt prearmado + contexto inyectado) |
  > | `AI_CHAT_SUGGESTED_ANSWER` | Click en respuesta sugerida → continúa la conversación | COR (continuación sugerida por MAIA) |
  >
  > **Pero no miden lo mismo, y por eso el KR necesita cortarlos.** `AI_CHAT_SEND` mide **demanda articulada por el usuario** — alguien tuvo una pregunta y la escribió. Los otros tres miden **demanda inducida por rieles que construimos nosotros**. Las dos cosas son valiosas y ninguna es falsa, pero responden preguntas de producto distintas: la primera dice si MAIA resuelve una necesidad propia del usuario, la segunda si nuestras superficies de entrada funcionan. **Un número que las suma no deja ver cuál de las dos se movió.** Vale igual para la intensidad: un 6,2 hecho de seis preguntas escritas no significa lo mismo que uno hecho de seis clicks en respuestas sugeridas.

**Base habilitada:** **128 companies** al 13-ago-2026 (~43% de los +300 clientes de COR), por habilitación progresiva a beta testers desde jul-2025. La habilitación sigue abierta y hay una decisión pendiente sobre liberar a toda la base.

> ⚠️ **Incomparabilidad con el baseline anterior de este archivo.** Todos los números de esta sección excluyen al rol **Colaborador**; los de la versión anterior lo incluían. Julio-26 es **373 usuarios / 2.303 interacciones** acá contra 413 / 2.463 antes. **MAIA no empeoró — cambió el denominador y el universo de roles.** El Colaborador se excluye porque **su propuesta de valor no está definida**, y porque el owner decidió mantenerlo fuera de esta medición _(ago-2026)_. **Ojo con el fundamento:** la documentación funcional del Orquestador (22-jul-26) le da acceso a MAIA desde el **header** y **desde dentro de una tarea**, así que el argumento de "alcance marginal" ya no se sostiene solo. **Es una decisión de scope del análisis, no una limitación del dato.** Si se decide incorporarlo, son 5.605 asientos contra los 3.775 elegibles actuales: el denominador de toda esta sección cambia de escala. Única excepción: la tabla de distribución de frecuencia, que Amplitude no entrega abierta por rol.

### Penetración — serie mensual

| Mes | Cuentas | Asientos elegibles | Usuarios | **Penetración** | Interacciones | Intensidad |
|---|---:|---:|---:|---:|---:|---:|
| Nov 25 | 32 | 852 | 32 | 3,8% | 122 | 3,8 |
| Dic 25 | 34 | 900 | 13 | 1,4% | 52 | 4,0 |
| Ene 26 | 34 | 900 | 22 | 2,4% | 113 | 5,1 |
| Feb 26 | 39 | 991 | 28 | 2,8% | 136 | 4,9 |
| Mar 26 | 41 | 1.004 | 69 | 6,9% | 318 | 4,6 |
| Abr 26 | 64 | 1.659 | 104 | 6,3% | 625 | 6,0 |
| May 26 | 95 | 2.703 | 219 | 8,1% | 1.329 | 6,1 |
| Jun 26 | 98 | 2.820 | 323 | 11,5% | 1.579 | 4,9 |
| **Jul 26** | **104** | **3.225** | **373** | **11,6%** | **2.303** | **6,2** |
| Ago 26 (parcial, 13 días) | 119 | 3.560 | 214 | 6,0% | 1.422 | 6,6 |

_Criterio de corte: asientos habilitados al **inicio** de cada mes — una cuenta dada de alta el día 20 recién computa el mes siguiente. Es deliberadamente conservador con las altas recientes._

> 📌 **Marca de release en la serie: el Orquestador se deployó el 22-jul-2026** (→ `01-producto`). Julio queda partido (21 días sin, 9 con) y **no sirve como corte**; agosto es el primer mes limpio. Quien lea el número de agosto sin esto no puede interpretarlo. El test de la hipótesis capacidad vs. superficie que se apoya en este corte vive en `08-roadmap`.

**Baseline oficial jul-26: penetración 11,6%** `[HECHO]`.
_Corregido el 2026-08-18. La salvedad anterior decía que el numerador incluía aperturas de panel sin escribir y concluía que el signo neto del sesgo era desconocido. **Las dos cosas eran incorrectas:** los cuatro eventos son conversación con respuesta generada, y las aperturas por `header` nunca estuvieron en la serie. **El numerador está limpio.**_
_Queda un solo sesgo, y es de denominador: incluye cuentas que pueden haber churneado, lo que **deprime** la penetración. **Signo neto conocido: el 11,6% es un piso conservador.** El valor real es igual o mayor, y se acota con el pedido de estado de actividad/churn por company._
**→ La cifra ya se puede usar para fijar un KR.** Lo que falta no es recalibrarla, es **cortarla por origen** (ver anti-metas en `05-estrategia-okrs`).

**La penetración creció ~5x entre enero y julio mientras el denominador se multiplicaba por 3,6** `[HECHO]`. Cada tanda de altas entra con penetración baja y arrastra el promedio hacia abajo; que el indicador suba igual descarta que el crecimiento sea efecto de composición.
_Replicación: panel cerrado de las 34 companies con alta en 2025, denominador constante de 900 asientos, sin altas ni bajas — **1,8% en enero → 14,6% en julio**. Misma dirección y mayor magnitud, porque no incorpora cuentas nuevas de penetración baja._

> `[HIPÓTESIS]` **"…y por lo tanto la adopción responde a producto."** El panel fijo demuestra que el crecimiento es comportamiento y no composición, pero no aísla al producto de la actividad de CSM, del servicio de consultoría ni del boca a boca dentro de la cuenta.
> **Qué la refutaría:** que el crecimiento del panel fijo se concentre en las cuentas con CSM activo o con consultoría contratada.

### Penetración por rol

| Mes | PM | Director | C-Level |
|---|---:|---:|---:|
| Feb 26 | 1,8% | 2,6% | 7,1% |
| Mar 26 | 6,2% | 5,6% | 11,4% |
| Abr 26 | 5,1% | 6,2% | 10,5% |
| May 26 | 8,0% | 7,6% | 9,5% |
| Jun 26 | 11,9% | 11,5% | 9,6% |
| **Jul 26** | **11,5%** | **10,8%** | **13,3%** |
| Ago 26 (parcial) | 5,2% | 7,0% | 7,7% |

_Asientos jul-26: PM 1.917 · Director 850 · C-Level 458._

**Los tres roles adoptan a tasas equivalentes** `[HECHO]` — replica en mayo, junio y julio. La aparente dominancia del PM (56% de los usuarios, 51% de las interacciones) es un **efecto de tamaño de base**: hay 1.917 asientos de PM contra 458 de C-Level. **Ver `[BAJA-01]`.**

**El C-Level tiene la intensidad más alta de los tres roles: 8,2 interacciones por usuario** (acumulado nov-25 a ago-26) contra **5,2** de PM y de Director, que son indistinguibles entre sí `[HECHO]`. Concentra 18% de los usuarios y 25% de las interacciones, con índice de sobre-representación >1 en 8 de los últimos 9 meses.
_Salvedad de n: el C-Level son ~25 usuarios por mes con volatilidad de 3,4 a 11,9 int./usuario. El acumulado de 8,2 es confiable; los meses individuales no._

**El C-Level lleva cinco meses en meseta** (entre 9,5% y 13,3% desde marzo) mientras PM y Director siguen en curva ascendente `[HECHO]`.

> `[HIPÓTESIS]` **"…porque el C-Level está saturado."** La meseta está medida; la saturación es una interpretación, y compite con dos explicaciones vivas: **sesgo de selección** (los C-levels fueron los interlocutores de la conversación del beta, así que adoptaron primero por acceso y no por ajuste) y **ausencia de valor específico para el rol**. Además "saturado" en 13,3% implica que 87% de los C-levels no toca MAIA en el mes, que es un techo natural fuerte de asumir.
> **Qué la refutaría:** que un release orientado a C-Level mueva su penetración por encima del 13,3%.
> ⚠️ **Peso de la decisión: alto** — de esto depende si se invierte o no en valor para el rol. **No usar como `[HECHO]` para repartir capacidad.**

### Forma de la distribución — usuarios por cantidad de interacciones en el mes

| Mes | 1 | 2-5 | 6-10 | 11-20 | 21-50 | 51-100 | +100 | Total |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Nov 25 | 12 | 14 | 4 | 1 | 1 | 0 | 0 | 32 |
| Dic 25 | 5 | 5 | 2 | 1 | 0 | 0 | 0 | 13 |
| Ene 26 | 7 | 10 | 2 | 2 | 1 | 0 | 0 | 22 |
| Feb 26 | 13 | 8 | 2 | 4 | 1 | 0 | 0 | 28 |
| Mar 26 | 22 | 31 | 11 | 3 | 2 | 0 | 0 | 69 |
| Abr 26 | 44 | 39 | 9 | 6 | 4 | **2** | 0 | 104 |
| May 26 | 84 | 100 | 18 | 6 | 6 | 3 | 0 | 219 |
| Jun 26 | 130 | 130 | 35 | 14 | 14 | 2 | 0 | 325 |
| Jul 26 | 148 | 168 | 40 | 31 | 20 | 6 | 0 | 413 |
| Ago 26 (parcial) | 74 | 96 | 38 | 19 | 13 | 3 | 0 | 243 |

_Única tabla de la sección que incluye al rol Colaborador (Amplitude no entrega el histograma abierto por rol). Buckets nativos de Amplitude salvo `2-5` y `+100`, que son agregaciones propias. **Validación:** el total de cada histograma coincide exactamente con los usuarios únicos del agregado mensual, en los diez meses._

**La forma de la base es estable** `[HECHO]`: el bucket de 1 interacción oscila entre 30% y 46% sin tendencia, y el de 2-5 entre 38% y 46% durante los diez meses. Lo que se mueve es la cola alta.

**El bucket 51-100 no existía antes de abril-2026** — cero usuarios durante cinco meses consecutivos `[HECHO]`.

**Concentración del volumen (jul-26):** los ~26 usuarios de los buckets 21-50 y 51-100 son el **6% de la base activa y generan ~43% de las interacciones**; los 148 usuarios de una sola interacción son el 36% de la base y aportan ~5% `[HALLAZGO]`.
_Es una estimación, no una medición: Amplitude entrega buckets, así que se multiplica la cantidad de usuarios de cada bucket por el punto medio de su rango (1 / 3,5 / 8 / 15,5 / 35,5 / 75,5). El total estimado de julio (2.699) sobreestima al real (2.463) en 10%. La concentración es robusta al error de estimación; las cifras exactas no — citar como "aprox."._
_Desplazamiento entre marzo y julio: el peso de los buckets 1-10 pasa de 65% a 39% del volumen y el de 11-100 de 35% a 61%._

> **Consecuencia de medición:** el volumen total de interacciones y el promedio de interacciones por usuario son **malas métricas de salud** — medir volumen equivale a medir a dos docenas de personas. **La métrica de salud de la base es la forma de la distribución, no el total ni el promedio.**

**Fuera del registro:** el "techo de uso individual de ~100 interacciones/mes" que aparece en el documento fuente **no entra**. Con un máximo de 413 usuarios activos mensuales y 6 personas en el bucket más alto, un bucket `>100` vacío es lo esperable por cola fina, no evidencia de un techo.

### Dispersión por cuenta

La penetración agregada esconde una dispersión muy grande entre cuentas, y ahí está la palanca más grande disponible sin construir producto.

| Cuenta | Alta | Asientos | Usuarios jul | Penetración | Int./usuario |
|---|---|---:|---:|---:|---:|
| TBWA Multisponsor | abr-26 | 102 | 4 | 3,9% | 2,2 |
| Ganem Group | jun-26 | 101 | 3 | 3,0% | 2,0 |
| Encender | abr-26 | 68 | 3 | 4,4% | 1,0 |
| Garnier Agency | abr-26 | 66 | 2 | 3,0% | 2,0 |
| Fahrenheit DDB | mar-26 | 64 | 2 | 3,1% | 2,0 |
| MASS DIGITAL | mar-26 | 50 | 1 | 2,0% | 2,0 |
| Anagram LATAM | mar-26 | 49 | 1 | 2,0% | 2,0 |
| DeNicolas | abr-26 | 43 | 2 | 4,7% | 1,0 |
| **Subtotal "dormidas"** | | **543** | **18** | **3,3%** | **~1,8** |
| **Crowe Global** *(contraste)* | jun-26 | 123 | 29 | **23,6%** | **8,7** |

**543 asientos —17% del universo elegible de julio— con 18 usuarios activos y una intensidad de 1 a 2,2** `[HALLAZGO]`. No son usuarios que usan poco: son personas que **probaron y no volvieron**. Llevar esos asientos al promedio de la base agregaría ~45 usuarios activos, sin construir nada.
_Por qué no es `[HECHO]`: el denominador no está depurado. El export de altas lista companies con MAIA habilitada, pero puede incluir cuentas churneadas o inactivas en COR en general. Si tres de estas ocho están dormidas a nivel plataforma, el asiento no existe y el problema no es de MAIA._
**→ Verificación obligatoria antes de dimensionar cualquier iniciativa sobre estos asientos: estado de actividad/churn por company. Es la verificación más barata de la lista y cambia el tamaño del premio.**

**Contraste:** Crowe Global se habilitó en jun-26, tiene escala comparable (123 asientos) y alta más reciente, y llegó a 23,6% de penetración con 8,7 interacciones por usuario. Misma escala, resultado opuesto. Entender qué pasó ahí es el insumo más valioso disponible para un playbook de activación (→ `07-discovery`).

**Cuentas sin ningún uso:** 15 companies (12% de la base, 149 asientos) no registraron un solo usuario activo en diez meses.

**Techo observado hoy:** las mejores cuentas superan el **23%** de penetración. Es la referencia disponible para fijar meta, no el 11,6% agregado.

### Cuentas de consultoría (el único revenue de MAIA)

MAIA es **gratuita para toda la base de beta testers**. El único revenue asociado proviene de un servicio de consultoría de AI ejecutado entre Producto y CSM, cobrado como extra por licencia sobre clientes que ya son de COR. No hay todavía casos de upsell de licencias por uso de MAIA fuera de ese marco.

| Cliente | Cuenta | Alta | Asientos | Usuarios jul | Penetración | Int./usuario |
|---|---|---|---:|---:|---:|---:|
| Sancho BBDO | GRUPO EXITO | jun-26 | 79 | 3 | 3,8% | **20,3** |
| Sancho BBDO | SODIMAC | jun-26 | 68 | 1 | 1,5% | **10,0** |
| Publicis | Publicis Impetu Uruguay | mar-26 | 49 | 10 | 20,4% | 8,3 |
| Robin | robin agency | may-26 | 71 | 10 | 14,1% | 4,8 |

_Referencia jul-26: penetración 11,6%, intensidad 6,2._

> `[HIPÓTESIS]` **La consultoría produce profundidad, no alcance.** Las dos cuentas de Sancho tienen penetración muy baja y la intensidad más alta de toda la base — son las únicas cuentas de baja penetración cuyos usuarios están muy por encima del promedio (las ocho dormidas tienen usuarios de 1 a 2 interacciones; acá hay de 10 y 20). Publicis y Robin muestran un perfil intermedio.
> **Consecuencia de negocio si se sostiene:** si el upsell se cotiza **por licencia** y el uso se concentra en 1 a 3 personas, el valor entregado y el precio cobrado se apoyan sobre bases distintas (→ `05-estrategia-okrs`, `08-roadmap`).
> **Qué la refutaría:** que las cuentas de consultoría alcancen penetración por encima del promedio a medida que madura el servicio. **n = 4 cuentas.**

### Calidad percibida — no medible hoy

| Acción | Total nov-25 a ago-26 |
|---|---:|
| Thumbs up | 79 |
| Thumbs down | 9 |
| Copiar respuesta | 33 |
| **Total feedback explícito** | **121** |

**Sobre ~8.200 interacciones, la tasa de feedback explícito es del 1,5%** `[HECHO]`. **No hay base para construir un KR de calidad percibida.** El ratio 9:1 a favor no indica que MAIA sea buena: indica que **casi solo califica quien está conforme**. Además "copiar respuesta" viene bajando en términos absolutos (7 eventos en nov-25 contra 1-4 mensuales en 2026) mientras las interacciones se multiplicaban por veinte.
_Salvedad técnica: el filtro actual captura solo `agent_type` = clone u orchestrator. Si existen otros tipos de agente, quedan fuera de la medición._
**→ Ver `[BAJA-02]`. Medir calidad requiere instrumentar otra cosa.**

### El límite de toda esta sección

**Todo lo que se mide acá es uso: cuánta gente, cuántas veces, con qué frecuencia. Ninguna métrica de esta sección dice si MAIA sirve.** No hay forma de saber, con los datos disponibles, si una interacción cambió una decisión operativa, evitó un desvío o protegió un margen. La tasa de feedback del 1,5% tampoco alcanza como proxy.

La brecha es **más grave para las otras features del portafolio de AI que para MAIA**. Un chat puede evaluarse razonablemente por frecuencia de uso; un workflow automatizado o una alerta de risk management, no — su valor está en el trabajo que ejecutan, y ese trabajo hoy no se registra como evento.

> ✏️ **Corregido el 2026-08-18, dos veces.** Este bloque afirmaba que "ninguna métrica actual captura la vertical de AI fuera de MAIA". **Era falso para Marketplace**, que tiene serie de diez meses con denominador propio, y desde este mismo día también para **Risk Management**, que tiene baseline de alcance y de engagement por tipo de riesgo (ver sus secciones). Sigue siendo cierto para **workflows/automatizaciones**, para la **creación** de agentes custom y —crucialmente— para el **valor entregado** de todas ellas.
>
> 📊 **Risk Management es hoy el mejor lugar del producto para instrumentar valor entregado.** Ofrece **acciones masivas reales** desde la respuesta (asignar colaboradores, mover deadlines, reasignar tareas) y **no existe ningún evento que registre si alguien las aplica**. Es un caso más limpio que la aprobación de Governance porque la acción está pegada a un desvío concreto y medible. Pedido cargado abajo.

**El candidato más directo para empezar a medir valor entregado:** el Pilar 3 de MAIA (Governance, `01-producto`) exige **aprobación explícita del usuario para cada acción crítica**. Ese evento existe en el producto y **no se está registrando como métrica**.

### Métricas oficiales candidatas para "Deploy de AI en clientes"

Reemplaza la lista anterior, que se apoyaba en conteos absolutos.

| Candidata | Estado | Nota |
|---|---|---|
| **Penetración por rol** sobre asientos elegibles | Con baseline | Métrica principal. **Meta diferenciada por rol** — no una sola meta para los tres |
| **Forma de la distribución** (share de los buckets 11+) | Con baseline | Reemplaza volumen total y promedio de interacciones |
| **Penetración por cuenta / dispersión** | Con baseline | Habilita meta de activación de cuentas, no solo de usuarios |
| **Penetración con corte por origen** (banner vs. resto) | Con baseline | **Obligatoria, no opcional:** el 63% de los usuarios de MAIA de jul-26 entra por banner de riesgo. Sin este corte, el KR agregado es ilegible |
| **Eventos de aprobación de acciones** (Governance) | No instrumentado | Candidato a medir **valor entregado** en lugar de actividad |
| **Acción aplicada desde una respuesta de riesgo** | No instrumentado | El otro candidato a **valor entregado**, y el más limpio: la acción está pegada a un desvío concreto |
| ~~Usuarios únicos activos/mes~~ | Degradada | Se mueve con el denominador; sirve de diagnóstico, no de meta |
| ~~Volumen de interacciones~~ | Descartada | Mide a ~26 personas |
| ~~% de power users vs. uso único~~ | Reformulada | Absorbida por "forma de la distribución" |
| ~~Calidad percibida (thumbs)~~ | Descartada | Tasa de feedback 1,5%. Ver `[BAJA-02]` |

### Risk Management — baseline nuevo (2026-08-18)

> _Primera medición de esta feature en el repo. **Vive acá adentro, no como bloque hermano**: Risk Management tiene Feature Access propio pero exige además el de "Chat de MAIA" y corre sobre un **subconjunto** de la base de MAIA, así que se mide **dentro de MAIA con corte propio por origen** (`AI_CHAT_OPEN` con `option = risk_banner`). Resolución completa en `01-producto`._
>
> **Tres fuentes, leídas según la convención de arriba:** Amplitude (5 cortes de `AI_CHAT_OPEN` / `option = risk_banner`, feb-26 → 18-ago-26) · **log de conversaciones** (14-may → 13-ago-26: 653 filas, **523 consultas distintas**, 348 usuarios, 73 companies) · **backend de detección** (422.897 detecciones, 11 `metric_key`, ⚠️ **ventana temporal a confirmar**) · **export de altas del Feature Access** (19-ago-26: 119 companies con fecha de alta, segmento y asientos por rol).

#### La base propia — 119 companies, no 128 `[HECHO — 2026-08-19]`

> _Cargado con el export "Desglose de roles por empresa" (19-ago-2026). **Es la primera vez que el repo tiene la fecha de habilitación de esta feature**, y cambia varias lecturas del bloque._

| Mes | Companies al inicio | Asientos elegibles al inicio |
|---|---:|---:|
| May-26 | 0 | 0 |
| Jun-26 | 15 | 580 |
| Jul-26 | 32 | 1.747 |
| Ago-26 | 111 | 3.230 |
| _Total al 19-ago-26_ | _119_ | _3.444_ |

**Primera alta: 14-may-2026.** El rollout está **concentrado**: **79 de las 119 companies (66%) se habilitaron en julio, y 55 el mismo día — el 8-jul-2026.** Ese único día es el 46% de la base.

_Verificación de consistencia: **3.444 asientos elegibles en 119 companies** contra 3.775 en 128 de MAIA. **Compatible con que Risk Management sea un subconjunto de MAIA**, que es lo que este archivo asume._

> 📌 **Trazabilidad del export.** La primera versión traía las **columnas de rol mal etiquetadas**. Se usó la **versión corregida**: los 119 IDs, las fechas de alta y los segmentos son idénticos entre ambas, solo cambiaron los conteos por rol. **Si aparece una versión con 4.955 PMs y 2.043 Colaboradores, es la incorrecta.** Con el archivo mal etiquetado la verificación de subconjunto no cerraba.

#### Definiciones y baseline

**Penetración de Risk Management, jul-26: ⏸️ EN PAUSA** `[SIN VALOR PUBLICABLE]`

_Puesta en pausa el 2026-08-19, con el export de fechas de alta del Feature Access. **El 7,3% que estuvo cargado se calculó sobre 3.225 asientos, que es el denominador de MAIA, no el propio de Risk Management.**_

**Los tres cálculos posibles y por qué ninguno sirve:**

| Criterio | Denominador jul-26 | Resultado |
|---|---:|---:|
| Base de MAIA (el usado hasta hoy) | 3.225 | 7,3% |
| Base propia, "habilitadas en cualquier momento del mes" | 3.230 | 7,2% |
| Base propia, **"asientos al inicio del mes"** — la convención declarada de este archivo | **1.747** | **13,4%** |

> ⚠️ **El 7,3% daba bien por coincidencia.** Los 3.225 asientos de MAIA y los 3.230 de Risk Management son casi idénticos por azar. Quien re-corra el cálculo con la base propia y la convención declarada va a obtener **13,4%** y no va a entender la diferencia.
>
> ⚠️ **El 13,4% tampoco es correcto.** Al 1-jul había 32 companies habilitadas, pero **el 8-jul entraron 55 más**. Los 234 usuarios de julio **incluyen gente de cuentas que el denominador de 1.747 excluye**: numerador de hasta 111 companies sobre denominador de 32. **Es un techo, no una medición** — restringir el numerador solo puede bajarlo.
>
> **El valor real está acotado entre 7,2% y 13,4%.** El cálculo correcto es barato: **usuarios únicos de julio restringidos a las 32 companies habilitadas antes del 1-jul.** Es un filtro por lista de IDs sobre una consulta que ya existe. **Hasta tenerlo, no publicar ninguna cifra de penetración de esta feature.** 🔴 Pedido cargado abajo.

> 📌 **Cuestión de convención que esto abre.** El criterio "asientos al inicio del mes" está diseñado para un rollout gradual como el de MAIA. Para una feature donde el **46% de la base entra un solo día a mitad de mes**, produce el desfasaje de arriba. **Evaluar si Risk Management necesita un criterio propio, documentado como excepción.**

> ✏️ **Lo que sí se corrigió y no vuelve:** la salvedad anterior decía que el 7,3% era provisorio "por el mismo problema de instrumentación que el 11,6% de MAIA". **Ese motivo se retira** (2026-08-18): `AI_CHAT_OPEN` con `option = risk_banner` **es un evento de conversión** —dispara un custom prompt con el contexto del riesgo y MAIA responde—, no una apertura de panel vacía. El numerador nunca estuvo sucio. **El motivo de la pausa es de denominador, no de instrumentación.**

**Serie de alcance** `[HECHO]`

| | May 26 | Jun 26 | Jul 26 | Ago 26 (1-18) |
|---|---:|---:|---:|---:|
| Interacciones | 246 | 506 | 479 | 133 |
| Usuarios únicos | 119 | 232 | 234 | 71 |
| Intensidad (int./usuario) | 2,07 | 2,18 | 2,05 | 1,87 |

Crecimiento may→jun, **usuarios planos jun→jul**, caída en agosto.
_Nota metodológica: extrapolar los 71 únicos de agosto a mes completo **sobreestima**, porque los usuarios únicos no escalan linealmente con los días. La caída real es probablemente mayor que la que sugiere la regla de tres._

> ⚠️ **"Meseta" era una lectura equivocada, y la corrección va en la dirección mala** `[HECHO — 2026-08-19]`. El conteo de usuarios se mantuvo plano **mientras la base habilitada se multiplicaba por 3,5**:
>
> | | Jun-26 | Jul-26 |
> |---|---:|---:|
> | Companies habilitadas al inicio | 15 | 32 |
> | Companies habilitadas al cierre | 32 | **111** |
> | Usuarios únicos | 232 | **234** |
>
> **Las 79 companies habilitadas en julio —incluidas las 55 del 8-jul— aportaron cero usuarios netos.** O no las usó nadie, o las usó gente que compensó exactamente una caída equivalente en la cohorte previa. **En cualquiera de los dos casos la penetración se desplomó**, y agosto (71 usuarios en 18 días sobre 111-119 companies) no revierte la dirección.
>
> **Esto no depende de ningún corte pendiente.** Es aritmética sobre datos que ya están en el repo. Y es un problema de **activación de cuentas nuevas**, no de retención de usuarios individuales — dos cosas que este bloque venía confundiendo. → `07-discovery`, `08-roadmap`.

**La intensidad es plana en ~2,0** `[HECHO]` — muy por debajo de la de MAIA en general (5,2 a 8,2 según rol). Es una feature de contacto corto.

**Retención: 59% de los 348 usuarios del log hizo una sola consulta en tres meses, y el 83% aparece en un solo mes** `[HECHO — no interpretable como no-retorno]`.

> ⚠️ **Corrección del 2026-08-19.** Estos porcentajes **no controlan por fecha de alta**, y el rollout está concentrado al final de la ventana de medición:
>
> | Cohorte de alta | Companies | Meses observables (may–ago) |
> |---|---:|---:|
> | May-26 | 15 | 4 |
> | Jun-26 | 17 | 3 |
> | **Jul-26** | **79** | **2** |
> | Ago-26 | 8 | 1 |
>
> **Solo 15 companies tuvieron los cuatro meses disponibles.** Una cuenta habilitada el 8-jul **no puede** aparecer en más de dos meses: el 83% mide en buena parte eso.
>
> **Cae también el corolario a nivel cuenta.** La afirmación de que "57 companies (45% de la base) tocaron un banner solo en julio" describe casi exactamente a las **55 companies habilitadas el 8-jul**, que antes no existían. **Retirar como evidencia de no-retorno.**
>
> **Lo que sí se puede medir:** retención en **meses desde la habilitación**, no en meses del calendario, y sobre la **cohorte de mayo (15 companies)**, la única con ventana completa. Si el no-retorno sobrevive ahí, es un hallazgo mucho más fuerte que el actual.

**Conversión de usuario abrir→enviar: 46,8%** (141 usuarios → 66), con mediana de 40 segundos. Últimos 30 días al 18-ago `[HECHO]`.
Mide **cuántos de los que llegan por banner siguen escribiendo con sus propias palabras** — o sea, cuánta demanda inducida se convierte en demanda articulada.
> ⚠️ **No presentar este 46,8% en la misma frase que la continuidad del log.** Son fuentes distintas y ventanas distintas (regla 4).

**Continuidad de conversación (log): 31,4% global** `[HECHO]`. Por mes: **4,8% (may) → 24,9% (jun) → 39,4% (jul) → 42,6% (ago)**.
> ⚠️ _La serie **mezcla poblaciones**: mayo son 15 companies beta, agosto son 119. **No se puede distinguir "el producto mejoró" de "cambió la composición".** Replicar sobre **panel cerrado de la cohorte de mayo** antes de sostener que mejora — igual que se hizo con MAIA en el panel de cuentas 2025._

#### Engagement por tipo de riesgo (log)

_Baseline de comparación: 31,4% de continuidad y 0,77 mensajes promedio después del análisis._

| Riesgo | n | % sigue | msgs prom. | msgs si sigue |
|---|---:|---:|---:|---:|
| Horas estimadas vs. cargadas (tarea) | 72 | **38,9%** | 0,90 | 2,32 |
| Fecha de finalización (proyecto) | 12 | 33,3% | 1,17 | **3,50** |
| Retrabajo | 34 | 32,4% | 0,53 | 1,64 |
| Tareas sin colaboradores | 266 | 31,6% | 0,85 | 2,69 |
| Tareas vencidas | 150 | 30,7% | 0,67 | 2,20 |
| Costo vs. ingresos | 8 | 12,5% | 0,25 | 2,00 |
| Horas cargadas vs. planificadas (tarea) | 11 | 9,1% | 0,45 | 5,00 |
| Tareas sin finalizar con retrabajo | 4 | 0% | 0 | — |

**Volumen y engagement no correlacionan** `[HECHO]`. Los **dos** riesgos que concentran el 91% de las consultas desde julio (tareas sin colaboradores 51% + tareas vencidas 40%; con retrabajo 8% los tres llegan al 99%) están **en o por debajo** del baseline de continuidad. El que mejor convierte tiene volumen medio.

**Cuando hay conversación, dura 2 a 3 mensajes** `[HECHO]`. Es repregunta y cierre, no diálogo. Consistente con que el **60,6% de las respuestas trae `suggest_reply`**: el usuario aprieta una opción sugerida y termina.

**Costo vs. ingresos convierte a menos de la mitad del baseline (12,5%)** `[HALLAZGO — n=8]`. Es el riesgo con lectura financiera y el que menos conversación genera — dirección contraria a la esperada. **No concluir con esa muestra.**

#### Detección y calibración de umbrales (backend)

| Métrica | Proyectos | Veces | Veces/proy | Desvío prom. | Umbral Alto | Sobre umbral |
|---|---:|---:|---:|---:|---:|---:|
| `tasks_without_collaborators` | 12.971 | 109.017 | 8,4 | 51,1% | 20% | **2,6x** |
| `task_finish_date_extended` | 8.961 | 81.005 | 9,0 | 39,5% | 20% | **2,0x** |
| `project_estimated_hours_vs_planned_task` | 5.546 | 44.875 | 8,1 | 10.738% | 40% | 268x |
| `project_estimated_hours_vs_loaded` | 5.493 | 40.886 | 7,4 | 30.544% | 40% | 764x |
| `task_estimated_hours_vs_loaded` | 5.120 | 46.151 | 9,0 | 30,9% | 20% | 1,5x |
| `project_finish_date_extended` | 4.796 | 20.070 | 4,2 | 481% | 41% | 11,7x |
| `task_estimated_hours_vs_planned` | 4.447 | 38.666 | 8,7 | 24,3% | 16% | 1,5x |
| `rework_loaded_hours` | 3.315 | 27.366 | 8,3 | 29,2% | 20% | 1,5x |
| `project_income_vs_costs` | 1.326 | 10.067 | 7,6 | 14.380.117% | 91% | 158.023x |
| `unfinished_tasks_with_rework` | 588 | 4.106 | 7,0 | 20,2% | — | — |
| `project_..._reserved_people_hours` | **52** | 688 | 13,2 | 255% | 20% | 12,8x |

_Leer la columna **Proyectos**, no **Veces** (regla 5). ⚠️ La ventana temporal de este export está sin confirmar: si es histórico acumulado, no prueba estado actual._

**"Alto" no es una severidad: es el estado por defecto** `[HECHO]`. En **las diez métricas que tienen umbral Alto configurado, el desvío promedio ya lo supera** — por 1,5x a 2,6x en las de nivel tarea, por órdenes de magnitud en las de nivel proyecto. _(La undécima, `unfinished_tasks_with_rework`, directamente no tiene umbral cargado: es la misma deuda por otra vía.)_ Bajo y Medio existen en la tabla de umbrales y casi no existen en la base. Eso **vacía de información al donut, al badge de severidad y al orden de la tarjeta**. Es un problema mayor que el nivel Crítico nunca configurado.

**Los porcentajes de los desvíos de nivel proyecto están rotos** `[HECHO]`. Los de nivel tarea son sanos porque son % de tareas (acotados a 100). Los de proyecto salen en miles a millones por ciento. Máximos observados: **2.592.566%** (horas estimadas vs. cargadas), **24.814.759.071%** (costo vs. ingresos), **154.300%** (fecha de proyecto).

**El riesgo que sostiene la propuesta de valor tiene la base más chica** `[HALLAZGO]`. Costo vs. ingresos aplica a **1.326 proyectos** (~10% de la base del #1), porque exige configuración por Ingreso total. A eso se le suman el permiso de **Presupuestos** y que solo se dibuja en pérdida real: **tres estrechamientos apilados sobre el mismo desvío** (→ `03-personas`).

**Horas reservadas tiene techo marginal: 52 proyectos** `[HECHO]`. Aunque se corrija el bug de display documentado, el alcance máximo es despreciable.

**Comparación de rankings** (sin dividir fuentes, regla 4) `[HECHO]`: detección y consulta **coinciden en los dos primeros puestos**. **Retrabajo puntúa muy por encima de su detección** (8º en proyectos, 4º en consultas). Las tres métricas de horas a nivel proyecto son las que más divergen: 3º, 4º y 11º en detección, últimas en consulta.

#### Peso de Risk Management dentro de MAIA

**La serie completa, no solo julio** `[HECHO]`:

| Mes | Usuarios RM / MAIA | Interacciones RM / MAIA |
|---|---:|---:|
| May-26 | 119 / 219 = **54,3%** | 246 / 1.329 = 18,5% |
| Jun-26 | 232 / 323 = **71,8%** | 506 / 1.579 = 32,0% |
| Jul-26 | 234 / 373 = **62,7%** | 479 / 2.303 = 20,8% |

**El 63% de julio no es un pico: es el valor más bajo de los tres meses.** En junio **siete de cada diez** usuarios mensuales de MAIA tocaron un banner.

**Entrada ancha, contacto corto** `[HECHO]`: **54-72% de los usuarios contra 19-32% de las interacciones**. Risk Management es **puerta de entrada, no puerta de paso** — mete mucha gente y casi nadie sigue hacia el resto de MAIA. Consistente con la intensidad de 2,0 y con que la conversación dure 2 a 3 mensajes.

A nivel cuenta: **73 de las 128 companies habilitadas de MAIA tocaron un banner en tres meses** `[HECHO]`.
> ⛔ **Retirado el 2026-08-19:** el corolario de que "**57 companies (45% de la base) tocaron un banner solo en julio**" se citaba como evidencia de no-retorno a nivel cuenta. **No lo es:** describe casi exactamente a las **55 companies habilitadas el 8-jul-2026**, que antes no tenían la feature. No es que dejaran de volver — es que recién llegaban.

> `[HIPÓTESIS — sigue sin dato]` **"Risk Management creó alcance."**
> _Reforzada el 2026-08-19 por la coincidencia de incrementos con MAIA (ver `08-roadmap`), pero **coincidencia no es causalidad y la distinción importa acá**: que Risk Management sea la superficie por la que la mayoría entra está **medido**; que haya traído gente que de otro modo no habría usado MAIA **no lo está**._
> **Qué la refutaría:** que al cruzar el solapamiento resulte que casi todos los usuarios de banner ya usaban MAIA por otra vía en el mismo mes. En ese caso el banner **reencauzó tráfico** en lugar de crear alcance.
> **Test pendiente:** 🔴 el corte de solapamiento — una sola consulta de Amplitude. Ver pedidos de datos.

> ⚠️ **Consecuencia de medición.** Si dos tercios del alcance de MAIA entran por banner, **un movimiento del KR de penetración de MAIA puede ser una feature de superficie funcionando o rompiéndose, y no adopción de MAIA.** El KR necesita cortes separados por origen. Cargado como anti-meta en `05-estrategia-okrs`.

> ⚠️ **La lectura incómoda que acompaña al hallazgo.** Si dos tercios del alcance mensual de MAIA entran por banner, **apagar o romper Risk Management le cuesta a MAIA dos tercios de su alcance.** No es solo un problema de legibilidad del KR: es una **dependencia estructural** — y es sobre la feature en la que Producto recomienda **no ir a GA** (`08-roadmap`). Las dos cosas conviven mal y merecen decidirse juntas.

#### El caso abierto: tres tipos de consulta que caen a cero

`deviationTaskHoursLoaded` (54 consultas en junio, 22,4% del mes), `deviationProjectIncome` (8) y `deviationProjectDelay` (11) caen a **cero** en las 287 consultas de julio y agosto. De las 12 companies que consultaron el primero en junio, **10 siguieron activas** y generaron 44 consultas, todas en los otros tres tipos. Bajo la tasa de junio, P(cero) ≈ 2,4e-32.

**Una conversión más baja produce una pendiente; esto es un escalón.** Hay dos explicaciones vivas y **ninguna se distingue con los datos disponibles**:

- `[HIPÓTESIS A]` **Monopolio de la primera fila.** La tarjeta muestra una sola fila por defecto y el orden es severidad primero; `tasks_without_collaborators` dispara con 51,1% promedio contra un umbral Alto de 20%, así que gana la primera fila casi siempre — aunque en la prioridad configurada esté 6º. El resto queda debajo del pliegue.
  *Refutable con:* la tasa de `AI_RISK_BANNER_SHOW_MORE`.
- `[HIPÓTESIS B]` **Regresión de fines de junio.** Los tres escalones caen en la misma ventana, que es también donde desaparece el tipo `unknown` (96 casos, todos entre el 14-may y el 17-jun): algo tocó ese pipeline ahí.
  *Refutable con:* el desglose de display por tipo del lado backend.

> ⚠️ **No escalar a IT hasta tener uno de los dos cortes.** La recomendación previa de abrir un ticket de regresión era una conclusión, no un dato.

#### Lo que este análisis NO permite afirmar

> _Se registra explícitamente para que no vuelva a circular (mismo criterio que las bajas)._

| Afirmación | Por qué queda afuera |
|---|---|
| "Risk Management opera hoy con tres riesgos" | Se infirió el **display** a partir de los **clicks**. El log no informa qué se mostró. **Retirada explícitamente** — ver `01-producto` |
| Tasas detección→click (ej. "0,15% de conversión") | Divide dos fuentes con unidades y ventanas distintas (regla 4) |
| "A los usuarios les importan las tareas sin colaboradores y las vencidas" | El 91% de concentración es casi tautológico si son lo que más se muestra. No es preferencia revelada |
| "La base decae sin releases", reforzado con la caída de agosto | La feature perdió tipos de consulta en el medio (ver el caso abierto). No sirve como segunda instancia de esa hipótesis |
| "Hay una regresión de fines de junio" (como hecho) | Es una de dos hipótesis competidoras, no un hallazgo |

---

## Marketplace (agentes custom) — baseline nuevo (2026-08-18)

> _Primera medición de esta feature en el repo. Fuente: Amplitude, `AI_CHAT_SEND` con `agent_type = custom`, serie nov-25 → ago-26, más el listado de companies con Feature Access "Marketplace" y sus asientos por rol (export 18-ago-2026)._

### Definiciones propias de esta feature

- **Base habilitada:** **57 companies** al 18-ago-2026 (24 Enterprise · 18 Mid Market · 14 SMB · 1 Retail), con **4.146 asientos** en los cuatro roles con permiso: 1.139 Colaborador · 2.662 PM · 85 Director · 260 C-Level.
- **Asiento elegible:** los cuatro roles, porque los cuatro tienen permiso de **Ver/usar** agentes de fábrica. Es un universo **distinto del de MAIA**, que excluye al Colaborador.
- **Dos poblaciones, dos preguntas.** De fábrica solo **C-Level y Director pueden crear** agentes; PM y Colaborador solo pueden usarlos. Así que "penetración de creación" (denominador jul-26: **268 asientos**) y "penetración de consumo" (denominador jul-26: **2.578 asientos**) son métricas distintas. **Todo lo de abajo mide consumo** — de creación no hay dato.
- **Criterio de corte:** asientos habilitados al inicio de cada mes, igual que en MAIA.

> ⚠️ **Asimetría de definición con MAIA — leer antes de comparar.** MAIA se mide con el `OR` de cuatro eventos; Marketplace, acá, con **`AI_CHAT_SEND` solamente**. La versión anterior de esta nota explicaba la brecha diciendo que tres de los eventos de MAIA eran "call-to-action de baja intención" y que por eso Marketplace estaba medido con la vara más estricta. **Eso quedó retirado el 2026-08-18:** los cuatro son conversación con respuesta generada.
>
> **El motivo real de la asimetría es otro, y es más interesante:** un agente custom **no tiene esas superficies de entrada instrumentadas** — se abre del selector, sin consultas frecuentes, sin banner que lo invoque, sin respuestas sugeridas. No es que la vara de MAIA sea laxa; es que **Marketplace no tiene rieles**.
>
> **`AI_CHAT_SEND` sigue siendo el único evento que significa lo mismo en las dos features: es el que hay que usar para comparar.** Pero la comparación mide *demanda articulada contra demanda articulada*, no "MAIA con trampa contra Marketplace sin ella".
>
> 🎯 **Pregunta de producto que abre esto** (no de medición): parte de la brecha entre 1,40% y 11,6% puede no ser adopción sino **ausencia de superficies de entrada** en Marketplace. Si los rieles que le funcionan a MAIA no existen para agentes custom, eso es una **decisión de roadmap**, no un problema de la feature. → `08-roadmap`.

### Penetración — serie mensual

| Mes | Cuentas | Asientos elegibles | Usuarios | **Penetración** | Interacciones | Intensidad |
|---|---:|---:|---:|---:|---:|---:|
| Nov 25 | 15 | 1.338 | 19 | 1,42% | 74 | 3,9 |
| Dic 25 | 17 | 1.456 | 6 | 0,41% | 61 | 10,2 |
| Ene 26 | 17 | 1.456 | 3 | 0,21% | 15 | 5,0 |
| Feb 26 | 18 | 1.456 | 5 | 0,34% | 17 | 3,4 |
| Mar 26 | 19 | 1.680 | 16 | 0,95% | 70 | 4,4 |
| Abr 26 | 22 | 1.758 | 8 | 0,46% | 109 | 13,6 |
| May 26 | 27 | 1.930 | 38 | 1,97% | 564 | 14,8 |
| Jun 26 | 30 | 2.392 | 41 | 1,71% | 557 | 13,6 |
| **Jul 26** | **31** | **2.578** | **36** | **1,40%** | **638** | **17,7** |
| Ago 26 (parcial, 13 días) | 48 | 3.685 | 26 | 0,71% | 236 | 9,1 |

**Baseline jul-26: penetración 1,40% con intensidad 17,7** `[HALLAZGO]`.
_Por qué no es `[HECHO]`: el denominador no está depurado (ver la nota de integridad más abajo) y la serie es de dos dígitos de usuarios, así que un puñado de personas mueve el indicador._

**Referencia para el universo comparable con MAIA:** sacando al Colaborador, jul-26 da **32 usuarios sobre 1.852 asientos = 1,73%** — sigue sin resolver la asimetría de eventos de la nota de arriba.

**La intensidad de Marketplace es ~3x la de MAIA** (17,7 contra 6,2 en jul-26) con una penetración ~8x menor `[HALLAZGO]`. Poca gente, muy metida. Es el perfil inverso al de MAIA.

### La feature es, en la práctica, una cuenta

| Corte jul-26 | Usuarios | Interacciones | Asientos | Penetración | Int./usuario |
|---|---:|---:|---:|---:|---:|
| **MullenLowe Delta** | 26 | 554 | 320 | 8,1% | **21,3** |
| Resto de la base habilitada | 10 | 84 | 2.258 | **0,44%** | 8,4 |
| **Total** | **36** | **638** | **2.578** | **1,40%** | **17,7** |

**MullenLowe Delta concentra el 72% de los usuarios y el 87% de las interacciones de julio** `[HECHO]`. Sin esa cuenta, la penetración del resto de la base habilitada es **0,44%**.

**36 de las 57 companies habilitadas no registraron un solo usuario en diez meses** `[HECHO]` — **2.012 asientos, 49% del universo**. En MAIA la cifra equivalente es 12% de las cuentas; acá es **63%**.

**Adentro de MullenLowe, una sola persona.** El histograma de julio tiene un usuario en el bucket `>100`; despejando el resto de los buckets por punto medio, esa persona explica **~230 de las 638 interacciones del mes — cerca de un tercio del volumen total de la feature** `[HALLAZGO]`.
_Es una estimación por punto medio, igual que la concentración de MAIA: los buckets bajos suman ~407 y el resto queda en un solo usuario. La conclusión (un individuo domina el volumen) es robusta; la cifra exacta no._

> **Consecuencia de medición:** para Marketplace, el volumen de interacciones **no mide la feature, mide a una persona**. Aplica la misma regla que en MAIA pero más fuerte: la métrica de salud es la penetración y la cantidad de cuentas con al menos un usuario recurrente, nunca el total.

### Distribución de frecuencia — usuarios por interacciones en el mes

| Mes | 1 | 2-5 | 6-10 | 11-20 | 21-50 | 51-100 | >100 | Total |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Nov 25 | 6 | 9 | 2 | 2 | 0 | 0 | 0 | 19 |
| Dic 25 | 2 | 2 | 1 | 0 | 1 | 0 | 0 | 6 |
| Ene 26 | 1 | 1 | 0 | 1 | 0 | 0 | 0 | 3 |
| Feb 26 | 3 | 1 | 0 | 1 | 0 | 0 | 0 | 5 |
| Mar 26 | 8 | 5 | 1 | 2 | 0 | 0 | 0 | 16 |
| Abr 26 | 1 | 4 | 0 | 0 | 3 | 0 | 0 | 8 |
| May 26 | 9 | 9 | 4 | 8 | 5 | 2 | **1** | 38 |
| Jun 26 | 8 | 14 | 0 | 7 | 11 | 1 | 0 | 41 |
| Jul 26 | 4 | 6 | 11 | 10 | 4 | 0 | **1** | 36 |

_Los buckets `2-5` son agregación propia (Amplitude entrega 2/3/4/5 por separado). **Validación:** el total de cada histograma coincide exactamente con los usuarios únicos del agregado mensual, en los nueve meses con histograma. Agosto no tiene histograma._

**El bucket `>100` existe en Marketplace y no existe en MAIA** `[HECHO]`. Con una base activa de 36 usuarios contra los 413 de MAIA, el uso individual llega más alto donde hay menos gente. Refuerza que son dos perfiles de uso distintos, no dos intensidades de lo mismo.

### Por rol

| Mes | Colaborador | PM | Director | C-Level |
|---|---:|---:|---:|---:|
| May 26 | 1,0% | 1,0% | 24,5% | 5,2% |
| Jun 26 | 0,9% | 0,8% | 32,1% | 2,9% |
| **Jul 26** | **0,7%** | **0,6%** | **29,1%** | **2,8%** |
| Ago 26 (parcial) | 0,1% | 0,3% | 13,8% | 3,2% |

_Asientos jul-26: Colaborador 726 · PM 1.584 · Director 55 · C-Level 213._

**El Director es el único rol con penetración de dos dígitos** `[HALLAZGO]`, muy por encima de todo lo demás y en las antípodas de MAIA, donde los tres roles penetran casi igual.
_Salvedad de n, fuerte: son **16 usuarios sobre 55 asientos de Director** en toda la base habilitada. Dos personas mueven el indicador cerca de 4 puntos. **Es señal de dirección, no magnitud** — y no alcanza para fijar una meta._

**Ojo con el Colaborador:** en Marketplace **no está excluido** y tiene 726 asientos elegibles con 0,7% de penetración. Es el único lugar del repo donde hay dato de uso de AI de ese rol.

### Por segmento

Jul-26 — **Enterprise: 27 de 36 usuarios y 557 de 638 interacciones**; Mid Market 3 usuarios / 45 interacciones; SMB 6 usuarios / 36 interacciones `[HALLAZGO]`.
_Sin normalizar por asientos por segmento — mismo problema que el "Enterprise 58%" de `[BAJA-01]`. **Tratar como composición, no como penetración por segmento.** Y está dominado por MullenLowe, que es Enterprise._

### Integridad del denominador — verificar antes de usar

**Seis companies con uso registrado no aparecen en el listado de habilitadas:** diPaola, Oxford, ABCOM, Help Team, Pinky y STRONG. O el export es una foto de hoy y esas cuentas perdieron el Feature Access, o hay churn sin depurar. **Su uso está contado en el numerador y sus asientos no están en el denominador**, así que la penetración de los meses donde aparecen está sobreestimada. Afecta sobre todo a nov-25 → abr-26.

### Lo que estos datos NO dicen

**Todo esto es consumo. De creación de agentes no hay nada.** La documentación funcional lista un funnel completo instrumentado —`AI_CHAT_MP_OPEN`, `AI_CHAT_MP_SELECT_AGENT`, `AI_CHAT_ABM_ACCESS`, `AI_CHAT_ABM_SECTION`, `AI_CHAT_ABM_SELECT_MODEL`, `AI_CHAT_ABM_CHOOSE_MODEL`, `AI_CHAT_ABM_ACCESSIBILITY_TYPE`, `AI_CHAT_ABM_CONFIRM`— y **nada de eso está pulleado**.

Por eso hoy **no se puede responder la pregunta que decide la iniciativa**: la penetración de 0,44% fuera de MullenLowe, ¿es porque casi no hay agentes creados, o porque hay agentes creados que nadie usa? Son dos problemas distintos con dos soluciones distintas.

> 📊 **`AI_CHAT_ABM_CONFIRM` registra un agente efectivamente creado — o sea un artefacto producido, no actividad.** Junto con el evento de aprobación de acciones de Governance, es el **segundo candidato a medir valor entregado** en lugar de uso. El bloque "El límite de toda esta sección" decía que había uno solo; son dos.

### Bajas registradas

> _No se borran: si no queda rastro, vuelven a aparecer en un deck en tres meses._

**`[BAJA-01]` — "El PM es, por lejos, el rol que más usa MAIA."** _(Baja 2026-08-17.)_
**Motivo:** falla el test de **denominador**. El 56% de los usuarios y el 51% de las interacciones del PM es efecto de tamaño de base (1.917 asientos contra 458 del C-Level). Normalizado, los tres roles penetran casi igual: 11,5% / 10,8% / 13,3% en julio.
**Alcance del error:** esta afirmación se usaba para reforzar el pilar "del brief al proyecto" de `01-producto`. **Ese cruce queda sin sustento cuantitativo** — el pilar puede seguir siendo válido, pero no por esta vía.
**Colateral pendiente:** el corte por segmento ("Enterprise 467, 58%") tiene exactamente el mismo problema y **sigue sin normalizar** — el documento fuente no trae penetración por segmento. **Tratar el 58% como no verificado** hasta tener el corte por asientos.

> 🔍 **Pista nueva (2026-08-19), no concluyente.** En la base de Risk Management, **los asientos elegibles de Enterprise son 2.002 de 3.444 = 58,1%** — prácticamente idéntico al 58% de *usuarios* Enterprise que este corte reporta para MAIA.
> `[HIPÓTESIS]` **El "Enterprise 58%" es efecto de tamaño de base, tercera instancia del mismo sesgo** (después del corte por rol de MAIA y del de banners por rol de `03-personas`).
> **Por qué no alcanza:** son features distintas y poblaciones distintas — **asientos** de Risk Management contra **usuarios** de MAIA. La coincidencia es sugestiva, no probatoria.
> **Qué la resolvería:** asientos elegibles de MAIA por segmento. Es el mismo tipo de export que el de Risk Management, para las 128 companies. 🟡 Pedido cargado abajo.

**`[BAJA-02]` — "Calidad percibida positiva: 91% de feedback favorable."** _(Baja 2026-08-17.)_
**Motivo:** falla el test de **instrumentación**. 121 eventos sobre ~8.200 interacciones es una tasa del 1,5%; un ratio 9:1 en una muestra autoseleccionada de ese tamaño no mide calidad, mide quién se molesta en calificar. Estaba cargado como **fortaleza** y no lo es.

## Enlaces entre archivos

- KPIs de negocio y metas → `05-estrategia-okrs`.
- Heavy users y roles → `03-personas`.
- Features que estas métricas miden → `01-producto`.
- Adopción de MAIA (arriba) responde a la prioridad "Deploy de AI en clientes" de `05-estrategia-okrs`.

**Interpretaciones derivadas de los datos de AI que NO viven en este archivo** (este archivo mide; los otros deciden):

- Reparto de capacidad entre **construir capacidad y construir superficie**, e iniciativa de activación de cuentas dormidas → `08-roadmap`.
- Metas, **anti-metas** y laddering de los KRs de AI → `05-estrategia-okrs`.
- Por qué las cuentas dormidas no volvieron, qué pasó en **Crowe Global** y por qué Risk Management **engancha en el momento y no genera vuelta** → `07-discovery`.
- Recomendación sobre el **GA de Risk Management** y su lugar en el eje capacidad vs. superficie → `08-roadmap`.
- Penetración de banners **por rol** y el segundo caso del sesgo de denominador → `03-personas`.
- Estado real de las capacidades de MAIA y cronología de releases → `01-producto`.

## Pendientes — input interno

- [x] North Star de negocio. _(ARR, confirmada.)_
- [ ] North Star de producto — todavía sin definir.
- [ ] Qué métricas de producto se trackean hoy y sus **valores actuales / baseline**. _(Ya cargado: NPS por rol y CSAT de soporte de Retently; DAU/WAU/MAU y stickiness de Amplitude. Falta: cobertura de time tracking, uso de features clave — en camino.)_
- [ ] ¿Se trackean hoy las métricas de **calidad de servicio** (performance, crash rate, bugs)? Son los dolores #1 según `07`.
- [ ] Definiciones y fórmulas exactas (cómo calcula COR NRR, GRR, churn, activación).
- [x] Métrica que mide la prioridad **"Deploy de AI en clientes"**. _(Reemplazada el 2026-08-17: **penetración sobre asientos elegibles**, con definiciones, baseline y etiquetado de evidencia. La versión anterior —usuarios únicos absolutos, composición por rol/segmento sin normalizar, calidad percibida— quedó dada de baja; ver `[BAJA-01]` y `[BAJA-02]`.)_
- [x] Health score: confirmado que **no existe hoy**. Queda pendiente definirlo (qué lo compondría: uso, retrabajos, rentabilidad del cliente, NPS, etc.).

### Pedidos de datos abiertos — vertical de AI

_Siete de estos salen del documento fuente de adopción; cinco están marcados ahí como "no solicitados", o sea que son baratos._

- [ ] 🟠 **Corte de autoría de la consulta** — separar `AI_CHAT_SEND` (demanda articulada por el usuario) de los otros tres eventos (demanda inducida por FAQ, banner y respuestas sugeridas), en usuarios y en interacciones, para la serie mensual completa. _Reclasificado el 2026-08-18: **ya no es una recalibración del baseline** —el numerador está limpio, ver el bloque de definiciones— **ni bloquea el KR.** Es la segmentación que hace legible el KR una vez fijado._
- [ ] 🟡 **Volumen de `AI_CHAT_OPEN` con `option = header`** — hoy explícitamente fuera de la serie por no ser conversión. No cambia ninguna métrica de este archivo, pero es la única lectura disponible de **intención sin conversión**: gente que abre MAIA y no llega a preguntar nada. Si el volumen es alto, es señal de fricción en el momento de formular la consulta. ⛔ **No incorporar a la serie de penetración bajo ningún concepto.**
- [ ] 🔴 **Estado de actividad/churn por company** para depurar el denominador de asientos elegibles. **Bloquea dimensionar la iniciativa de cuentas dormidas de `08`.**
- [ ] **Distribución de frecuencia abierta por rol.** Hoy no se sabe si los 6 power users de julio son C-levels o PMs, y de eso depende toda la lectura de saturación del C-Level. _Es el corte más valioso que falta._
- [ ] **Interacciones desagregadas por tool/agente** — para saber qué capacidades movieron la aguja (y poder testear la hipótesis capacidad/superficie de `08`). **Baja de dificultad:** el registro de qué especialista intervino en cada consulta **ya existe** (se guarda para análisis y debug, según la documentación funcional del Orquestador). El pedido pasa de "instrumentar" a **"refinar y extraer"**.
- [ ] **Retención de usuarios de MAIA por cohorte de primer uso** (Amplitude — mencionada, no compartida).
- [ ] **Penetración por segmento** normalizada por asientos (ver colateral de `[BAJA-01]`: el "Enterprise 58%" sigue sin verificar).
- [ ] **Instrumentar el evento de aprobación de acciones** de MAIA (Governance, Pilar 3 de `01`) — único camino a medir valor entregado en lugar de actividad.
- [ ] **Revenue por company** (MRR/ARR + eventos de churn) para medir si MAIA impacta la retención. _Depende del reporte de HubSpot, ya pendiente en `04-mercado`._
- [ ] **Propuesta de valor y métrica para el rol Colaborador** — hoy excluido del análisis, pero son **5.605 asientos adicionales**, más que todo el universo elegible actual (3.775). → `03-personas`.
- [ ] **Métrica para las features del portafolio de AI sin instrumentar:** hoy queda **solo workflows / automatizaciones**. _(Marketplace tiene baseline de consumo desde el 2026-08-18 y **Risk Management tiene baseline de alcance desde el 2026-08-18** — ver sus secciones. Sigue faltando el funnel de **creación** de Marketplace y el **valor entregado** de Risk Management, listados aparte.)_
  - ⚠️ Antes de instrumentar workflows: definir si es feature hermana (denominador propio) o pilar de MAIA (se mide adentro). Criterio en `01-producto`. **Risk Management ya está resuelto: pilar de MAIA con activación separada, medido acá adentro con corte por origen.**

### Pedidos de datos abiertos — Risk Management

_Cargados el 2026-08-18 y ampliados el 2026-08-19 con el export de altas._

- [ ] 🔴 **Solapamiento MAIA / banner por usuario** (usuarios únicos de MAIA en julio menos los que dispararon algo distinto de `risk_banner`). **Desbloquea** la hipótesis de que Risk Management creó alcance, y el eje capacidad vs. superficie de `08-roadmap`. Es una sola consulta de Amplitude.
- [ ] 🔴 **Ventana temporal del export de detecciones del backend.** **Bloquea todo el bloque de calibración de umbrales:** si es histórico acumulado, no prueba estado actual.
- [ ] 🟠 **Tasa de `AI_RISK_BANNER_SHOW_MORE`.** Decide si la fila única explica la concentración en dos riesgos (`[HIPÓTESIS A]` del caso abierto).
- [ ] 🟠 **Desglose por tipo de lo que efectivamente se dibujó** (lado backend). Convierte la asimetría detección→consulta en métrica en lugar de inferencia, y refuta o confirma `[HIPÓTESIS B]`.
- [x] ✅ **Denominador real del rol Director** — **resuelto el 2026-08-19** con el export de altas: **923 asientos de Director en la base de Risk Management** (865 al 1-ago-26). La inferencia por resta (~850) era correcta. _Ojo: es la base de Risk Management (119 companies), no la de MAIA (128)._
- [ ] 🔴 **Usuarios únicos de Risk Management restringidos a la cohorte del denominador.** Para cada mes, contar usuarios **solo de las companies habilitadas antes del inicio de ese mes** (jun → las 15 de mayo · jul → las 32 de may+jun · ago → las 111). **Desbloquea la penetración de Risk Management, hoy en pausa.** Es un filtro por lista de company IDs sobre una consulta que ya existe; la lista sale del export de altas del 19-ago-2026.
- [ ] 🟠 **Retención de Risk Management en meses desde la habilitación**, sobre la cohorte de mayo (15 companies, única con ventana completa). Reemplaza al 83% "en un solo mes", que no controla por fecha de alta.
- [ ] 🟡 **Asientos elegibles de MAIA por segmento** — mismo export que el de Risk Management, para las 128 companies. Cierra el colateral de `[BAJA-01]` ("Enterprise 58%").
- [ ] 🟠 **Evento de acción aplicada desde una respuesta de riesgo.** Risk Management ofrece acciones masivas reales (asignar colaboradores, mover deadlines, reasignar tareas) y **no existe ningún evento que registre si alguien las aplica**. Es el mejor lugar del producto para medir **valor entregado**, junto con la aprobación de Governance.
- [ ] 🟡 **Aperturas sin respuesta generada** (el gap entre 1.364 aperturas de Amplitude y 653 filas de log). Calidad, no bloqueante del baseline.

### Pedido a Data — versión consolidada (2026-08-19)

_Los pedidos de arriba están listados por feature. Esto es cómo se agrupan en **un solo pedido** a Data, para no ir tres veces._

**Universo común:** usuarios de las 128 companies con MAIA habilitada, roles **PM + Director + C-Level**. Período **may–ago 2026** (julio como referencia). Métrica **`Uniques`**, no `Totals`. Filtro de `AI_CHAT_OPEN`: **solo valores de conversión**, `header` excluido (regla 8).

| | Corte | Qué pedir | Desbloquea |
|---|---|---|---|
| 🔴 | **A — solapamiento MAIA / banner** | Por mes: (1) usuarios únicos con al menos un evento de conversión · (2) con al menos uno con `option = risk_banner` · (3) con al menos uno distinto de `risk_banner` · **(4) la intersección de 2 y 3** | El KR de MAIA y el eje capacidad vs. superficie |
| 🔴 | **D — RM por cohorte de habilitación** | Usuarios únicos de `risk_banner` por mes, **restringidos a las companies habilitadas antes del inicio de cada mes** (jun → las 15 de mayo · jul → las 32 · ago → las 111). Lista de IDs en el export del 19-ago-26 | La penetración de Risk Management, hoy en pausa |
| 🟠 | **C — verificación de Marketplace** | Confirmar si la serie histórica de MAIA se pulleó con filtro `agent_type in (orchestrator, clone)` o sin filtro. Si fue sin filtro, re-pullear julio con el filtro puesto | Tratar MAIA y Marketplace como series independientes |
| 🟠 | **B — autoría de la consulta** | Usuarios e interacciones separando `AI_CHAT_SEND` de los otros tres eventos, serie mensual completa. _Puede ir en la misma consulta que A si es barato_ | La legibilidad del KR una vez fijado |
| 🟡 | **E — asientos de MAIA por segmento** | Mismo tipo de export que el de Risk Management, para las 128 companies | El colateral de `[BAJA-01]` ("Enterprise 58%") |

> ⚠️ **Salvedad que va dentro del pedido:** los funnels de Amplitude **dedupean a nivel usuario** (regla 7). Necesitamos **conteos de usuarios únicos por condición**, no filas de funnel.

#### Regla de decisión del corte A — fijada antes de ver el número

> _Se escribe de antemano a propósito: si se decide después de ver el resultado, no es una regla de decisión, es una racionalización._

| Resultado | Lectura | Consecuencia |
|---|---|---|
| **Intersección baja** — la mayoría de los 234 usuarios de banner no tocó MAIA por otra vía | Risk Management **creó alcance** | El eje capacidad vs. superficie pasa de `[HIPÓTESIS FUERTE]` a hallazgo (`08-roadmap`). El KR de MAIA **se reporta en dos líneas separadas** |
| **Intersección alta** — casi todos ya usaban MAIA en el mismo mes | Risk Management **reencauzó tráfico** | Hipótesis refutada. El 63% no es alcance nuevo: es la misma gente entrando por otra puerta. El KR agregado es menos engañoso de lo temido |

**En los dos escenarios el KR se puede escribir.** Es lo único que separa a `05-estrategia-okrs` de tener KRs de AI.

### Pedidos de datos abiertos — Marketplace

- [ ] 🔴 **Verificar si la serie de MAIA de este archivo se pulleó filtrando `agent_type in (orchestrator, clone)` o sin filtro.** _(En el pedido consolidado va como **Corte C**, priorizado 🟠 dentro de esa tanda: es el menos urgente de los que se piden juntos, pero sigue siendo 🔴 para el repo porque bloquea tratar las dos series como independientes.)_ Si no está filtrada, los 373 usuarios y 2.303 interacciones de jul-26 **incluyen uso de agentes custom** y las dos series no son independientes. _Indicio de que puede no estar filtrada: la sección de calidad percibida documenta explícitamente su filtro por `agent_type` y el bloque de definiciones de uso no menciona ninguno._ **Bloquea tratar los dos números como features separadas o como aditivos.**
- [ ] 🔴 **Funnel de creación de agentes** (`MP_OPEN` → `SELECT_AGENT` / `ABM_ACCESS` → `ABM_CONFIRM`) y **cantidad de agentes creados, vivos y por company.** **Bloquea saber si el problema es que no se crean agentes o que los creados no se usan** — y sin eso no se puede diseñar ninguna iniciativa sobre esta feature.
- [ ] **Separar los dos Feature Access** ("Marketplace" vs. "Marketplace Maiaker"): cuántas companies tienen cada uno. Hoy la serie los mezcla, así que no se puede medir la creación conversacional (MAIAKER) sobre su propia base.
- [ ] **Depurar el denominador:** las seis companies con uso que no están en el listado de habilitadas (ver la nota de integridad).
- [ ] **Overlap con la base de MAIA:** cuántas de las 57 companies tienen las dos features. Decide si Marketplace es superficie nueva o un segundo uso de las mismas cuentas.
- [ ] **Distribución de modelo elegido** (`ABM_CHOOSE_MODEL`) y de **accesibilidad** (compañía / clientes específicos / solo para mí). El primero testea si la elección de modelo es palanca real o si todos quedan en el default; el segundo, si los agentes son activos organizacionales o herramientas personales.
