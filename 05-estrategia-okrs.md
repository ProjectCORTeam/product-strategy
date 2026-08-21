# 05 — Estrategia y OKRs (COR)

> **Última actualización:** 2026-08-21
> **Owner:** Product Manager, área de Producto
> **Contexto para IA:** Visión, pilares estratégicos, KPIs y OKRs, para priorizar y alinear iniciativas. Base principal: **Business Plan 2026–2027** (presentado internamente). Es un plan de negocio/GTM: fuerte en revenue y go-to-market, liviano en estrategia de producto.
> ✅ **Los OKRs de la vertical de AI están cargados desde el 2026-08-19** — ver "OKRs del trimestre". Son los **primeros OKRs de producto de COR**. Los de las otras verticales y ejes/squads **siguen sin definir: no inventarlos.**
> 🔄 **O1 se reescribió el 2026-08-21:** cambió de título (*"Confiabilidad y calidad"* → *"Ejecución confiable"*), pasó de **cinco KRs a cuatro** —tres retirados, dos nuevos— y **las cuatro metas están puestas pero son provisorias: ninguna se fijó contra una medición.** O2 no se tocó.

## Visión / ambición de empresa

No hay una visión de producto formalizada (ver `01-producto.md`). La ambición de **empresa** está fijada por el Business Plan 2026–2027:

- **Meta:** crecer de **$6.8M a $10.2M ARR** para el cierre de 2027 (**+50%**), diversificando más allá del core de agencias LatAm.
- **Lema del plan:** "see the future".

## KPIs núcleo (a sostener)

Los tres KPIs contra los que se mide todo el plan ("main KPIs to keep"):

- **ARR Annual Growth:** 51%
- **NRR (Net Revenue Retention):** 115%
- **GRR (Gross Revenue Retention):** 90%

## Trayectoria financiera

- **Exit 2025:** $4.7M ARR → **Hoy (jul-26):** $5.48M → **Goal cierre 2026:** $6.8M → **Goal cierre 2027:** $10.2M.
- Faltan **~$1.32M de ARR en 5 meses** para cerrar 2026 en $6.8M.
- **Construcción del número 2027:** $6.8M (Exit 2026) + **$2.38M Net New** + **$1.02M Installed Base** (a NRR 115%) = **$10.2M** (Exit 2027).
- Claves del exit 2026: 1 *whale*, mantener churn, e igualar el Net New del H2 2026 (sin whales).

## Prioridades estratégicas 2026–2027

Las tres prioridades oficiales del plan ("todo lo demás es ruido"):

1. **Apertura de nuevos verticales** — diversificación de la base y generación de pipeline propio en cada vertical.
2. **Thought leadership por vertical** — voz propia y contenido de industria en cada mercado nuevo.
3. **Deploy de AI en clientes** — más valor entregado en la base instalada para buscar un **NRR > 115%**. _(La prioridad más ligada a Producto / MAIA.)_

## Estrategia GTM

- **Playbook replicable:** el mismo que funcionó en agencias LatAm y se validó en Brasil, replicado vertical por vertical. Tres piezas: **Owner por BU**, **Target Accounts** (lista corta y explícita por vertical, no prospección abierta) y **Account-Based Marketing** (demanda construida alrededor de esas cuentas).
- **Nuevos roles — Industry Leads:** uno por vertical. *Goal:* ejecutar y liderar el GTM del vertical. *Scope:* expertise de industria, thought leadership, networking y soporte al ciclo de venta.
  > _Confirmado con organigrama interno (`02-equipos`): ya están cubiertos **Agencies** (Birger Kamrath), **Law & Accounting** (Mariano Covatti) e **IT** (Francisco Vizcaino), más **Brands** (Sol Spicuglia, no estaba explícito acá). Falta **Media**._

## Verticales y geografías de expansión

El core de **Agencias LatAm por sí solo no alcanza para crecer +50% YoY**, de ahí la apertura de verticales. Net New 2027 por línea:

| Línea | Net New |
|---|---|
| Agencias LatAm | $576K |
| Agencias Brazil | $576K |
| Agencias EMEA | $432K |
| Law & Accounting | $432K |
| IT Consulting | $432K |
| Brands | $396K |
| Media | $306K |
| Buffer | 32% |

- **Brands y Media** arrancan en **abril 2027** — son upside de mitad de año, no baseline.
- Nota: esto **expande el ICP y el mercado** de los archivos `03-personas` y `04-mercado` (nuevos verticales + geografía EMEA).

## Desafíos / riesgos 2026–2027

1. **Acelerar conversion rates de los verticales nuevos** — sin conversión, el pipeline de Law, IT, Brands y Media no se traduce en ARR. Focos: Pain Points, Discovery & Demo.
2. **Aumentar el pipeline de whales y asegurar conversión** — cuentas grandes con ticket alto: menos deals, más ARR por deal.
3. **Blindaje 2027: reducción de churn** — el +$1.02M de installed base depende de sostener un NRR de 115%.

## Cómo laddera Producto a "Deploy de AI en clientes"

> _Cargado el 2026-08-17 a partir de *MAIA — Análisis de adopción y penetración v3.0*. La medición vive en `06-kpi-tree` (sección de AI, con etiquetado de evidencia); acá está lo que la estrategia puede apoyarse en decir._

**Contexto de partida.** MAIA se desarrolló hasta hoy **sin estrategia de producto formalizada**: sin outcomes definidos, sin OKRs ni KRs. La lógica fue construir capacidades, medir actividad y responder a pedidos. Este bloque existe para que el paso siguiente —definir la estrategia de la vertical de AI— arranque con baseline.

> ✅ **Ese paso siguiente ya ocurrió: el 2026-08-19 se cargaron O1 y O2 de la vertical de AI** (sección "OKRs del trimestre"). Lo que sigue en este bloque —métrica, anti-metas, huecos y decisiones abiertas— **es la evidencia sobre la que se apoyan**, y se mantiene como tal.

### La métrica que mide la prioridad

**Penetración = usuarios únicos ÷ asientos elegibles** (PM + Director + C-Level de las cuentas con MAIA habilitada). Reemplaza el conteo de usuarios activos absolutos, que se movía con el denominador.

| Referencia | Valor |
|---|---|
| Baseline jul-26, base completa | **11,6%** `[HECHO]` _— **piso conservador** (2026-08-18: la salvedad de instrumentación se retiró; el único sesgo vivo es de denominador y deprime la cifra)_ |
| Baseline jul-26, panel cerrado de cuentas 2025 | **14,6%** |
| **Techo observado hoy** (mejores cuentas) | **>23%** |
| Piso observado (8 cuentas Enterprise "dormidas") | **3,3%** |

### Cinco anti-metas — errores de KR que la evidencia ya descarta

Esto es lo más accionable del análisis para este archivo: **no** fijar KRs sobre estas bases.

