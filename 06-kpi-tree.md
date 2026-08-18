# 06 — KPI Tree (COR)

> **Última actualización:** 2026-08-17
> **Owner:** Product Manager, área de Producto
> **Contexto para IA:** Árbol de métricas de COR, desde la North Star hasta las métricas operativas y de producto, para definir el éxito de una feature o analizar resultados. Las métricas de **negocio** vienen confirmadas del Business Plan 2026–2027 (`05`); las de **producto** están inferidas y marcadas como hipótesis hasta confirmarlas.
>
> ⚠️ **La sección de AI usa un etiquetado de evidencia propio** (`[HECHO]` / `[HALLAZGO]` / `[HIPÓTESIS]` / `[BAJA]`) definido dentro de esa sección. **Respetar la etiqueta al citar un número:** un `[HALLAZGO]` no se cita como si fuera un hecho, y un `[HIPÓTESIS]` no sirve para justificar reparto de capacidad. El resto del archivo todavía no está etiquetado.

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

## Métrica de producto para "Deploy de AI en clientes" (medida — baseline ago-2026, fuente: Amplitude)

> **Reescrita el 2026-08-17** a partir de *MAIA — Análisis de adopción y penetración v3.0* (Producto, 2026-08-15). Reemplaza el baseline anterior, que estaba construido sobre conteos absolutos sin denominador. Dos afirmaciones de esa versión quedaron **dadas de baja** — ver el final de la sección.

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

### Definiciones

Sin estas tres definiciones los números de abajo no se pueden leer, y su ausencia es lo que produjo las dos bajas del final.

- **Asiento elegible.** Suma de asientos de **PM + Director + C-Level** de las companies con MAIA habilitada al inicio del mes. Al 13-ago-2026: **3.775 asientos en 128 companies**.
- **Penetración.** Usuarios únicos ÷ asientos elegibles, en el mismo período. **Es la métrica principal de la vertical de AI.** Reemplaza el conteo de usuarios únicos absolutos.
- **Intensidad.** Interacciones ÷ usuarios únicos.
- **Usuario único / interacción.** Métricas `Uniques` y `Totals` de Amplitude sobre los eventos `AI_CHAT_SEND`, `AI_CHAT_SELECT_FAQ`, `AI_CHAT_OPEN` y `AI_CHAT_SUGGESTED_ANSWER`. Se deduplica **dentro** de cada mes, no entre meses: las columnas mensuales **no son sumables**. La vara es una sola interacción.

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

**Baseline oficial jul-26: penetración 11,6%** `[HALLAZGO — provisorio]`.
_El numerador incluye `AI_CHAT_OPEN`, es decir usuarios que abrieron el panel sin escribir nada, así que la cifra está inflada por arriba. En paralelo, el denominador incluye cuentas que pueden haber churneado, lo que la infla por abajo. **El signo neto del sesgo es desconocido** — no asumir que 11,6% es un piso conservador._
**→ Recalibrar con el corte por solo `AI_CHAT_SEND` antes de fijar cualquier KR sobre esta cifra.**

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

La brecha es **más grave para el resto de la vertical de AI que para MAIA**. Un chat puede evaluarse razonablemente por frecuencia de uso; un workflow automatizado, un agente custom del marketplace o una alerta de risk management, no — su valor está en el trabajo que ejecutan, y ese trabajo hoy no se registra como evento. **Ninguna métrica actual captura la vertical de AI fuera de MAIA.**

**El candidato más directo para empezar a medir valor entregado:** el Pilar 3 de MAIA (Governance, `01-producto`) exige **aprobación explícita del usuario para cada acción crítica**. Ese evento existe en el producto y **no se está registrando como métrica**.

### Métricas oficiales candidatas para "Deploy de AI en clientes"

Reemplaza la lista anterior, que se apoyaba en conteos absolutos.