1. **No fijar una meta única de penetración para los tres roles.** El C-Level lleva cinco meses entre 9,5% y 13,3% mientras el PM pasó de 1,8% a 11,9% en cinco meses. Una meta común castiga a un rol posiblemente cerca de su techo y subestima a los otros dos. **Metas diferenciadas por rol.**
2. **No usar volumen de interacciones como KR.** El 6% de los usuarios genera ~43% de las interacciones: mover ese número equivale a mover a dos docenas de personas. La métrica de salud es **la forma de la distribución**.
3. **No usar calidad percibida (thumbs up/down) como KR.** La tasa de feedback explícito es del **1,5%**; el ratio 9:1 a favor mide quién se molesta en calificar, no si MAIA es buena. Requiere instrumentar otra cosa.
4. **No confundir alcance con intensidad.** Son dos palancas separables que responden a tipos de release distintos (→ `08-roadmap`). Un solo número no las captura, así que un KR único los promedia y esconde el movimiento real.
5. **No leer el alcance de Risk Management como alcance de MAIA.** ⬅️ _nueva (2026-08-18), y la más consecuente de las cinco._ En jul-26, **234 de los 373 usuarios de MAIA (63%) entran por un banner de riesgo**, y aportan el 21% de las interacciones. Si el KR de penetración se fija sobre el 11,6% agregado, **dos tercios de ese número los mueve una feature de superficie**: el KR puede subir o bajar porque Risk Management funciona —o se rompe— y no porque cambie la adopción de MAIA. **El KR necesita cortes separados por origen** (`AI_CHAT_OPEN` con `option = risk_banner` vs. el resto). Baseline propio de Risk Management: **⏸️ en pausa** — ver `06-kpi-tree`; el 7,3% que estuvo cargado usaba el denominador equivocado.
   _Precisión del 2026-08-18: el corte **no** es entre "conversación real" y "click de superficie" —los cuatro eventos que se totalizan son conversación con respuesta generada—, sino entre **quién formula la consulta**. `AI_CHAT_SEND` es demanda que el usuario articuló con sus palabras; FAQ, banner y respuesta sugerida son **demanda inducida por rieles que construimos nosotros**. Un KR agregado no deja ver cuál de las dos se movió, y son palancas de producto distintas: la primera se mueve construyendo **capacidad**, la segunda construyendo **superficie** (→ el eje abierto en `08-roadmap`)._
   _Refuerzo del 2026-08-19: el 63% de julio **no es un pico, es el valor más bajo de los tres meses** (54% en mayo, 72% en junio). La dependencia es mayor de lo que sugería el número que motivó esta anti-meta._

### Dos huecos que la estrategia tiene que cubrir

**Ninguna métrica actual mide valor entregado, solo uso.** Nada de lo medido dice si una interacción cambió una decisión operativa, evitó un desvío o protegió un margen.

Hay **dos candidatos** para cerrar ese hueco, y los dos existen en el producto sin registrarse:

1. El evento de **aprobación explícita de acciones** del pilar de Governance.
2. ⬅️ _nuevo (2026-08-18)_ **La acción aplicada desde una respuesta de riesgo.** Risk Management ofrece **acciones masivas reales** —asignar colaboradores, mover deadlines, reasignar tareas— y **no existe ningún evento que registre si alguien las aplica**. Es el mejor lugar del producto para instrumentar valor entregado: a diferencia de Governance, **la acción está pegada a un desvío concreto y medible**, así que permite cerrar el loop "hubo un riesgo → alguien hizo algo → el riesgo se resolvió".

> **Por qué esto es estratégico y no técnico:** la hipótesis de `08-roadmap` dice que lo que predice disposición a pagar es que MAIA **ejecute trabajo**, no que se consulte. Risk Management es donde MAIA más cerca está de ejecutar trabajo, y es justo lo que no se mide.

**El portafolio de la vertical de AI está medido a medias: tres features con baseline, una sin instrumentar.** _(Corregido el 2026-08-18, tres veces: este bloque decía primero que "no tiene ninguna métrica", después encuadraba el problema como "fuera de MAIA", y hasta hoy contaba dos features medidas en lugar de tres. MAIA es un miembro del portafolio, no el portafolio — ver la tabla en `01-producto`.)_

- **Marketplace (agentes custom) sí tiene baseline:** 57 companies habilitadas, **1,40% de penetración en jul-26 con intensidad 17,7** — poca gente muy metida, el perfil inverso al de MAIA. Pero **es consumo, no creación**: el funnel de creación de agentes está instrumentado y sin pullear, así que no se sabe si la penetración baja viene de que no se crean agentes o de que los creados no se usan.
- **Risk Management tiene medición propia** desde el 2026-08-18, aunque **su penetración quedó ⏸️ en pausa el 2026-08-19** (usaba el denominador de MAIA; el valor real está acotado entre 7,2% y 13,4% — ver `06-kpi-tree`). Lo que **sí** está medido y no depende de ese corte: aporta **54-72% de los usuarios mensuales de MAIA y solo 19-32% de las interacciones** —puerta de entrada, no puerta de paso—, intensidad plana en ~2,0, y **las 79 companies habilitadas en julio no movieron el conteo de usuarios**. **Sale de la lista de features sin outcome por la parte de alcance** —hay serie, aunque falte el denominador correcto— y **queda adentro por la de valor entregado**, que sigue sin instrumentar (ver arriba).
- **Solo workflows / automatizaciones no tienen ninguna métrica.** Entregan valor en **trabajo ejecutado**, no en consultas — un chat se evalúa razonablemente por frecuencia de uso, un workflow automatizado no.

> ⚠️ **Marketplace no se puede sumar ni comparar de frente contra MAIA:** otra base habilitada (57 companies contra 128), otro universo de roles (incluye Colaborador) y una definición de interacción más estricta. Detalle en `06-kpi-tree`.

### Modelo de negocio de MAIA — estado real

MAIA es **gratuita para toda la base de beta testers** (128 companies al 13-ago-2026). El **único revenue** asociado proviene de un servicio de **consultoría de AI** ejecutado entre Producto y CSM, cobrado como extra por licencia sobre tres clientes que ya son de COR (Sancho BBDO, Publicis, Robin). **No hay todavía casos de upsell de licencias por uso de MAIA** fuera de ese marco.

> **Tensión de pricing a resolver:** el servicio se cotiza **por licencia**, pero produce 1 a 3 usuarios muy profundos por cuenta en lugar de adopción amplia — las cuentas de Sancho tienen la intensidad más alta de toda la base (10 y 20 interacciones por usuario) con penetración de 1,5% y 3,8%. Si eso se sostiene, **el valor entregado y el precio cobrado se apoyan sobre bases distintas**. Marcado como hipótesis en `06`: n = 4 cuentas.
>
> **Hipótesis asociada, con muestra de tres:** los tres contratos se cerraron en momentos en que MAIA **pasó de responder a accionar** (Sancho justo después del MVP de la tool para crear tareas; Publicis y Robin con el bloque de tools de acción ya maduro). Si se sostiene, la variable que predice disposición a pagar no sería cuánto se usa MAIA sino **si ejecuta trabajo**. → `08-roadmap`.

### Decisiones abiertas de la vertical de AI

| Decisión | Evidencia disponible |
|---|---|
| ~~¿Cuál es la meta de penetración?~~ ✅ **Resuelta el 2026-08-19: 25% sobre el panel Enterprise + Midmarket** (KR1 de O2). **Queda abierta la mitad de la pregunta:** ¿es la misma para los tres roles? | El KR se fijó como número único; la **anti-meta 1 pide metas diferenciadas**. C-Level 5 meses entre 9,5% y 13,3%; PM de 1,8% a 11,9%; techo observado Crowe Global 23,6% |
| ¿Cómo se reparte capacidad entre construir **capacidades** y construir **superficie**? | Ver `08-roadmap`: abril (capacidades) movió intensidad y no alcance; mayo (superficie) duplicó alcance |
| ~~¿Qué se hace con los **543 asientos dormidos**?~~ ✅ **Resuelta el 2026-08-19: es el KR4 de O2** — 6 de 8 cuentas a ≥20% de penetración con ≥4 int./usuario, con CSM dedicado. **Sujeta a la verificación de churn**, que ahora bloquea un KR | 8 cuentas, 543 asientos, 18 usuarios, intensidad 1 a 2,2. Crowe Global, escala y antigüedad similares, llegó a 23,6% |
| ~~¿Se **libera MAIA a toda la base**, y bajo qué criterio?~~ ✅ **Cerrada el 2026-08-19 — pero no por Producto.** Se libera **la semana del 24-ago-26 a toda la base (~300 clientes, ~172 companies nuevas)**, e incorpora al Colaborador. La decisión se tomó **fuera del área**, así que la cobertura deja de ser una variable que Producto controla — por eso O2 pasó de "adopción activada" a **"adopción validada"** | La evidencia que aconsejaba lo contrario **sigue en pie y ahora es riesgo, no argumento**: 12% de las cuentas habilitadas nunca registró un usuario, y las 79 companies de julio de Risk Management aportaron **cero usuarios netos**. Liberar multiplica el denominador sin evidencia de que mueva el numerador: la penetración cae de 11,6% a **~2,6% el mismo día sin que nada empeore**. De ahí el panel E+MM como denominador y el KR3 de cohorte |
| ¿Cuál es la propuesta de valor para el rol **Colaborador**? | **El acceso ya existe** (header y tareas, desde el Orquestador) y **con el release entra a la base completa**. Falta la propuesta de valor y la métrica. **Decidido el 2026-08-19: va a ficha propia con denominador separado** — ~15 usuarios recurrentes sobre 5.605 asientos = **0,27%**, dos órdenes de magnitud por debajo de los roles con caso de uso definido. **Su primer paso no es un KR sino discovery:** 15 personas usándola son 15 entrevistas posibles (→ `07-discovery`) |
| ¿Cuál es el **modelo de negocio** de MAIA fuera de la consultoría? | El único revenue actual produce 1 a 3 usuarios profundos por cuenta. Hay cuentas gratuitas con penetración muy superior |
| ¿Qué rol juega la **elección de modelo**? | El cambio a Sonnet 4.5 en marzo coincide con el segundo mayor salto de penetración de la serie (→ `01-producto`) |
| ¿Cómo se miden las **otras features del portafolio**? | Marketplace ya tiene baseline de consumo (1,40% jul-26); le falta la **creación**. **Risk Management tiene serie de alcance, pero su penetración está ⏸️ en pausa** (denominador propio pendiente); le falta además el valor entregado. Solo workflows sigue sin ninguna métrica |
| ¿**Risk Management va a GA**, y con qué condición? | **Recomendación de Producto: no está en condiciones**, no por falta de features sino porque **cuatro cálculos de nivel proyecto producen porcentajes imposibles** y **la severidad no discrimina** (el desvío promedio supera el umbral Alto en las diez métricas que lo tienen configurado; la undécima no tiene umbral cargado). Detalle en `06-kpi-tree`, encuadre de roadmap en `08`. ⚠️ **La pregunta se volvió más urgente el 2026-08-19:** con el release a ~300 clientes, esa deuda **se expone a toda la base** haya GA o no, y se decidió **no cubrirla con un KR** — su prioridad queda apoyada en convicción, no en medición |
| ¿Qué se hace con **Marketplace**? ¿Es una apuesta de producto o una feature de nicho? | 57 companies habilitadas, 1,40% de penetración en jul-26. **MullenLowe Delta es el 87% de las interacciones** y una sola persona ahí explica ~un tercio del volumen total. **36 de 57 companies nunca registraron un usuario** (49% de los asientos). El Director es el único rol con penetración de dos dígitos (29,1%, sobre 55 asientos — señal, no magnitud). Falta todo el dato de creación de agentes |

## OKRs del trimestre

> ✅ **Cargados el 2026-08-19 — vertical de AI, ciclo Q4 2026** (algunas metas cierran en Q1 2027). Son los **primeros OKRs de producto de COR**: MAIA se construyó hasta hoy sin outcomes, sin OKRs y sin KRs. Este set parte de un baseline real de diez meses de datos, todo en `06-kpi-tree`.
>
> ⚠️ **Los otros ejes/squads siguen sin OKRs** (`02-equipos`: Coherencia de dinero y negocio, Coherencia de datos, Fundamentals COR, GGN-GUT). Cargar acá apenas estén definidos.

### Cómo se relacionan los tres objetivos

```
O1 EJECUCIÓN        ──habilita──>  O2 ADOPCIÓN  ──habilita──>  O3 REVENUE
   CONFIABLE                        (si falla, no hay          (en revisión)
   (si falla, escalar                a quién cobrarle)
    amplifica el problema)
```

**No es una cascada.** Buena parte corre en paralelo, pero la dependencia importa: **escalar un producto poco confiable multiplica los defectos por el tamaño de la base**, y no se le puede poner precio a algo que la base no usa.

> ⚠️ **Tensión conocida entre O1 y O2, declarada de antemano.** Recalibrar la calidad de las detecciones de riesgo —trabajo que vive bajo O1 **como iniciativa y no como KR**, ver el hueco declarado en la sección de O1— hará que **se disparen menos alertas**, y eso puede **bajar el alcance de MAIA** en el corto plazo — una buena noticia con forma de mala. Tiene fundamento medido: entre **54% y 72%** de los usuarios mensuales de MAIA entran por un banner de riesgo (anti-meta 5). **Leer los números de O2 de los primeros meses con esto puesto.**

---

### O1 — Ejecución confiable de la vertical de AI