| Candidata | Estado | Nota |
|---|---|---|
| **Penetración por rol** sobre asientos elegibles | Con baseline | Métrica principal. **Meta diferenciada por rol** — no una sola meta para los tres |
| **Forma de la distribución** (share de los buckets 11+) | Con baseline | Reemplaza volumen total y promedio de interacciones |
| **Penetración por cuenta / dispersión** | Con baseline | Habilita meta de activación de cuentas, no solo de usuarios |
| **Eventos de aprobación de acciones** (Governance) | No instrumentado | Único candidato a medir **valor entregado** en lugar de actividad |
| ~~Usuarios únicos activos/mes~~ | Degradada | Se mueve con el denominador; sirve de diagnóstico, no de meta |
| ~~Volumen de interacciones~~ | Descartada | Mide a ~26 personas |
| ~~% de power users vs. uso único~~ | Reformulada | Absorbida por "forma de la distribución" |
| ~~Calidad percibida (thumbs)~~ | Descartada | Tasa de feedback 1,5%. Ver `[BAJA-02]` |

### Bajas registradas

> _No se borran: si no queda rastro, vuelven a aparecer en un deck en tres meses._

**`[BAJA-01]` — "El PM es, por lejos, el rol que más usa MAIA."** _(Baja 2026-08-17.)_
**Motivo:** falla el test de **denominador**. El 56% de los usuarios y el 51% de las interacciones del PM es efecto de tamaño de base (1.917 asientos contra 458 del C-Level). Normalizado, los tres roles penetran casi igual: 11,5% / 10,8% / 13,3% en julio.
**Alcance del error:** esta afirmación se usaba para reforzar el pilar "del brief al proyecto" de `01-producto`. **Ese cruce queda sin sustento cuantitativo** — el pilar puede seguir siendo válido, pero no por esta vía.
**Colateral pendiente:** el corte por segmento ("Enterprise 467, 58%") tiene exactamente el mismo problema y **sigue sin normalizar** — el documento fuente no trae penetración por segmento. **Tratar el 58% como no verificado** hasta tener el corte por asientos.

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
- Por qué las cuentas dormidas no volvieron y qué pasó en **Crowe Global** → `07-discovery`.
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

- [ ] 🔴 **Recalibrar el baseline con el corte por solo `AI_CHAT_SEND`** — hoy el 11,6% incluye aperturas de panel sin escribir. **Bloquea fijar el KR de penetración.**
- [ ] 🔴 **Estado de actividad/churn por company** para depurar el denominador de asientos elegibles. **Bloquea dimensionar la iniciativa de cuentas dormidas de `08`.**
- [ ] **Distribución de frecuencia abierta por rol.** Hoy no se sabe si los 6 power users de julio son C-levels o PMs, y de eso depende toda la lectura de saturación del C-Level. _Es el corte más valioso que falta._
- [ ] **Interacciones desagregadas por tool/agente** — para saber qué capacidades movieron la aguja (y poder testear la hipótesis capacidad/superficie de `08`). **Baja de dificultad:** el registro de qué especialista intervino en cada consulta **ya existe** (se guarda para análisis y debug, según la documentación funcional del Orquestador). El pedido pasa de "instrumentar" a **"refinar y extraer"**.
- [ ] **Retención de usuarios de MAIA por cohorte de primer uso** (Amplitude — mencionada, no compartida).
- [ ] **Penetración por segmento** normalizada por asientos (ver colateral de `[BAJA-01]`: el "Enterprise 58%" sigue sin verificar).
- [ ] **Instrumentar el evento de aprobación de acciones** de MAIA (Governance, Pilar 3 de `01`) — único camino a medir valor entregado en lugar de actividad.
- [ ] **Revenue por company** (MRR/ARR + eventos de churn) para medir si MAIA impacta la retención. _Depende del reporte de HubSpot, ya pendiente en `04-mercado`._
- [ ] **Propuesta de valor y métrica para el rol Colaborador** — hoy excluido del análisis, pero son **5.605 asientos adicionales**, más que todo el universo elegible actual (3.775). → `03-personas`.
- [ ] **Métrica para la vertical de AI fuera de MAIA** (workflows, marketplace, risk management): hoy **no existe ninguna**.