> 🔄 **Reescrito el 2026-08-21. Este bloque reemplaza al O1 cargado el 2026-08-19.** Pasa de **cinco KRs a cuatro**: se **retiran tres** (precisión verificada, conversión de apertura, tickets por 100 usuarios activos) y **entran dos nuevos** (flujo de archivos, performance). El registro de los retiros y el mapeo de IDs están al final de la sección.
>
> 📌 **Cambió el título.** El objetivo se llamaba *"Confiabilidad y calidad"*. **Al retirarse la precisión verificada, calidad-como-verdad dejó de estar cubierta** y el título prometía más de lo que el set mide.

**Qué persigue:** que MAIA **entregue el trabajo que promete** — que sepa responder dentro de su dominio, que **ejecute** lo que aprueba el usuario, que **produzca los artefactos** que se le piden, y que todo eso **se sienta rápido**.

**Por qué ahora:** **la semana del 24 de agosto MAIA se libera a toda la base de COR (~300 clientes).** La deuda de calidad deja de ser algo a resolver *antes* de escalar y pasa a **exponerse a toda la base**. Las cuentas nuevas además no llegan con expectativas neutras: la base actual tiene **NPS −27,8** y **95% de menciones negativas sobre performance** (`07-discovery`, I-01 y siguientes).

| # | KR | Baseline | Meta | Estado del instrumento |
|---|---|---|---|---|
| **KR1** | **Cobertura de respuesta** — % de consultas **dentro de dominio** resueltas con datos, sin derivar a "no tengo esa información" | sin cargar | **75%** ⚠️ | 🟠 método definido, **sin cadencia** |
| **KR2** | **Éxito de ejecución** — % de acciones aprobadas que se completan **sin errores del sistema** | sin cargar | **80% en Q4 → 95% en Q1** ⚠️ | 🔴 evento a construir |
| **KR3** | **Éxito del flujo de archivos** — % de **sesiones con archivo** que terminan con el artefacto entregado | sin cargar | **80%** ⚠️ | ⛔ sin instrumentar y **sin spec** |
| **KR4** | **Performance** — % de consultas con **primer token en menos de 3s** | referencia 1,5–2,5s (no es baseline) | **≥95%** ⚠️ | 🟢 el único con referencia numérica |

> ⚠️ **Las cuatro metas son provisorias, y esto no es una salvedad de forma.** Se fijaron **por criterio, no contra una medición**: **ninguno de los cuatro KRs tiene baseline cargado.** Cada meta se recalibra contra su primer baseline. **Ningún número de esta tabla es un dato medido de MAIA.**
>
> ⚠️ **Expectativa declarada de antemano — cambió respecto del 19-ago.** Antes decía "el Q4 de O1 produce baselines, no mejoras". La versión precisa es: **tres de los cuatro KRs necesitan instrumentación que hoy no existe, así que el Q4 de O1 es, en los hechos, construir tres instrumentos con metas ya puestas.** Si no se dice ahora, **en enero los cuatro números van a leerse como resultados incumplidos en lugar de metas recalibradas.**

#### KR1 — MAIA sabe lo que debería saber

**Cobertura de respuesta: 75% de las consultas resueltas con datos.**

- **Scope: solo consultas dentro de los dominios de MAIA.** ⚠️ **Decisión pendiente y no cosmética:** si el scope se define por **entidades** (Tarea, Proyecto, Cliente, Horas) o por **especialistas** (Proyectos, Tareas, Clientes). **Horas no es un especialista** — la regla de dominio dice que las consultas de horas las resuelve el Especialista en Proyectos. **Elegir una y escribirla**, porque el denominador del KR depende de eso.
- **Instrumento:** corrida sistemática del análisis de fricciones. **Método ya definido; falta cadencia.**
- **Distingue dos problemas que suelen confundirse:** que MAIA responda **mal** y que MAIA **no pueda** responder. Este KR mide el segundo. _(El primero ya no lo mide nadie — ver el hueco declarado al final de la sección.)_
- **Cada consulta sin respuesta es una funcionalidad que falta**, así que el mismo trabajo produce el KR **y** el input de roadmap: el volumen de consultas **fuera de dominio** no es fallo del KR, es el pedido de features → `08-roadmap`.

> 📌 Para calcular el 75% hay que **clasificar cada consulta como dentro o fuera de dominio**. Las de afuera **no se descartan.** Cortes del KPI en `06-kpi-tree`.

#### KR2 — MAIA hace lo que dice que va a hacer

**Éxito de ejecución: 80% de las acciones aprobadas se completan sin errores del sistema.**

- **Criterio:** *errores del sistema*, **no** "el usuario no quería eso". **Fallo técnico, no desacierto de intención.**
- **Escalón declarado: 80% en Q4, camino a 95% en Q1.** El 95% es el umbral estándar para operaciones que modifican datos del cliente; **el 80% es un escalón intermedio, no la vara definitiva.** _(El 19-ago este KR estaba cargado directamente como ≥95%.)_
- **Instrumento:** evento de acción aplicada, con la spec ya acordada (IDs de entidades o `batch_id`; **sin evento de "acción revertida"** — ver pendientes).
- 🔴 **Es la pieza más apalancada del árbol.** El mismo evento alimenta este KR, **dos KRs futuros de O3** y **una condición de salida de beta de Risk Management**. **Si una sola cosa arranca ya, es esta.**

#### KR3 — MAIA entrega los archivos que promete

**Éxito del flujo de archivos: 80% de las sesiones con archivo terminan con el artefacto entregado.**

- **Unidad: la sesión** (= conversación). El contexto de MAIA es fijo por conversación, así que **la ventana de observación es la conversación entera, sin límite de tiempo**.
- **Criterio de éxito — las tres condiciones:** artefacto entregado **+** sin error técnico **+ sin señal de corrección** en la misma conversación. Cuenta como corrección: **re-adjuntar el mismo archivo, repetir el mismo pedido, o corregir explícitamente en el turno siguiente**.
  > ⚠️ **El criterio hace al número.** Con "sin corrección" adentro, **80% es exigente**. Si el equipo lo instrumenta como "no tiró error", **el mismo 80% es casi trivial**. **El criterio va siempre al lado de la meta** — en el review, en el dashboard y en cualquier lugar donde se cite el 80%.
- **Dos líneas desde el primer mes, no una:** **entrada** (adjuntar e interpretar) y **salida** (generar documento). Son direcciones opuestas con fallas distintas —parseo e interpretación de un lado; formato, completitud y fidelidad del otro—. **Separarlas después es carísimo: el corte por origen del banner es el precedente.** Detalle en `06-kpi-tree`.
- ⛔ **Sin instrumentar y sin spec.** Es el KR más atrasado del set.

> ⚠️ **Evidencia: `[HIPÓTESIS]` hasta la primera corrida.** **No hay ni un dato de este flujo en el repo.** La señal más cercana —archivos, **25 menciones, 96% negativas** (`07-discovery`, I-07)— es de **adjuntos en tareas de COR, no de MAIA**, y **no se cita como evidencia de este KR**. Hoy la existencia del KR se apoya en **observación cualitativa, no en medición**.
>
> 📌 **Hay un número que no es un driver y hay que mirar igual: el volumen del flujo sobre el total de sesiones.** No explica por qué el KR se mueve — **valida que el KR debía existir.** Si vuelve marginal, **lo que se revisa no es el driver: es el KR.**

#### KR4 — MAIA responde rápido

**Performance: ≥95% de las consultas con primer token en menos de 3 segundos.**

- **Por qué TTFT y no otra cosa:** es el único indicador de performance **casi insensible a la complejidad de la consulta**. Lo que varía con la complejidad es el largo de la respuesta y el trabajo posterior; **el TTFT mide el camino previo**. Y es lo que el usuario percibe como *"¿esto está vivo?"* — **que es donde abandona**.
- **Referencia disponible: promedio actual de 1,5–2,5s.** ⚠️ **No es baseline todavía:** es un **promedio**, y un promedio es perfectamente compatible con **una cola larga que el KR sí castigaría**.
- **De dónde sale el 3s:** margen razonable por encima del techo del rango actual, **para que el KR se rompa ante una degradación real y no por ruido**.
- 🟢 **El único KR del set con referencia numérica y con drivers ya medibles.** Y es el único que ataca de frente el **95% de menciones negativas sobre performance** con el que la base llega al release.

> ⚠️ **Chequeo previo obligatorio — antes de convertir el 1,5–2,5s en baseline.** El **Orquestador se deployó el 22-jul-2026** y **agregó un hop antes del primer token**. Si la medición del 1,5–2,5s es anterior a esa fecha, **es de otra arquitectura y no sirve como referencia**. Y si hay mediciones **a ambos lados** de esa fecha, **la resta es el costo en latencia del Orquestador** — dato directamente relevante para el eje **capacidad vs. superficie** de `08-roadmap`, donde el Orquestador es test en curso y **hoy apunta en contra**.

#### Registro de los tres KRs retirados

_Se registran en vez de borrarse. **Los IDs de los KRs retirados no se reutilizan como referencia histórica** — ver la nota de numeración abajo._

| KR retirado | Fecha | Motivo |
|---|---|---|
| **Precisión verificada** _(era O1-KR1)_ | 2026-08-21 | Requería **muestra manual mensual** cotejada contra el backend, **sin forma automática**, y **nunca tuvo dueño asignado**. Era el KR más caro del set y **sin dueño no iba a tener dato** |
| **Conversión de apertura** _(era O1-KR4)_ | 2026-08-21 | ⚠️ **No falla el test de "resultado vs. entregable"** que se usó para bajar otros candidatos a iniciativa. **Se retira para no sostener cinco KRs en un objetivo que nace sin instrumentar.** _Motivo propio, escrito para que no parezca arbitrario_ |
| **Tickets por 100 usuarios activos** _(era O1-KR5)_ | 2026-08-21 | Métrica **descendente** cuya meta **no puede fijarse sin baseline** sin quedar indefinida **en la dirección peligrosa** |

> ⚠️ **Nota de numeración — colisión declarada.** El documento fuente numera los cuatro KRs vivos como **KR1 a KR4** y a la vez enuncia la regla "los IDs no se reutilizan". **Las dos cosas no pueden ser ciertas al mismo tiempo:** el viejo KR1 era precisión verificada y el nuevo KR1 es cobertura de respuesta. **Se carga la numeración del documento fuente (KR1–KR4)** para que el repo coincida con él, y **el mapeo queda escrito acá abajo**. Cualquier acta, dashboard o review anterior al 2026-08-21 que diga "O1-KR3" está hablando de otro KR.

| Referencia vieja (hasta 19-ago) | Referencia nueva (desde 21-ago) |
|---|---|
| O1-KR1 · Precisión verificada | **retirado** — sin equivalente |
| O1-KR2 · Cobertura de respuesta | **O1-KR1** |
| O1-KR3 · Éxito de ejecución | **O1-KR2** |
| O1-KR4 · Conversión de apertura | **retirado** — sin equivalente |
| O1-KR5 · Tickets por 100 usuarios | **retirado** — sin equivalente |
| — | **O1-KR3** · Éxito del flujo de archivos *(nuevo)* |
| — | **O1-KR4** · Performance *(nuevo)* |

#### 🚫 Lo que queda sin cobertura de medición

**Ningún KR de O1 mide si MAIA dice la verdad.** Los cuatro miden si **hizo** algo; **ninguno mide si lo que hizo era correcto.** El caso concreto: responde con datos de dominio ✅, ejecuta sin error ✅, genera el documento ✅ — **y los números están mal. El objetivo marca verde perfecto.**

**No es hipotético:** cuatro cálculos de nivel proyecto de Risk Management producen **porcentajes imposibles** (hasta 24.814.759.071%) y **la severidad no discrimina** — el desvío promedio ya supera "Alto" en las diez métricas configuradas, así que **"Alto" es el estado por defecto**. Se decidió no cubrirlo con un KR: sigue como **iniciativa** (→ `08-roadmap`).

> **Se registra con el mismo lenguaje que la deuda de cálculos: su prioridad se apoya en convicción y no en medición** — justo cuando el release la expone a ~300 clientes. **Ahora son dos cosas en esa lista, y son la misma cosa.**

#### Regla de método que aplica a todo el set

⚠️ **Regla 4 de la convención de fuentes: no dividir una fuente por otra.** Varios de los desgloses de estos cuatro KRs son tentadores de armar cruzando **Amplitude con Metabase**. **Cada corte tiene que vivir dentro de una sola fuente.** Es una de las dos reglas que más se rompen.

⚠️ **Todo corte se reporta con su `n` y su fecha.** Un 41% sobre 12 sesiones no es lo mismo que sobre 900, y **post-release toda serie cruza el cambio de denominador**.

⚠️ **Regla 8: toda serie declara evento, filtro y valores incluidos.** **Ningún KR de este set se puede reportar sin su fila en el mapa de instrumentación de `06-kpi-tree`.**

---

### O2 — Adopción validada y valor demostrado en Enterprise y Midmarket

**Qué persigue:** demostrar que MAIA funciona para quien tiene motivo de usarla — que **alcanza**, que **sirve**, y que **habilitarla produce uso real**.

**Por qué el título cambió.** El objetivo original hablaba de *adopción activada* y contemplaba metas de cobertura. **Con el release a toda la base decidido por fuera de Producto, la cobertura deja de ser una variable que el área controla.** Lo que queda por demostrar es la **validación**.

**Lo aprovechable del release:** **172 companies entrando el mismo día es el experimento de activación más grande que COR va a correr.** Un caso equivalente en julio —79 companies habilitadas de golpe en Risk Management— **no sumó ningún usuario neto y nadie lo instrumentó**. Si esta vez se mide por cohorte, en octubre hay respuesta a una pregunta hoy abierta.

| # | KR | Baseline | Meta |
|---|---|---|---|
| **KR1** | **Alcance** — penetración sobre el panel Enterprise + Midmarket | **11,6%** ⚠️ | **25%** |
| **KR2** | **Retorno** — % de usuarios con una sola interacción en el mes *(baja mejor)* | **35,8%** | **≤25%** |
| **KR3** | **Activación de cohorte** — % de companies con primer usuario dentro de los 30 días de habilitadas | **~0%** | **40%** |
| **KR4** | **Recuperación de dormidas** — cuentas Enterprise dormidas que alcanzan ≥20% de penetración con ≥4 interacciones por usuario | **3,3%** y ~1,8 int. | **6 de 8 (70%)** |

**Qué valida cada uno:** que MAIA **alcanza** (KR1), que **sirve** (KR2), que **habilitar produce uso** (KR3) y que **lo dormido se puede despertar** (KR4).

> 📌 **Lectura conjunta:** si KR1 y KR3 se cumplen pero KR2 no, **hay alcance sin valor** — y es exactamente lo que O3 necesita saber antes de poner precio.

#### ⏰ Dos cosas que deben ocurrir ANTES del release

1. **Congelar el panel de referencia Enterprise + Midmarket** — la lista de companies y asientos elegibles del día previo. Sin esto **se pierde la capacidad de distinguir *mejora* de *dilución*** durante los próximos meses. Cuesta una consulta ahora; después hay que reconstruirlo a mano.
2. **Instrumentar la activación con marca de cohorte** — sin eso **KR3 no existe** y el experimento se pierde.

#### Por qué el denominador es el panel Enterprise + Midmarket

Con el release la base pasa de **128 a ~300 companies** e incorpora el rol **Colaborador**. El universo de asientos elegibles saltaría de ~3.775 a **~15.000**, y **la penetración caería de 11,6% a ~2,6% el mismo día, sin que nada empeore.**

Medir sobre el panel Enterprise + Midmarket (roles PM, Director y C-Level) resuelve tres cosas a la vez:

1. Es el universo que el objetivo nombra en su propio título.
2. **Mantiene la serie comparable:** el 11,6% sigue siendo baseline y los nueve meses de historia siguen sirviendo.
3. Es el universo sobre el que **se va a monetizar**.

**El rol Colaborador va a ficha propia**, con denominador y métrica separados: **~15 usuarios recurrentes sobre 5.605 asientos (0,27%)**. Está dos órdenes de magnitud por debajo de los roles con caso de uso definido, **lo cual es esperable** — el rol todavía no tiene propuesta de valor. Su primer paso **no es un KR de adopción sino discovery**: con 15 personas usándola, son 15 entrevistas posibles (→ `03-personas`, `07-discovery`).

Las **~172 companies nuevas fuera de Enterprise y Midmarket se reportan, pero no llevan meta**: son población nueva sin baseline.

**KR1 — Alcance.** Usuarios únicos sobre asientos elegibles. Es la métrica de la prioridad "Deploy de AI en clientes" del plan de negocio. **Baseline 11,6%** (jul-26), piso conservador: el único sesgo vivo deprime la cifra. Sobre el panel cerrado de cuentas de 2025 —denominador constante— el mismo mes da 14,6%. **Meta 25%:** supera el techo observado hoy, que es **Crowe Global con 23,6%**. Es una **meta de estiramiento consciente** — está fuera de lo que cualquier cuenta de COR alcanzó, pero en el mismo orden de magnitud que algo que **sí ocurrió** en una cuenta real, de alta reciente y escala comparable.

> ⚠️ **Salvedad de denominador — leer antes de evaluar el KR** _(cargada el 2026-08-19)_. **El baseline de 11,6% no se calculó sobre el panel Enterprise + Midmarket**, sino sobre las 128 companies completas, todos los segmentos (373 usuarios ÷ 3.225 asientos al inicio de jul-26). **Los asientos del panel E+MM todavía no existen como dato** — salen del Corte E de `06-kpi-tree`, que sigue sin correr. Se decidió **cargar el 11,6% igual** para que el KR exista la semana del release, pero: si el panel E+MM penetra por encima del promedio —lo esperable, porque Enterprise concentra el uso—, **el baseline real es más alto y la meta de 25% es menos exigente de lo que parece.** Correr el Corte E es lo que convierte esta meta en una meta medida. _(Nota aparte: el documento fuente escribía el baseline como "373 sobre 3.775 asientos"; eso da 9,9%. Los 3.775 son los asientos al 13-ago-26, no los de julio. El 11,6% de la serie es correcto; la aritmética del paréntesis no.)_

**KR2 — Retorno.** Cuánta gente prueba MAIA una vez y no vuelve; baja mejor. Es **la métrica que más se parece a "MAIA agrega valor"** —nadie vuelve a algo que no le sirvió— y mide **la forma de la distribución** en lugar del promedio, que es lo correcto en una base donde el 6% de los usuarios genera ~45% de las interacciones. **Baseline 35,8%:** en julio, **148 de 413 usuarios** hicieron una sola consulta en todo el mes y aportaron ~5% del volumen.

**Meta ≤25%:** es **más exigente de lo que parece**, porque bajar un número se lee como menos ambicioso que subirlo. **Todo usuario nuevo entra por el bucket de una interacción, así que el crecimiento de KR1 alimenta la cola que KR2 tiene que reducir.** Con KR1 cumplido, el 25% implica que **4 de cada 5 personas que prueben MAIA vuelvan una segunda vez**; hoy vuelven 2 de cada 3. Se evaluó 15% y se descartó: habría exigido que volviera el 95%.

> 📌 **Cómo leerlo en un review:** si KR2 queda **entre 25% y 35,8% mientras KR1 crece de forma sostenida, la base mejoró aunque el KR no se haya cumplido.** Sostener la proporción con la base ampliada ya es un avance.
>
> 📌 **Defecto conocido de la métrica:** mezcla a quien probó MAIA por primera vez este mes con quien la usa desde marzo haciendo una consulta mensual. **Solo el segundo caso es mala señal.** La versión limpia —*% de usuarios nuevos que registran una segunda interacción dentro de los 30 días*— requiere instrumentación adicional y **queda como mejora para el ciclo siguiente**.
>
> ⚠️ **Y arrastra un segundo defecto, de universo** _(2026-08-19)_: los **413 usuarios del denominador incluyen al rol Colaborador** —es la única tabla de `06-kpi-tree` que Amplitude no entrega abierta por rol—, mientras que **KR1 mide sobre 373, que lo excluye**. Los dos KRs del mismo objetivo corren sobre universos distintos. Hoy el desvío es chico; **después del release, con el Colaborador entrando en masa, deja de serlo.** Resolverlo pide el histograma abierto por rol, que ya es un pedido abierto en `06`.

**KR3 — Activación de cohorte.** De las companies que se habilitan, cuántas registran su primer usuario dentro de los 30 días: **la medición de si habilitar sirve para algo**. Es el KR diseñado para el escenario post-release y el único que instrumenta el experimento de las 172 companies. **La evidencia disponible es contundente y desalentadora:** en julio se habilitó Risk Management a **79 companies —55 el mismo día— y los usuarios únicos pasaron de 232 a 234. Cero usuarios netos.** Ese es el baseline ~0%. **Meta 40%:** originalmente se planteó 60%, pensando en olas controladas de ~20 cuentas con playbook de activación; **con 172 companies de golpe y sin playbook, 40% es lo realista.**
> ⚠️ **Medir por cohorte mensual, no agregado.** Si se promedia, **el resultado del release queda enterrado.**

**KR4 — Recuperación de cuentas dormidas.** Ocho cuentas Enterprise concentran **543 asientos elegibles (17% del universo)** con solo **18 usuarios activos** e intensidad de 1 a 2,2. No es "uso bajo": es **no-retorno tras el primer contacto**. Es **la mejor relación valor/esfuerzo del set** — llevar esos 543 asientos al promedio son **~45 usuarios activos sin construir nada**, y con ocho cuentas nominables es **una lista de llamadas, no un proyecto**. Su valor relativo **sube justo cuando todo lo demás se diluye por el release**. **Meta 6 de 8 (70%) a ≥20% de penetración con ≥4 interacciones/usuario:** la ambición se apoya en que **habrá un CSM dedicado**. El 20% es ~6x el nivel actual y se acerca al techo histórico de 23,6%, pero **se mantiene dentro de lo observado**; se evaluó 40% y se descartó (12x el nivel actual, 1,7x la mejor cuenta de la historia, sobre cuentas que **ya fallaron una vez**).
> 📐 **El criterio incluye intensidad a propósito.** Con un CSM involucrado, el alcance solo puede inflarse con una sesión de onboarding grupal: 30 personas entran, prueban y no vuelven, y la cuenta "cumple" mientras sigue dormida. **El umbral de 4 interacciones es deliberadamente bajo** (la base está en 6,2) — no pide excelencia, **pide que la gente vuelva**.
>
> ⚠️ **Verificación previa:** confirmar que estas cuentas **no estén inactivas en COR en general**. Si el asiento no existe, el KR es incumplible por motivos ajenos a MAIA. Es el 🔴 de estado de actividad/churn por company que ya está pedido en `06-kpi-tree`, y **ahora bloquea un KR, no solo el dimensionamiento de una iniciativa**.

---

### O3 — Modelo de negocio de AI con revenue propio — ⏸️ EN REVISIÓN

**No se carga con KRs.** Depende de definiciones de **pricing y lógica de venta que no decide Producto**. Se retoma cuando esa definición exista. El estado actual del modelo de negocio y la tensión de pricing están más abajo, en su sección propia.

_Dos de sus KRs futuros dependen del mismo evento de acción aplicada que sostiene el **KR2 de O1** (éxito de ejecución; era el KR3 hasta el 2026-08-21) — otra razón para arrancar por ahí._

---

### Cuatro cosas que registrar sobre este set

_Cargadas el 2026-08-19 al integrar los OKRs al repo. No invalidan el set: son las costuras que hay que mirar en el primer review._

1. **KR1 de O2 es un número único y la anti-meta 1 pide metas diferenciadas por rol.** El set re-enuncia esa anti-meta en sus propios criterios, y aun así fija 25% para el panel entero. **O el KR se desagrega por rol al reportar, o la anti-meta se revisa explícitamente.** El dato que la motiva sigue vivo: el C-Level lleva cinco meses entre 9,5% y 13,3% mientras el PM pasó de 1,8% a 11,9%.
2. **El KR de penetración se fijó con el corte por origen todavía abierto.** Era el único bloqueo declarado en este archivo. **No es un error:** la regla de decisión de `06-kpi-tree` está escrita de antemano y dice que el KR se puede escribir en los dos desenlaces. Lo que el Corte A decide ahora **no es si el KR existe, sino si se reporta en una línea o en dos** (MAIA por chat / MAIA por banner). Sigue siendo la consulta más desbloqueante del repo.
3. **La meta del KR1 se apoya en un baseline de otro universo** — ver la salvedad de denominador arriba. Correr el Corte E la convierte en una meta medida.
4. **Todo KR persigue un resultado, no un entregable.** Se bajaron a iniciativas varios candidatos que eran milestones: instrumentar un evento, corregir cálculos, poner workflows en producción, definir un modelo de negocio. **El trabajo sigue siendo necesario, pero no se mide como resultado** (→ `08-roadmap`).

### Tres costuras que agregó la reescritura de O1

_Cargadas el 2026-08-21. Las cuatro de arriba siguen vigentes y son todas de O2._

5. **La numeración de los KRs de O1 colisiona con su propia regla.** El documento fuente dice "los IDs no se reutilizan" **y** numera los cuatro KRs vivos como KR1–KR4. Se cargó la numeración del fuente con el **mapeo viejo→nuevo escrito** (ver O1). **Toda referencia a "O1-KRn" anterior al 21-ago apunta a otro KR:** actas, dashboards y el propio historial de este repo.
6. **Se retiró el único KR que fallaba por falta de dueño, no por falta de valor.** La precisión verificada era el KR más caro del set y **el retiro cierra un pendiente sin resolverlo**: el hueco de medición de verdad **queda abierto y ahora sin candidato**. Está registrado en O1 como tal, con el mismo lenguaje que la deuda de cálculos.
7. **Dos KRs nuevos nacen con meta y sin evidencia.** El de archivos es `[HIPÓTESIS]` —**no hay ni un dato del flujo en el repo**— y el de performance apoya su referencia en un promedio que puede ser de **otra arquitectura** (Orquestador, 22-jul-26). **Las metas son de criterio; el primer baseline las recalibra.**

## Marco de priorización

Producto prioriza combinando dos ejes:

1. **Alineación a las 3 prioridades del plan** (apertura de nuevos verticales, thought leadership por vertical, deploy de AI en clientes) — una iniciativa pesa más si sirve directamente a alguna de las tres.
2. **Valor vs. esfuerzo** — dentro de lo alineado, se prioriza por relación de impacto esperado sobre costo de implementación.

No es un framework formalizado tipo RICE con scoring numérico, sino un criterio cualitativo de dos ejes.

## Pendientes — input interno

- [x] ✅ **OKRs de la vertical de AI — cargados el 2026-08-19, O1 reescrito el 2026-08-21.** O1 (**ejecución confiable, 4 KRs**) y O2 (adopción validada, 4 KRs); **O3 queda ⏸️ en revisión** por depender de pricing, que no decide Producto. Ver "OKRs del trimestre". _Los cinco bloques de evidencia que sostienen O2 —baseline, anti-metas, distribución, dormidas y Crowe— estaban cargados desde el 17 al 19 de agosto. **Los cuatro KRs de O1, en cambio, no tienen baseline cargado.**_
- [ ] **OKRs de los otros ejes/squads** (Coherencia de dinero y negocio, Coherencia de datos, Fundamentals COR, GGN-GUT) — siguen sin definir. **No inventarlos.**
- [ ] ⏰ **ANTES del release del 24-ago: congelar el panel Enterprise + Midmarket** (companies y asientos elegibles del día previo) e **instrumentar la activación con marca de cohorte**. Sin lo primero se pierde poder distinguir mejora de dilución; sin lo segundo **KR3 de O2 no existe**. Las dos son consultas, no desarrollo. → `06-kpi-tree`.
- [ ] 🔴 **Correr el Corte A (solapamiento MAIA / banner)** — ya no bloquea escribir el KR de penetración, pero **decide si se reporta en una línea o en dos**. Sigue siendo la consulta más desbloqueante del repo. → `06-kpi-tree`.
- [ ] **Resolver la tensión entre KR1 de O2 y la anti-meta 1:** el KR es un número único (25%) y la anti-meta pide metas diferenciadas por rol. **Desagregar al reportar, o revisar la anti-meta explícitamente.** No dejarlo implícito.
- [x] ~~**Asignar dueño con nombre al KR1 de O1 (precisión verificada).**~~ ⚠️ **Cerrado el 2026-08-21 por retiro del KR, no por resolución.** Se retiró justamente porque nunca tuvo dueño y no había forma automática de medirlo. **El hueco que dejó —nadie mide si MAIA dice la verdad— está registrado en la sección de O1 y sigue abierto.**
- [x] ~~**Fijar las metas de los cuatro KRs de O1 que decían "por definir".**~~ ✅ **Cerrado el 2026-08-21: los cuatro KRs tienen meta** (75% · 80%→95% · 80% · ≥95%). ⚠️ **Con la salvedad que reemplaza al pendiente: las cuatro son provisorias, fijadas por criterio y no contra una medición.** Ninguno tiene baseline cargado.
- [ ] 🔁 **Recalibrar las cuatro metas de O1 contra su primer baseline**, y dejar registrado el número viejo al lado del nuevo. **Es el pendiente que sustituye al de "fijar las metas".** Sin esto, en enero los cuatro números se leen como resultados incumplidos.
- [ ] ⚠️ **Definir el scope del KR1 de O1 (cobertura de respuesta): por entidades o por especialistas.** Entidades = Tarea, Proyecto, Cliente, Horas. Especialistas = Proyectos, Tareas, Clientes. **Horas no es un especialista** — la regla de dominio manda esas consultas al Especialista en Proyectos. **El denominador del KR depende de esta elección: hay que elegir una y escribirla.**
- [ ] ⛔ **Especificar e instrumentar los eventos del flujo de archivos (KR3 de O1)** — **entrada y salida como dos líneas desde el primer mes**, con el criterio de éxito de tres condiciones (entregado + sin error + sin señal de corrección). **Es el KR más atrasado del set: sin instrumentar y sin spec.** → `06-kpi-tree`.
- [ ] ⚠️ **Chequear si el 1,5–2,5s de TTFT es anterior al deploy del Orquestador (22-jul-26)** antes de usarlo como baseline del KR4 de O1. **Si lo es, es de otra arquitectura.** Y si hay mediciones a ambos lados, **la resta es el costo en latencia del Orquestador** — insumo del eje capacidad vs. superficie de `08-roadmap`. Pedir además la **distribución p50/p90/p95/p99**: el 3s se fijó sobre un promedio, y un promedio no ve la cola.
- [x] Cómo laddera Producto a "Deploy de AI en clientes": ¿qué métrica de producto la mide? _(Resuelto 2026-08-17: **penetración sobre asientos elegibles**, con metas diferenciadas por rol. Ver sección dedicada. Sigue abierto el laddering de las otras dos prioridades.)_
- [ ] **Definir outcome y meta para lo que del portafolio de AI sigue sin métrica** — entregan valor en trabajo ejecutado, no en consultas, así que la vara de MAIA no les sirve. Queda adentro de esta lista: **workflows/automatizaciones** (sin ninguna métrica), la **creación** de agentes en Marketplace, y el **valor entregado** de Risk Management. _(Marketplace salió por consumo el 2026-08-18; **Risk Management salió por alcance el 2026-08-18**, aunque su penetración quedó en pausa el 2026-08-19 por denominador.)_
  - ⚠️ **Depende de una definición previa, ya resuelta para dos de tres:** Marketplace es feature hermana, **Risk Management es pilar de MAIA con activación separada** (FA propio, pero **exige el FA de Chat de MAIA** — resuelto el 2026-08-18 en `01-producto`). ⚠️ _El fundamento original decía "mismo denominador": **eso es falso** (2026-08-19). Risk Management tiene **base propia de 119 companies**, subconjunto de las 128 de MAIA. La resolución se sostiene por la dependencia del FA, no por el denominador._ **Falta solo workflows.**
- [ ] **Instrumentar el evento de acción aplicada desde una respuesta de riesgo** — junto con la aprobación de Governance, es el camino a medir valor entregado en lugar de uso. Pedido cargado en `06-kpi-tree`.
  - 📐 _**Especificación acordada el 2026-08-19** (esto es la spec, no el outcome — el outcome sigue pendiente arriba): el evento registra **los IDs de las entidades afectadas** o un `batch_id` que las agrupe, **no solo el conteo**. Un evento de "acción revertida" **se propuso y se retiró**, y no por prioridad: las acciones de Risk Management son **ediciones ordinarias** de proyectos y tareas, así que si el producto no tiene un "deshacer", el evento **no tiene nada que lo dispare**. Con los IDs, el retroceso se lee después contra el backend. La **ventana de re-edición no se fija de antemano** (7 / 14 / 30 días): sale de mirar la distribución real. Detalle en `06-kpi-tree`._
  - ⚠️ _Tres preguntas al **squad de AI** condicionan el arranque: si existe un "deshacer" sobre esas ediciones, **si hay registro de backend que permita reconstruir histórico** —si lo hay, el baseline puede arrancar antes del primer mes de instrumentación— y la estimación de la V1. Cargadas en `06-kpi-tree`._
- [ ] **Definir el modelo de negocio de MAIA** más allá del servicio de consultoría, resolviendo la tensión de cotizar por licencia un valor que se concentra en 1 a 3 personas.
- [x] Marco de priorización de Producto. _(Alineación a las 3 prioridades del plan + valor vs. esfuerzo; no es un framework formal tipo RICE.)_
- [x] Propagar la expansión de verticales/EMEA a `03-personas` y `04-mercado`. _(Hecho.)_
