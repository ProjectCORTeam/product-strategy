# 05 — Estrategia y OKRs (COR)

> **Última actualización:** 2026-09-02
> **Owner:** Product Manager, área de Producto
> **Contexto para IA:** Visión, pilares estratégicos, KPIs y OKRs, para priorizar y alinear iniciativas. Base principal: **Business Plan 2026–2027** (presentado internamente). Es un plan de negocio/GTM: fuerte en revenue y go-to-market, liviano en estrategia de producto.
> ✅ **Los OKRs de la vertical de AI están cargados desde el 2026-08-19** — ver "OKRs del trimestre". Son los **primeros OKRs de producto de COR**. Los de las otras verticales y ejes/squads **siguen sin definir: no inventarlos.**
> 🔄 **Revisión completa del set el 2026-08-31 — la más grande desde que se cargó.** **O1 pasa a llamarse "Ejecución sin fallas"** y baja a **tres KRs** (se retira el flujo de archivos). **O2 se toca por primera vez desde el 19-ago:** cuatro KRs sobre **dos universos**, con dos retiros (activación de cohorte, dormidas) y dos altas (**percepción de valor**, **sustitución del flujo de horas**). **Entran tres baselines medidos** —fricciones **50%**, éxito de ejecución **85%**, uso intensivo **8,19%**— y el horizonte queda declarado: **Q4 = sep–dic, revisión mensual, cierre en diciembre.** **O3 sigue ⏸️ sin cambios.**
> 🔄 **El KR1 de O1 se redefinió el 2026-08-27:** pasa de **cobertura de respuesta (75%)** a **conversaciones limpias** — % de conversaciones sin fricción de tipo `bug`, `nlu` o `incompleta`, **meta a fijar contra la primera corrida** y **críticas = 0** como meta propia. **Deja de medir alcance de capacidades y pasa a medir calidad de ejecución.** KR2, KR3 y KR4 no se tocaron; **O2 y O3 tampoco.**
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
| ~~¿Qué se hace con los **543 asientos dormidos**?~~ ⏸️ **Reabierta el 2026-08-31.** Fue el KR4 de O2 entre el 19 y el 31 de agosto (6 de 8 cuentas a ≥20% con ≥4 int./usuario y CSM dedicado); **el KR se retiró** porque **la ventana del Colaborador es ahora**. **Las 8 cuentas siguen nombrables, siguen siendo 543 asientos con cero desarrollo, y vuelven como candidato a KR en Q1 2027** | 8 cuentas, 543 asientos, 18 usuarios, intensidad 1 a 2,2. Crowe Global, escala y antigüedad similares, llegó a 23,6% |
| ~~¿Se **libera MAIA a toda la base**, y bajo qué criterio?~~ ✅ **Cerrada el 2026-08-19 — pero no por Producto.** Se libera **la semana del 24-ago-26 a toda la base (~300 clientes, ~172 companies nuevas)**, e incorpora al Colaborador. La decisión se tomó **fuera del área**, así que la cobertura deja de ser una variable que Producto controla — por eso O2 pasó de "adopción activada" a **"adopción validada"** | La evidencia que aconsejaba lo contrario **sigue en pie y ahora es riesgo, no argumento**: 12% de las cuentas habilitadas nunca registró un usuario, y las 79 companies de julio de Risk Management aportaron **cero usuarios netos**. Liberar multiplica el denominador sin evidencia de que mueva el numerador: la penetración cae de 11,6% a **~2,6% el mismo día sin que nada empeore**. De ahí el panel E+MM como denominador y el KR3 de cohorte |
| ¿Cuál es la propuesta de valor para el rol **Colaborador**? | **El acceso ya existe** (header y tareas, desde el Orquestador) y **con el release entra a la base completa**. Falta la propuesta de valor y la métrica. **Decidido el 2026-08-19: va a ficha propia con denominador separado** — ~15 usuarios recurrentes sobre 5.605 asientos = **0,27%**, dos órdenes de magnitud por debajo de los roles con caso de uso definido. **Su primer paso no es un KR sino discovery:** 15 personas usándola son 15 entrevistas posibles (→ `07-discovery`) |
| ¿Cuál es el **modelo de negocio** de MAIA fuera de la consultoría? | El único revenue actual produce 1 a 3 usuarios profundos por cuenta. Hay cuentas gratuitas con penetración muy superior |
| ¿Qué rol juega la **elección de modelo**? | El cambio a Sonnet 4.5 en marzo coincide con el segundo mayor salto de penetración de la serie (→ `01-producto`) |
| ¿Cómo se miden las **otras features del portafolio**? | Marketplace ya tiene baseline de consumo (1,40% jul-26); le falta la **creación**. **Risk Management tiene serie de alcance, pero su penetración está ⏸️ en pausa** (denominador propio pendiente); le falta además el valor entregado. Solo workflows sigue sin ninguna métrica |
| ¿**Risk Management va a GA**, y con qué condición? | **Recomendación de Producto: no está en condiciones**, no por falta de features sino porque **cuatro cálculos de nivel proyecto producen porcentajes imposibles** y **la severidad no discrimina** (el desvío promedio supera el umbral Alto en las diez métricas que lo tienen configurado; la undécima no tiene umbral cargado). Detalle en `06-kpi-tree`, encuadre de roadmap en `08`. ⚠️ **La pregunta se volvió más urgente el 2026-08-19:** con el release a ~300 clientes, esa deuda **se expone a toda la base** haya GA o no, y se decidió **no cubrirla con un KR** — su prioridad queda apoyada en convicción, no en medición |
| ¿Qué se hace con **Marketplace**? ¿Es una apuesta de producto o una feature de nicho? | 57 companies habilitadas, 1,40% de penetración en jul-26. **MullenLowe Delta es el 87% de las interacciones** y una sola persona ahí explica ~un tercio del volumen total. **36 de 57 companies nunca registraron un usuario** (49% de los asientos). El Director es el único rol con penetración de dos dígitos (29,1%, sobre 55 asientos — señal, no magnitud). Falta todo el dato de creación de agentes |

## OKRs del trimestre

> ✅ **Cargados el 2026-08-19 — vertical de AI, ciclo Q4 2026.** Son los **primeros OKRs de producto de COR**: MAIA se construyó hasta hoy sin outcomes, sin OKRs y sin KRs. Este set parte de un baseline real de diez meses de datos, todo en `06-kpi-tree`.
>
> ⚠️ **Los otros ejes/squads siguen sin OKRs** (`02-equipos`: Coherencia de dinero y negocio, Coherencia de datos, Fundamentals COR, GGN-GUT). Cargar acá apenas estén definidos.

### Horizonte y calendario

_Cargado el 2026-08-31. **Antes el horizonte estaba declarado como nota general —"ciclo Q4 2026, algunas metas cierran en Q1 2027"— pero no por objetivo, sin cadencia y sin mes de corte por KR, lo que lo volvía no operable.**_

**Período: Q4 2026 = septiembre a diciembre.** Los dos objetivos corren sobre el mismo período, **son de equipo** y por eso su horizonte es trimestral. _(El OKR anual es organizacional y hoy no existe para producto.)_

> 📌 **Son cuatro meses, no tres.** Es una **decisión propia** y queda escrita **para que nadie lo lea como un error de conteo** al comparar contra la cadencia de la guía.

**Revisión de los KRs: mensual.**

| Mes | Qué se hace |
|---|---|
| **Septiembre** | **La revisión más cargada del trimestre:** primera corrida del KR de fricciones · **completar el punto de partida de performance** · **recalibrar las metas en las dos direcciones** · declarar los Roofshot/Moonshot pendientes |
| **Octubre** | **Los siete leading declarados** + los KRs que ya dan lectura mensual |
| **Noviembre** | Ídem. ⚠️ **Es el último mes en que un leading todavía permite corregir el trimestre** |
| **Diciembre** | Revisión mensual **= cierre de trimestre.** Resultado final y creación de los OKRs de Q1 2027 |

> ⚠️ **El cierre es en diciembre, no en enero.** El repo hablaba en varios lugares de *"leer los números en enero"*; **con esta cadencia eso queda desactualizado** — y si el cierre se corre a enero, **el diseño de Q1 2027 arranca tarde.**

**Septiembre produce baselines, no resultados — y está adentro del período.** Declarado de antemano: los números de septiembre de los KRs sin instrumento **no son resultados, son la primera medición**, y **las metas puestas por criterio se recalibran en la revisión del 30 de septiembre**.

### Cómo se relacionan los tres objetivos

```
O1 EJECUCIÓN        ──habilita──>  O2 ADOPCIÓN  ──habilita──>  O3 REVENUE
   SIN FALLAS                       (si falla, no hay          (en revisión)
   (si falla, escalar                a quién cobrarle)
    amplifica el problema)
```

**No es una cascada.** Buena parte corre en paralelo, pero la dependencia importa: **escalar un producto poco confiable multiplica los defectos por el tamaño de la base**, y no se le puede poner precio a algo que la base no usa.

> ⚠️ **Tensión conocida entre O1 y O2, declarada de antemano.** Recalibrar la calidad de las detecciones de riesgo —trabajo que vive bajo O1 **como iniciativa y no como KR**, ver el hueco declarado en la sección de O1— hará que **se disparen menos alertas**, y eso puede **bajar el alcance de MAIA** en el corto plazo — una buena noticia con forma de mala. Tiene fundamento medido: entre **54% y 72%** de los usuarios mensuales de MAIA entran por un banner de riesgo (anti-meta 5). **Leer los números de O2 de los primeros meses con esto puesto.**

#### Laddering a nivel KR — `[HIPÓTESIS]`

_Cargado el 2026-08-31. **El repo tenía la flecha a nivel objetivo —O1 habilita O2— pero no decía qué KR predice qué KR.** Esa es la parte operable._

```
O1 · Fricciones por error ──────┬──▶ O2 · Uso intensivo
                                ├──▶ O2 · Percepción de valor
                                └──▶ O2 · Sustitución del flujo de horas

O1 · Éxito de ejecución ────────┬──▶ O2 · Uso intensivo
                                └──▶ O2 · Percepción de valor

O1 · Performance ──────────────────▶ O2 · Alcance
                                     (vía conversión apertura → primera consulta)

           ── y en sentido contrario ──

O2 · Alcance cumplido ─────────────▶ presiona O1 · Performance
O1 · recalibrar detecciones ───────▶ presiona O2 · Alcance
```

| Conexión | El mecanismo |
|---|---|
| **Fricciones → Uso intensivo** | Al usuario cuya primera conversación se rompe **no lo trae de vuelta ningún onboarding**. Es la conexión más fuerte del mapa |
| **Fricciones → Percepción** | El leading real del NPS está aguas arriba: **quien tiene conversaciones que fallan puntúa peor** |
| **Fricciones → Sustitución del flujo de horas** | Cargar horas es una tarea obligatoria **con un flujo alternativo que ya funciona**. **Si la carga por MAIA falla una vez, el colaborador vuelve al flujo de siempre y no reintenta.** La tolerancia al error acá es más baja que en cualquier otro KR |
| **Ejecución → Uso intensivo** | Quien logró que MAIA hiciera trabajo real vuelve |
| **Ejecución → Percepción** | La hipótesis del roadmap dice que **lo que predice disposición a pagar es que MAIA ejecute trabajo, no que se consulte** |
| **Performance → Alcance** | Si el primer token tarda, el usuario **abre y no pregunta**. Impacta directo sobre *conversión apertura → primera consulta* |

**Por qué importa: es la respuesta a "¿por qué O1 y no features?"** Sin este mapa, O1 es un objetivo técnico que compite con construir features y **se defiende con convicción**. Con él, **los KRs de O1 son los leading de los KRs de O2** — y O2 es lo que pide el plan de negocio.

**Y cambia el orden de lectura:** si el uso intensivo no se mueve **pero las fricciones sí bajaron**, el mecanismo está **retrasado, no roto**.

> ⚠️ **Marcado `[HIPÓTESIS]` a propósito: nadie midió que la fricción cause el no-retorno.**
> **Qué lo refutaría:** que **las fricciones bajen sostenidamente y el uso intensivo no se mueva nada**. Si eso pasa, el problema del no-retorno no es de calidad **y O1 deja de justificarse por esta vía** — y eso es **un hallazgo, no un fracaso**.
> 📌 **El target de discovery *"¿por qué las cuentas grandes probaron MAIA y no volvieron?"* pasa a ser el test de este mapa, no un pendiente suelto** (→ `07-discovery`).

---

### O1 — Ejecución sin fallas de la vertical de AI

> *Que MAIA haga, sin romperse, lo que ya sabe hacer.*

> 🔄 **Renombrado y reducido a tres KRs el 2026-08-31.** El objetivo se llamaba ***Ejecución confiable*** — y antes de eso, hasta el 21-ago, *"Confiabilidad y calidad"*. **Motivo del cambio, el mismo de la vez anterior:** *confiable* prometía que se podía **fiar del output**, y el set **solo garantiza que no se rompe**. El nombre nuevo no promete de más.
>
> 🔄 **Historia del bloque, que no se borra:** reescrito el **21-ago** (de 5 KRs a 4, tres retiros) · KR1 redefinido el **27-ago** (tercera versión) · **renombrado y KR3 retirado el 31-ago**. El registro de los retiros y el mapeo de IDs están al final de la sección.

**Qué persigue:** que MAIA **haga bien lo que ya sabe hacer** — que no falle técnicamente cuando tenía cómo responder, que **ejecute sin romperse** lo que aprueba el usuario, y que **sostenga la latencia mientras la base se triplica**.

**Por qué ahora:** MAIA **se liberó a toda la base la semana del 24 de agosto** (128 → ~300 companies). La deuda de calidad dejó de ser algo a resolver *antes* de escalar: **ya está expuesta a toda la base**, que además llega con **NPS −27,8** y **95% de menciones negativas sobre performance** (`07-discovery`, I-01 y siguientes).

> 🚫 **Lo que este objetivo NO cubre, a propósito y por escrito.**
> **Ningún KR mide si MAIA dice la verdad.** Los tres miden si **hizo** algo; **ninguno mide si lo que hizo era correcto.** El caso: responde con datos de dominio ✅, ejecuta sin error ✅, genera el documento ✅ — **y los números están mal. El objetivo marca verde perfecto.**
> **No es hipotético:** son los cuatro cálculos de nivel proyecto que producen porcentajes imposibles (hasta 24.814.759.071%) y la severidad que no discrimina, **hoy expuestos a ~300 clientes**.
> **Por eso el objetivo se llama "sin fallas" y no "confiable": el hueco queda visible en el título en vez de tapado por él.**
> **Estado: hueco declarado, sin KR y sin plan de cierre en este trimestre.**

#### KRs

> 📐 **Convención de redacción — nueva el 2026-08-31.** Los KRs se enuncian como **delta**: *llevar X de A a B*. El punto de partida que falte queda **en blanco hasta la revisión del 30 de septiembre**, cuando la primera medición lo completa.

| # | KR | Punto de partida | Meta (dic) | Instrumento | Estado |
|---|---|---|---|---|---|
| — | **Conversaciones sin fricciones por error** — % de conversaciones sin fricción de tipo `bug`, `nlu` o `incompleta` | **50%** ✅ validado | **70%** · críticas = **0** | Log de conversaciones + skill `maia-friction-metrics` | 🟢 Instrumento existente, **baseline cargado** |
| **KR2** | **Éxito de ejecución** — % de acciones aprobadas que se completan sin error del sistema | **85%** ✅ medido | **95%** ⬅️ _reemplaza al 80%_ | Evento de acción aplicada (spec acordada 19-ago) | 🔴 A construir |
| **KR4** | **Performance sostenida durante el escalamiento** — % de consultas con primer token <3s, **todos los meses**, sin degradación contra el baseline de septiembre | **___** ⚠️ pendiente de medición | **≥95% todos los meses** | Amplitude | 🟡 Sin baseline. **Reformulado como guardrail el 31-ago** |

> 📌 **El primer KR va sin número y se cita por nombre.** Es la convención de citación que arrastra este objetivo desde la colisión de IDs — ver la nota al final de la sección. **Y desde el 2026-08-31 la misma convención aplica a O2.**

> ⛔ **KR3 · Éxito del flujo de archivos — RETIRADO el 2026-08-31. El número 3 queda vacante y no se reutiliza.**
> **No desaparece la medición:** baja a **corte por tipo de acción dentro del árbol de *Éxito de ejecución*** (crear/modificar tareas · asignar colaboradores · **generar artefacto**) y al **tablero de KPIs, sin meta**.
> ⚠️ **Condición de validez del corte:** el KR de ejecución mide **acciones aprobadas** —las que pasan por Governance— y **generar un artefacto puede no pasar por aprobación**. Si no comparte denominador, **va al tablero y NO al árbol**. **Decisión pendiente con el squad de AI.**

#### Conversaciones sin fricciones por error — baseline 50%, meta 70%

🔤 **Cambio de NOMBRE, no de KR** _(2026-08-31)_. Se llamaba *conversaciones limpias*. **Criterio, alcance y baseline no se movieron, así que no rompe la serie y NO es la cuarta redefinición.** Motivo: *"limpia"* sugería que la conversación salió bien, y el criterio solo cubre `bug`/`nlu`/`incompleta` — **una conversación podía contar como limpia habiendo fallado al usuario por falta de datos o de capacidad.**

**Criterio, sin cambios desde el 27-ago:** ***MAIA tenía cómo y falló.*** Los tipos `datos`, `capacidad` y `feature` **no cuentan**: son huecos de alcance, van al input de roadmap (`08-roadmap`).

> ✅ **Baseline 50%, validado en las dos dimensiones.** **Criterio:** el 50% **NO incluye** `datos`, `capacidad` ni `feature` — son fallas puramente técnicas. **Unidad:** medido por **conversación reconstruida**, no por fila. **El número empeora respecto de lo que se suponía:** no estaba inflado por fricciones de alcance. **Una de cada dos conversaciones se rompe.**
>
> 📌 **El 70% es una escala, no un destino.** Con la meta cumplida, **3 de cada 10 conversaciones siguen fallando técnicamente.** Sigue siendo la meta correcta para el trimestre —reducción del 40% en cuatro meses— pero **decirlo en el review**, para que nadie lea el 70% como un buen lugar.
>
> 💡 **Pista sobre el dueño del KR.** El export viene multi-turno, partido en filas y **sin ID de conversación**, así que **alguien ya hizo la reconstrucción**: el método no es teórico, se ejecutó una vez. **Esa persona es la candidata natural a dueña del KR.**
>
> 🔴 **El dato que falta y decide el plan del trimestre: la apertura del 50% en `bug` / `nlu` / `incompleta`.** Es el primer nivel del árbol. **Si domina `nlu`, el trabajo es prompt y ruteo; si domina `bug`, es ingeniería. Son dos trimestres distintos y hoy no se sabe cuál.**

**Meta acompañante: fricciones `críticas` = 0**, reportada siempre al lado del porcentaje.

#### KR2 — Éxito de ejecución: baseline 85%, meta corregida a 95%

> ✅ **La meta se corrigió con el primer dato, y este es el precedente más transferible de toda la revisión.** La meta era **80%** y **el baseline volvió en 85%**: **el KR estaba cumplido antes de empezar y, leído literal, pedía empeorar.** Es la misma patología que retiró *tickets por 100 usuarios* el 21-ago, **en la dirección opuesta**.
>
> 📐 **Regla nueva que sale de acá y aplica a todo el set: las metas se recalibran en las DOS direcciones, no solo hacia arriba.**

**Meta 95%, y no es inventada:** el repo ya tenía registrado que **95% es el umbral estándar para operaciones que modifican datos del cliente**. Implica **bajar la tasa de falla de 15% a 5%**.

**Criterio, sin cambios:** *errores del sistema*, **no** "el usuario no quería eso". **Fallo técnico, no desacierto de intención.**

> 📌 **El "→95% en Q1" sale de este OKR.** Un KR de equipo es **trimestral**, y el enunciado viejo cruzaba siete meses. Lo que siga después del 95% **queda como intención declarada del ciclo siguiente, a confirmar en la ceremonia de diciembre** — no como parte de este OKR.
> ⚠️ **Contradicción del documento fuente, registrada:** su sección *"KRs que cruzan el horizonte"* propone dejar el Q4 en **80%**. **Esa redacción es anterior al baseline de 85% y quedó superada por él** — con 85% medido, un KR al 80% pide empeorar. **Se carga 95%.**

🔴 **Sigue siendo la pieza más apalancada del árbol:** el mismo evento de acción aplicada alimenta este KR, **su propio leading declarado** (ratio de aprobación), dos KRs futuros de O3 y una condición de salida de beta de Risk Management. **Sin el evento, este KR no tiene ni lagging ni leading.**

#### KR4 — Performance sostenida durante el escalamiento

🔄 **Reformulado como guardrail el 2026-08-31.** **Enunciado:** *sostener ≥95% de consultas con TTFT bajo 3s en todos los meses del período, sin degradación contra el baseline de septiembre, mientras la base pasa de 128 a ~300 companies.*

**Por qué es un KR y no telemetría permanente:** sostener la latencia mientras se triplica la base **no pasa solo**. Es trabajo acotado al trimestre, con un disparador con fecha —el release del 24-ago—. **Es el resultado de esta carrera, no un umbral que vale para siempre.**

**Tres reglas de lectura propias, distintas del resto del set:**

| Regla | Por qué |
|---|---|
| **Se mide todos los meses, no solo en diciembre** | Un guardrail que se lee al cierre **no detecta degradación: la certifica tarde** |
| **Manda el peor mes. No se promedia** | Si noviembre rompe, el KR falla aunque octubre y diciembre estén bien. **Promediar esconde exactamente lo que el KR vigila** |
| **Se lee junto a la serie de carga** (volumen, concurrencia, companies activas) | *"Sin degradación"* no significa nada si el volumen no cambió. **Sostener performance porque nadie usa MAIA no es un logro** |

> ⚠️ **La referencia de 1,5–2,5s no sirve, y no solo por vieja: no es un percentil.** El KR pide *% de consultas bajo 3s* y la referencia es **latencia típica**. Además es **pre-Orquestador y pre-release**. **Hay que medir de nuevo** — sale de una consulta de Amplitude, cortada por origen y post-release. ⏱️ **No espera a septiembre.**
>
> ⚠️ **Residuo abierto sobre la palanca:** si el TTFT está dominado por el **backend de COR** y no por el ruteo del Orquestador, **la palanca no es del squad de AI** — el mismo motivo por el que se retiró *cobertura de respuesta* el 27-ago. Los nodos de **latencia de ruteo** y **latencia hasta la primera tool call** del árbol lo responden.
> ✅ **Por qué el guardrail resiste mejor esa duda:** *"mejorar el TTFT 10 puntos"* sería un KR que el equipo quizá no controla; ***"no dejar que se degrade al escalar"* sí involucra al squad casi con seguridad** — ruteo, tool calls y concurrencia son suyos. **La duda no desaparece, pero deja de ser bloqueante.**


#### Registro de los KRs retirados de O1 — cuatro

_Se registran en vez de borrarse. **Los IDs de los KRs retirados no se reutilizan: los números vacantes quedan vacantes** — ver la nota de numeración abajo._

| KR retirado | Fecha | Motivo |
|---|---|---|
| **Precisión verificada** _(era O1-KR1)_ | 2026-08-21 | Requería **muestra manual mensual** cotejada contra el backend, **sin forma automática**, y **nunca tuvo dueño asignado**. Era el KR más caro del set y **sin dueño no iba a tener dato** |
| **Conversión de apertura** _(era O1-KR4)_ | 2026-08-21 | ⚠️ **No falla el test de "resultado vs. entregable"** que se usó para bajar otros candidatos a iniciativa. **Se retira para no sostener cinco KRs en un objetivo que nace sin instrumentar.** _Motivo propio, escrito para que no parezca arbitrario_ |
| **Tickets por 100 usuarios activos** _(era O1-KR5)_ | 2026-08-21 | Métrica **descendente** cuya meta **no puede fijarse sin baseline** sin quedar indefinida **en la dirección peligrosa** |
| **Éxito del flujo de archivos** _(era O1-KR3)_ | 2026-08-31 | **No se retira por poco valor: se baja de categoría.** Pasa a **corte por tipo de acción del árbol de *Éxito de ejecución*** y a **KPI del tablero sin meta**. ⚠️ **Condición de validez del corte:** el KR mide *acciones aprobadas* y **generar un artefacto puede no pasar por Governance** — si no comparte denominador, va al tablero y **no** al árbol. **Decisión pendiente con el squad de AI** |

> ⚠️ **Nota de numeración — colisión declarada.** El documento fuente numera los cuatro KRs vivos como **KR1 a KR4** y a la vez enuncia la regla "los IDs no se reutilizan". **Las dos cosas no pueden ser ciertas al mismo tiempo:** el viejo KR1 era precisión verificada y el nuevo KR1 es cobertura de respuesta. **Se carga la numeración del documento fuente (KR1–KR4)** para que el repo coincida con él, y **el mapeo queda escrito acá abajo**. Cualquier acta, dashboard o review anterior al 2026-08-21 que diga "O1-KR3" está hablando de otro KR. 🔄 **Agravado el 2026-08-27:** el KR1 se redefinió otra vez —**tercera definición del mismo número en una semana**— así que **la regla pasa a ser citar este KR por nombre y no por número.** 🔄 **Cerrado el 2026-08-31:** el KR de fricciones **deja de tener número** y se cita solo por nombre; **el 3 queda vacante**; y **la convención de citar por nombre se extiende a O2**, donde los números 3 y 4 también quedan vacantes. 📐 **Regla nueva que completa la convención: distinguir *renombrar* de *redefinir*.** Un cambio de nombre **con el mismo criterio, alcance y baseline no rompe la serie y no cuenta como redefinición** — es el caso de *conversaciones limpias* → *conversaciones sin fricciones por error*.

| Referencia | Significado |
|---|---|
| O1-KR1 · Precisión verificada | **retirado** — sin equivalente |
| O1-KR2 · Cobertura de respuesta | **O1-KR1** |
| O1-KR3 · Éxito de ejecución | **O1-KR2** |
| O1-KR4 · Conversión de apertura | **retirado** — sin equivalente |
| O1-KR5 · Tickets por 100 usuarios | **retirado** — sin equivalente |
| — | **O1-KR3** · Éxito del flujo de archivos *(nuevo)* |
| — | **O1-KR4** · Performance *(nuevo)* |
| O1-KR1 · Cobertura de respuesta (21-ago → 27-ago) | **redefinido** → **O1-KR1 · Conversaciones limpias** (desde 27-ago). El scope cambia de **alcance** a **calidad de ejecución**: **no es el mismo KR con otro nombre** |
| O1-KR1 · Conversaciones limpias (27-ago → 31-ago) | 🔤 **RENOMBRADO** → **Conversaciones sin fricciones por error** (desde 31-ago), **sin número**. **Criterio, alcance y baseline no se movieron: NO es una redefinición y no rompe la serie** |
| O1-KR3 · Éxito del flujo de archivos | **retirado el 31-ago** — el número **3 queda vacante** |
| O2-KR3 · Activación de cohorte | **retirado el 31-ago** — el número **3 queda vacante**. Sobrevive como nodo del árbol de *Alcance* y KPI del tablero |
| O2-KR4 · Recuperación de dormidas | **retirado el 31-ago** — el número **4 queda vacante**. Reemplazado por **O2-KR6** |
| — | **O2-KR5** · Percepción de valor *(nuevo el 31-ago)* |
| — | **O2-KR6** · Sustitución del flujo de carga de horas *(nuevo el 31-ago)* |

#### 🚫 Lo que queda sin cobertura de medición — historia del hueco

> 📌 _La declaración vigente está **en la cabecera de O1**, a la vista y sin tapar. Este bloque conserva cómo se llegó hasta ahí._

**Ningún KR de O1 mide si MAIA dice la verdad.** Los **tres** miden si **hizo** algo; **ninguno mide si lo que hizo era correcto.** El caso concreto: responde con datos de dominio ✅, ejecuta sin error ✅, genera el documento ✅ — **y los números están mal. El objetivo marca verde perfecto.**

**No es hipotético:** cuatro cálculos de nivel proyecto de Risk Management producen **porcentajes imposibles** (hasta 24.814.759.071%) y **la severidad no discrimina** — el desvío promedio ya supera "Alto" en las diez métricas configuradas, así que **"Alto" es el estado por defecto**. Se decidió no cubrirlo con un KR: sigue como **iniciativa** (→ `08-roadmap`).

> **Se registra con el mismo lenguaje que la deuda de cálculos: su prioridad se apoya en convicción y no en medición** — justo cuando el release la expone a ~300 clientes. **Ahora son dos cosas en esa lista, y son la misma cosa.**

> 🔄 **Actualizado el 2026-08-27 con la redefinición del KR1.** El tipo `bug` incluye explícitamente ***dato incorrecto o inventado*** y ***contradicción***, y la severidad `alta` es **dato incorrecto entregado como bueno para decidir**. **El KR1 nuevo recupera parte de lo que se perdió al retirar precisión verificada: la alucinación visible en la conversación** — el usuario repregunta, MAIA se contradice, los números no cierran entre sí.
>
> **Lo que sigue sin cobertura es la alucinación silenciosa:** un número mal entregado con confianza que nadie cuestiona. Para verla hay que **cotejar contra el backend**, que es justo lo que hacía el KR retirado. **El hueco se achica, no se cierra** — y conviene decirlo así, porque **si el review lo lee como cerrado, se cierra en el papel y no en los datos.**

#### Regla de método que aplica a todo el set

⚠️ **Regla 4 de la convención de fuentes: no dividir una fuente por otra.** Varios de los desgloses de estos tres KRs son tentadores de armar cruzando **Amplitude con Metabase**. **Cada corte tiene que vivir dentro de una sola fuente.** Es una de las dos reglas que más se rompen.

⚠️ **Todo corte se reporta con su `n` y su fecha.** Un 41% sobre 12 sesiones no es lo mismo que sobre 900, y **post-release toda serie cruza el cambio de denominador**.

⚠️ **Regla 8: toda serie declara evento, filtro y valores incluidos.** **Ningún KR de este set se puede reportar sin su fila en el mapa de instrumentación de `06-kpi-tree`.**

---

### O2 — Adopción validada y valor demostrado en Enterprise y Midmarket

> *Que MAIA alcance, que sirva, y que habilitarla produzca uso real.*

> 🔄 **Reescrito el 2026-08-31 — primera modificación desde que se cargó el 19-ago** (sobrevivió intacto a las dos reescrituras de O1). **El título no cambia.** Pasa a **cuatro KRs sobre dos universos**: se **retiran dos** (activación de cohorte, recuperación de dormidas) y **entran dos** (percepción de valor, sustitución del flujo de horas). **Los números 3 y 4 quedan vacantes y no se reutilizan.**

**Qué persigue:** demostrar que MAIA funciona para quien tiene motivo de usarla — que **alcanza**, que **se vuelve hábito**, que **no arrastra la percepción del producto** y que **reemplaza un flujo real de trabajo**.

**Por qué el título dice "validada".** El objetivo original hablaba de *adopción activada* y contemplaba metas de cobertura. **Con el release decidido por fuera de Producto, la cobertura dejó de ser una variable que el área controla.** Lo que queda por demostrar es la **validación**.

#### ⚠️ O2 corre sobre DOS universos, y nunca se suman

| KRs | Universo |
|---|---|
| **Alcance · Uso intensivo · Percepción de valor** | **Panel Enterprise + Midmarket** (PM, Director, C-Level), congelado al día previo al release |
| **Sustitución del flujo de horas** | **Asientos elegibles: colaboradores con MAIA habilitada (5.605)** |

> ⛔ **Nunca se suman ni se promedian entre sí.** Queda escrito, no implícito.
>
> 🔄 **Precisado el 2026-09-02: la habilitación está dentro del universo, no es un filtro aparte.** **MAIA se habilita por company**, así que el universo del KR6 es **la misma convención de `asiento elegible` que usa el panel E+MM**, con Colaborador en lugar de PM + Director + C-Level. **Un colaborador sin MAIA habilitada no entra al numerador ni al denominador**: no se puede sustituir un flujo con una herramienta que no se tiene.
>
> ✅ **El universo NO se congela** — cada lectura toma los elegibles del momento. **Motivo: no hay tiempo de instrumentación para sostener una base congelada.** ⚠️ **Costo declarado: cada tanda de release entra al denominador con cero horas vía MAIA y empuja el share hacia abajo sin que nada haya empeorado** — el mismo mecanismo del corte de serie del 24-ago (11,6% → ~2,6%). 📌 **La decisión es reversible: la fecha de habilitación se guarda**, así que la serie sobre cohorte congelada se reconstruye retroactivamente con un filtro, no con instrumentación nueva.
>
> 🔄 **El fundamento por el que el Colaborador estaba afuera venció el 2026-08-31.** El repo decía: *"no se lee como problema de adopción: el rol no tiene propuesta de valor definida; su primer paso es discovery, no un KR"*. **Con la propuesta de carga de horas asistida, el rol ya tiene propuesta de valor** — y pasa de **ficha sin meta** a **universo propio con KR propio** (→ `03-personas`).

#### KRs

| # | KR | Baseline | Meta | Qué valida |
|---|---|---|---|---|
| **KR1** | **Alcance** — penetración del panel E+MM | **11,6%** ⚠️ | **25%** 🚀 | Que MAIA **alcanza** |
| **KR2** | **Uso intensivo** — % de usuarios del panel con **≥15 interacciones en el mes** | **8,19%** ✅ medido (66 de 806) | **25%** 🚀 | Que MAIA **se vuelve hábito** |
| **KR5** | **Percepción de valor** — NPS de la vertical de AI | sin baseline · referencia externa **−27,8** | **≥ el NPS global de COR** | Que la vertical **no arrastra la percepción** |
| **KR6** | **Sustitución del flujo de carga de horas** — % de horas **cargadas** vía MAIA sobre el total de horas **cargadas** por colaboradores con MAIA habilitada, en **ventana de 28 días** | **0%** | **25%** 🚀 | Que MAIA **reemplaza el flujo de la tarea obligatoria** |

> ⛔ **Retirados el 2026-08-31, sin renumerar — los números 3 y 4 quedan vacantes** para no repetir la colisión de IDs que ya arrastra O1.
>
> **KR3 · Activación de cohorte.** Su medición **baja de categoría, no desaparece:** sobrevive como **nodo leading del árbol de *Alcance*** —con sus tres indicadores: comunicación de alta, champion identificado, mediana de días hasta el primer usuario— y como **KPI del tablero, por cohorte y sin meta**. 📌 **La marca de cohorte ya no bloquea ningún KR, pero sigue siendo condición de existencia de ese nodo y de ese KPI. La fecha comprometida —antes del release del 24-ago— está vencida.**
>
> **KR4 · Recuperación de dormidas**, reemplazado por el KR6. ⚠️ **Registrar qué se pierde:** eran **8 cuentas nombrables con 543 asientos, cero desarrollo, ejecutable por el CSM** — **y el único KR del set que miraba cuentas en vez de usuarios.** **Motivo del cambio:** la ventana del Colaborador **es ahora**, con el release recién puesto y la propuesta nueva en la calle. **Las dormidas siguen disponibles para Q1** (→ compromiso de Q1 2027).

> 📌 **Lectura conjunta:** si el **alcance** se cumple pero el **uso intensivo** no, **hay alcance sin valor** — exactamente lo que O3 necesita saber antes de poner precio. **El KR6 es el test más limpio de la misma pregunta:** la carga de horas es la única tarea recurrente y obligatoria del producto, así que **si MAIA es mejor puerta, el colaborador vuelve solo, sin campaña.**

**Anti-metas vigentes: las cinco, sin cambios.**

#### Por qué el denominador es el panel Enterprise + Midmarket

Con el release la base pasó de **128 a ~300 companies** e incorporó el rol **Colaborador**. El universo de asientos elegibles saltaría de ~3.775 a **~15.000**, y **la penetración caería de 11,6% a ~2,6% el mismo día, sin que nada empeore.**

Medir sobre el panel Enterprise + Midmarket (roles PM, Director y C-Level) resuelve tres cosas a la vez:

1. Es el universo que el objetivo nombra en su propio título.
2. **Mantiene la serie comparable:** el 11,6% sigue siendo baseline y los nueve meses de historia siguen sirviendo.
3. Es el universo sobre el que **se va a monetizar**.

Las **~172 companies nuevas fuera de Enterprise y Midmarket se reportan, pero no llevan meta**: son población nueva sin baseline.

> ⏰ **Las dos cosas que debían ocurrir ANTES del release están vencidas** _(estaban comprometidas para el 24-ago)_: **congelar el panel E+MM** e **instrumentar la activación con marca de cohorte**. La segunda ya no bloquea un KR —activación de cohorte se retiró— pero **sí bloquea el nodo del árbol de Alcance y el KPI del tablero**. La primera sigue siendo lo que separa **mejora** de **dilución** en toda la serie posterior.

#### KR1 — Alcance: sin cambios

Usuarios únicos sobre asientos elegibles. Es la métrica de la prioridad "Deploy de AI en clientes" del plan de negocio. **Baseline 11,6%** (jul-26), piso conservador. Sobre el panel cerrado de cuentas de 2025 —denominador constante— el mismo mes da 14,6%. **Meta 25%:** supera el techo observado, que es **Crowe Global con 23,6%**.

> ⚠️ **Salvedad de denominador — leer antes de evaluar el KR** _(cargada el 2026-08-19, sigue vigente)_. **El baseline de 11,6% no se calculó sobre el panel Enterprise + Midmarket**, sino sobre las 128 companies completas, todos los segmentos (373 usuarios ÷ 3.225 asientos al inicio de jul-26). **Los asientos del panel E+MM todavía no existen como dato** — salen del Corte E de `06-kpi-tree`, que sigue sin correr. Si el panel penetra por encima del promedio —lo esperable—, **el baseline real es más alto y la meta de 25% es menos exigente de lo que parece.**

#### KR2 — Uso intensivo: 8,19% → 25%

🔄 **Es una REDEFINICIÓN, no un cambio de nombre** _(2026-08-31)_.

**Antes:** *Retorno* — % de usuarios con **una sola** interacción en el mes *(baja mejor)*, **35,8% → ≤25%**.
**Ahora:** % de usuarios del panel con **≥15 interacciones en el mes**, **8,19% → 25%**.

**Motivo del cambio — el KR anterior tenía tres defectos:** era **descendente**, **mezclaba usuarios nuevos con recurrentes caídos**, y **KR1 cumplido lo empujaba en contra** (todo usuario nuevo entra por el bucket de 1).

**La distribución real, medida** (panel E+MM, agosto-26 · n=806 · `06-kpi-tree`): ≥2 = 66,3% · ≥4 = 36,1% · ≥6 = 24,6% · **≥15 = 8,19% (66 usuarios)** · ≥21 = 4,6%.

> ⚠️ **La apuesta que representa este corte, declarada.** El ≥15 es una **métrica de cola**: mide si MAIA se vuelve hábito, **no si deja de fallar en el primer contacto**. Tiene fundamento —**las únicas cuentas de las que COR factura algo por AI tienen intensidad 10 a 20**— pero hay que asumirlo: **con el corte en 15, el KR se puede cumplir sin tocar el 33,7% que hace una sola interacción.** Ese fondo **deja de estar cubierto por un KR y pasa a vigilarse desde el tablero.**

**La aritmética del 25%, para tenerla a mano en el review:** 25% de 806 son **~202 usuarios**; hoy hay **66**; **faltan 136**. La población adyacente —**11–14: 37 usuarios · 6–10: 95**— **suma 132 y no alcanza aunque cruce completa.**

> 🚀 **Por eso es Moonshot inequívoco: triplicar la cola en cuatro meses.** Y por eso conviene que la cuenta esté escrita: **en diciembre, un 15% se va a leer como fracaso cuando en realidad sería casi duplicar la cola.**
>
> ⚠️ **Dependencia con el KR1, declarada.** El denominador de este KR son **usuarios activos**, que es el **numerador del KR1**. **Si el KR1 cumple y entran cientos de usuarios nuevos, caen todos en los tramos bajos y diluyen el KR2 sin que nada haya empeorado.** Es la misma trampa que tenía el KR anterior: **cambió la dirección de la métrica, no la dependencia.** **Al reportar, poner el numerador absoluto al lado** (hoy 66) para distinguir **dilución** de **estancamiento**.

**Corte obligatorio:** la **distribución completa por bucket se reporta siempre al lado del KR**. Un número único sobre una cola larga esconde de dónde vino el movimiento — es la **anti-meta 3** aplicada.

> 🔴 **Pendiente antes de cerrar este baseline: verificar que el segmento de Amplitude sea el panel.** ⚠️ **806 usuarios E+MM activos en agosto contra 373 en julio son 2,2x en un mes**, y sobre ~3.775 asientos darían **21,4% de penetración** — o sea el KR1 casi cumplido antes de arrancar. **Si el segmento cambia, se mueven los baselines del KR1 y del KR2 a la vez.** Detalle y las dos hipótesis, en `06-kpi-tree`.

#### KR5 — Percepción de valor ➕ nuevo

**Cierra un hueco propio del objetivo: O2 decía "valor demostrado" y todos sus KRs medían frecuencia.** También corrige la mezcla de tipos de métrica — O2 pasa a tener **escala, comportamiento, sustitución y percepción**.

**Instrumento:** experiencia in-app disparada **post-interacción**. Tres preguntas, un solo widget:

| # | Pregunta | Escala | Para qué |
|---|---|---|---|
| 1 | **¿Qué tan probable es que recomiendes MAIA a un colega?** | **0–10** | **Define el KR.** NPS = % promotores (9–10) − % detractores (0–6) |
| 2 | **Del 1 al 10, ¿cuánto valor te entrega MAIA en COR?** | 1–10 | **KPI del tablero**, como promedio. Más directa sobre valor |
| 3 | **¿Por qué?** | Texto libre | **No se metrifica.** Fuente del árbol de drivers y del research de Q1 |

> ⚠️ **La pregunta 1 no es reemplazable por la 2.** Un promedio de valor y un NPS **no son comparables**, y toda la meta se apoya en comparar contra el **NPS global de COR**. Sin la pregunta 1, el KR se queda sin vara.

**Mes de corte: acumulado sep–dic, se corta una vez. No se lee mensualmente.** Con ~806 usuarios del panel y una tasa de respuesta optimista del 20% son **~160 respuestas**, y el IC de un NPS con ese `n` es de **±8 a 12 puntos**: cualquier movimiento mes contra mes es ruido. _(⚠️ Ese cálculo usa los 806 bajo verificación. **Si el segmento vuelve al orden de los 373, son ~75 respuestas y el IC se abre a ±11–12** — el KR sigue siendo anual-de-una-lectura, pero con menos precisión todavía.)_ **El punto de comparación de la tasa de respuesta es el 1,5% de los thumbs**, que es exactamente lo que los descartó como instrumento.

**Tres salvedades a declarar de antemano:**

1. **La comparación contra −27,8 es direccional, no estricta.** El global sale de **Retently, relacional por mail**; esta es **transaccional post-interacción**, y las transaccionales dan sistemáticamente más alto. **La vertical podría "ganar" por método y no por mérito.** Si no hay medición global nueva en el período, la vara queda fija en −27,8 (ago-26).
2. **Sesgo de selección:** una encuesta post-interacción **encuesta a los que volvieron**. El **33,7% de una sola interacción no está en la muestra.** Mide satisfacción de quien ya adoptó, no de quien se fue.
3. **Si vuelve muy negativo, el primer sospechoso es la performance de COR, no MAIA** — el 95% de las menciones negativas de la base son sobre eso. **Sin la pregunta 3 no se distingue, y el KR se vuelve inaccionable.**

**Cortes obligatorios:** por **origen** (banner de riesgo vs. chat) y por **rol**.

#### KR6 — Sustitución del flujo de carga de horas ➕ nuevo

**Denominador declarado:** horas cargadas por **colaboradores**, en **companies con MAIA habilitada**. **No** el total de horas de COR ni las de otros roles. **0% → 25%.**

**El árbol de este KR no es una heurística, es una identidad:**

> **Share de horas = penetración × share individual promedio**

> ⚠️ **Los dos factores tienen que correr sobre la misma población** _(2026-09-02)_. **El `N` es el mismo arriba y abajo o el álgebra no cancela:** si la penetración se calcula sobre **asientos elegibles** y el share individual sobre **colaboradores que cargan horas**, **el segundo factor deja de tener techo en 100%** y la descomposición no se puede leer. **Va escrito en la definición de cada corte, no asumido** (→ `06-kpi-tree`).

| Si la penetración llega a… | …el share individual tiene que ser |
|---:|---:|
| 25% | **100%** de sus horas |
| 40% | 63% |
| 50% | 50% |
| 100% | 25% |

> 🚨 **Consecuencia a registrar: no hay combinación que llegue a 25% sin que la penetración pase de 0,27% a por lo menos 25% — un salto de ~90x.** **El cuello de botella no es de producto, es de amplitud:** exposición, comunicación, activación. **Si eso no se mueve, ninguna mejora de producto alcanza.**
>
> ⚠️ **`[HIPÓTESIS]` desde el 2026-09-02 — el ~90x no está verificado.** La tabla de arriba **se apoya en que el segundo factor tiene techo en 100%**, y eso **solo es cierto si los dos factores corren sobre la misma población**. Hoy no corren: la penetración se declara sobre **5.605 asientos elegibles** y el share individual sobre **horas cargadas**, así que **el divisor queda deflactado por los colaboradores que cargan cero, el techo desaparece y el multiplicador podría ser bastante menor.**
> **Qué lo refutaría:** que **una parte grande de los elegibles no cargue horas en una ventana de 28 días**. Ahí el 25% de share se alcanza con mucha menos penetración que 25%, **y el cuello de botella deja de ser tan claramente de amplitud.**
> 📌 **Lo resuelve una consulta, no un desarrollo:** cuántos elegibles cargan horas en una ventana de 28 días — pedido cargado, **antes del cierre del 27-sep**. **Hasta entonces, el ~90x no se usa para repartir capacidad sin decir que es hipótesis.**

**Regla de lectura: por trayectoria, no por resultado.** **0% no es un baseline, es una línea de largada:** no hay riesgo de que la medición vuelva por encima de la meta —lo que le pasó al éxito de ejecución— **pero tampoco hay información sobre qué es alcanzable. Sin ancla, el 25% es una convicción, no un cálculo.** Lo que informa es **la pendiente**. 🔄 _Los checkpoints mensuales que estaban acá (sep ~6% · oct ~12% · nov ~19% · dic 25%) **quedaron reemplazados el 2026-09-02 por los cierres de ventana**, abajo — el KR ya no corta por mes calendario._

> ⚠️ **En septiembre el share va a estar cerca de 1% y no va a decir nada.** Lo que se mira ese mes es el **embudo de amplitud** — expuestos → activados → abandono. **Es el único KR del set donde el árbol no complementa al número: lo reemplaza en la primera ventana.**
>
> ⚠️ **La meta de 25% está puesta por criterio, no contra una medición.** El 0,27% es **pre-release y pre-propuesta**: describe un rol que todavía no tenía caso de uso, así que **no sirve como punto de partida**. **El cierre del 06-sep da el baseline real** y **la meta se recalibra en el cierre del 27-sep, en las dos direcciones** — mismo procedimiento que corrigió el éxito de ejecución de O1.
>
> 🔄 **Checkpoints de trayectoria** _(2026-09-02, interpolación lineal — vara de alerta temprana, **no metas intermedias**)_:
>
> | cierre 06-sep | cierre 04-oct | cierre 01-nov | cierre 29-nov | cierre 27-dic |
> |---:|---:|---:|---:|---:|
> | ~0% | ~6% | ~13% | ~19% | **25%** |
>
> ⚠️ **Solo esos cinco cierres son comparables entre sí.** Están separados por 4 semanas, así que no comparten datos. **Las lecturas semanales intermedias comparten tres cuartos de su dato con la anterior:** sirven para ver la pendiente, **no para declarar cambios**, y **una racha de subas semanales no es evidencia de tendencia** — aparece por construcción en cualquier serie de ventana móvil.
>
> ⚠️ **La concentración es el riesgo propio de esta métrica.** **Si diez colaboradores cargan el 100% de sus horas por MAIA y el resto nada, el ratio se ve bien y la adopción es nula.** Por eso el **corte de distribución de share por colaborador es obligatorio** — anti-meta 3 aplicada a otra métrica.

**A favor, un argumento que ningún otro KR tiene:** cargar horas es **obligatorio**. **No hay que crear demanda, hay que redirigir una que ya existe.** **En contra, con precedente propio:** habilitar no produce uso — las **79 companies habilitadas para Risk Management en julio aportaron cero usuarios netos**, y el rol Colaborador lleva diez meses en 0,27%.

**El 0,27% de penetración del Colaborador baja a KPI del tablero.** Mide **cuánta gente toca MAIA**, no **cuánto flujo pasa por MAIA**: es **complemento del KR6, no sustituto**.


---

### O3 — Modelo de negocio de AI con revenue propio — ⏸️ EN REVISIÓN

**No se carga con KRs.** Depende de definiciones de **pricing y lógica de venta que no decide Producto**. Se retoma cuando esa definición exista. El estado actual del modelo de negocio y la tensión de pricing están más abajo, en su sección propia.

_Dos de sus KRs futuros dependen del mismo evento de acción aplicada que sostiene el **KR2 de O1** (éxito de ejecución; era el KR3 hasta el 2026-08-21) — otra razón para arrancar por ahí._

---

### Declaración Roofshot / Moonshot

_Cargada el 2026-08-31._ **Regla: un Moonshot al 70% es un éxito; un Roofshot al 70% es un problema.** **Sin declarar el tipo por adelantado, cualquier resultado se interpreta como convenga.**

| KR | Tipo | Fundamento |
|---|---|---|
| O1 · Conversaciones sin fricciones por error | 🚀 **Moonshot** | **50% → 70%** baja la fricción de 50% a 30%: **reducción del 40% en cuatro meses.** Baseline validado en criterio y unidad, así que la declaración queda firme |
| O1 · Éxito de ejecución | 🚀 **Moonshot** | **85% → 95%** implica **cortar los errores a un tercio**. La vara es **externa** —umbral estándar para operaciones que modifican datos del cliente—, no arbitraria |
| O1 · Performance sostenida | 🏢 **Roofshot** | Un guardrail al 70% **es un problema por definición**. ⚠️ **Muta a 🚀 Moonshot si el baseline de septiembre vuelve por debajo del 95%**: ahí deja de ser *sostener* y pasa a ser **mejorar mientras se escala** |
| O2 · Alcance | 🚀 **Moonshot** | **25% de promedio del panel supera el techo histórico de cualquier cuenta individual** (Crowe, 23,6%) |
| O2 · Uso intensivo | 🚀 **Moonshot** | **Triplicar la cola:** de 66 a ~202 usuarios, +136. **La población adyacente entera —132 usuarios entre 6 y 14— no alcanza aunque cruce completa.** Al 70% (≈18%) sigue siendo un buen resultado |
| O2 · Percepción de valor | **A declarar en la revisión del 30-sep** | Sin baseline propio y con la vara sujeta al confounder de método. **Declarar el tipo antes de la primera lectura es adivinar** |
| O2 · Sustitución del flujo de horas | 🚀 **Moonshot** | **El más extremo del set: de 0% a 25% en cuatro meses.** A favor, que cargar horas es obligatorio. En contra, que habilitar no produce uso |

> 📌 **Nota para el review:** el **25% aparece como meta en Alcance, Uso intensivo y Sustitución del flujo de horas**, sobre **tres denominadores distintos**. Cada uno tiene fundamento propio, pero **juntos en una slide pueden leerse como un número elegido por redondo.** Tener a mano por qué cada uno llegó a ese valor.
>
> **Lo que esto cambia en el cierre:** **cinco de los siete son Moonshot. Al 70% son buenos resultados** — y antes de esta declaración no había nada escrito que permitiera leerlos así.

### Mes de corte por KR

_Cargado el 2026-08-31._ **Sin esto, "25%" es ambiguo: ¿diciembre, el promedio del período, el mejor mes?**

| KR | Cómo se mide el resultado del trimestre |
|---|---|
| O1 · Conversaciones sin fricciones por error | **Corrida de diciembre.** Sep–nov son revisión mensual; **septiembre es el baseline** |
| O1 · Éxito de ejecución | **Acumulado del período**, desde que el evento exista (el volumen mensual es bajo al inicio) |
| O1 · Performance | **Todos los meses. Manda el peor** — es un guardrail: **no se promedia ni se corta una vez** |
| O2 · Alcance | **Penetración de diciembre-26.** Métrica mensual, no acumulada |
| O2 · Uso intensivo | **Diciembre-26** · métrica mensual, no acumulada |
| O2 · Percepción de valor | **Acumulado sep–dic, se corta una vez en diciembre.** No se lee mensualmente: el `n` no lo permite |
| O2 · Sustitución del flujo de horas | 🔄 **No usa mes calendario** _(2026-09-02)_. **Ventana de 28 días que cierra el domingo 27-dic-26** (30-nov → 27-dic) · share de la ventana, **no acumulado**. Lectura **semanal**; los cierres comparables son **06-sep / 04-oct / 01-nov / 29-nov / 27-dic** |

> ⚠️ **El KR6 es el único del set que no corta por mes calendario.** La ventana de 28 días son **cuatro semanas exactas**, lo que **mantiene constante la composición de días de la semana en toda lectura** — importante porque el denominador son **horas cargadas**, que se cargan en días hábiles. **Cuatro semanas no encajan con el fin de mes: el resultado cierra el 27-dic y los últimos cuatro días de diciembre quedan afuera.** Son días de fiestas con carga mínima, **pero conviene decirlo antes de que alguien lo cuente.**
>
> ✅ **Verificado al cargar:** los cinco cierres —**06-sep, 04-oct, 01-nov, 29-nov y 27-dic de 2026**— **son todos domingos y están separados por exactamente 28 días**, así que la convención cierra. **La ventana final va del 30-nov al 27-dic.**
>
> ⚠️ **Y una salvedad sobre el primer cierre, que el criterio no menciona:** la ventana del **06-sep arranca el 10-ago**, así que **21 de sus 28 días son de agosto** — antes de que la propuesta estuviera en la calle y con el evento todavía inexistente. **Como baseline sirve igual —va a dar ~0% y eso es el punto— pero no es "el arranque de septiembre": es una ventana que mira casi toda hacia atrás.**

### Un leading indicator declarado por KR

_Cargado el 2026-08-31._ **Regla: uno por KR, no el árbol entero. Siete números se miran; veintiocho no.** **Estos siete son la agenda de las revisiones de octubre y noviembre** — sin ellos, la cadencia mensual existe pero no tiene de qué hablar.

| KR | Leading declarado | Costo |
|---|---|---|
| O1 · Conversaciones sin fricciones por error | **Tasa de reformulación del usuario** | 🟢 Sale del mismo log de la corrida |
| O1 · Éxito de ejecución | **Ratio de aprobación del usuario** | 🔴 Depende del evento de acción aplicada |
| O1 · Performance | **Latencia de ruteo del Orquestador** | 🟢 Una consulta de Amplitude |
| O2 · Alcance | **Conversión apertura → primera consulta** (Corte A) | 🟢 Una consulta de Amplitude |
| O2 · Uso intensivo | **Tasa de 2ª interacción ≤30 días** | 🔴 Instrumentación a construir |
| O2 · Sustitución del flujo de horas | **Tasa de 2ª carga vía MAIA dentro de 2 semanas** | 🟡 Sale del mismo instrumento que el KR |
| O2 · Percepción de valor | **Promedio mensual de la pregunta de valor (1–10)** ⚠️ lectura temprana, **no leading estricto** | 🟡 Sale del propio widget |

> **Cuatro son gratis o una consulta; tres dependen de instrumentación a construir.**
>
> 💡 **El de percepción es el que más cambia el set:** hoy no daría **ninguna** señal hasta diciembre, y con su indicador declarado pasa a ser observable mes a mes.
>
> ⚠️ **La tasa de respuesta de la encuesta NO es un leading: es una variable de control.** **Predice si el KR será legible, no si será bueno.** Y el leading real de percepción está **aguas arriba**: las fricciones por error de O1.
>
> 📌 **Convención nueva del árbol: distinguir *leading* de *variable de control*.** Un control **no se mueve con el trabajo del equipo pero condiciona la lectura** — asientos elegibles, tasa de respuesta de la encuesta, serie de carga del guardrail. **Y un leading que alimenta dos KRs es señal de palanca real:** la *2ª interacción ≤30 días* aparece en Uso intensivo y en Sustitución del flujo de horas.

### Tablero de KPIs permanentes

_Cargado el 2026-08-31._ Series que **no dejan de importar cuando termina el trimestre**, y que **por eso no son KRs**. **Se reportan sin meta.**

| KPI | Por qué acá y no como KR |
|---|---|
| **Usuarios de una sola interacción** — % del panel en el bucket de 1 | **33,7% hoy.** Era el KR2 hasta esta revisión. **Sale del KR pero no del radar:** es el fondo de la distribución y ningún KR de O2 lo cubre |
| **Flujo de archivos** — % de sesiones con archivo que entregan el artefacto | **Bajó de KR de O1.** Si comparte denominador con *Éxito de ejecución*, además es **corte del árbol** |
| **Activación de cohorte** — % con primer usuario ≤30 días, por cohorte | **Bajó de KR de O2.** Sigue siendo **el lagging más rápido disponible**: resuelve en 30 días |
| **Penetración del Colaborador** — % de colaboradores que usan MAIA | **0,27%**, pre-release y pre-propuesta. **Bajó de KR.** Mide cuánta gente toca MAIA, no cuánto flujo pasa por MAIA — **complemento del KR6, no sustituto** |
| **Puntualidad de carga** — % de colaboradores que cargan dentro de la semana en curso | **Es el valor real** —la tesis de COR es que el margen se pierde porque la operación no se ve mientras el trabajo está en curso— **pero la atribución es difícil**: distinguir "cargó por MAIA" de "cargó *porque* MAIA" pide antes/después o grupo de control |
| **Spillover del Colaborador** — % que usa MAIA para algo además de cargar horas | **Es lo que justificaría la apuesta más allá del time tracking:** dice si la carga de horas es **la puerta o el destino** |
| **Percepción de valor** — promedio de la pregunta *"¿cuánto valor te entrega MAIA?"* (1–10) | Sale del mismo widget que el KR5. **Es la lectura directa de valor; el NPS es la comparable** |
| **Tickets por 100 usuarios activos** | Retirado como KR el 21-ago **por ser descendente sin baseline**. **Como KPI no necesita meta** — y es la alerta post-release más barata |
| **Penetración de las ~172 companies nuevas** | Población nueva sin baseline |
| **Forma de la distribución de frecuencia** | El total y el promedio **ya se declararon malas métricas de salud** (anti-metas 2 y 3) |
| **% del alcance que entra por banner** (54–72%) | Serie de dependencia de riel. **Donde la tensión O1/O2 se ve primero** |

### Cuatro cosas que registrar sobre este set

_Cargadas el 2026-08-19 al integrar los OKRs al repo. No invalidan el set: son las costuras que hay que mirar en el primer review._

1. **KR1 de O2 es un número único y la anti-meta 1 pide metas diferenciadas por rol.** El set re-enuncia esa anti-meta en sus propios criterios, y aun así fija 25% para el panel entero. **O el KR se desagrega por rol al reportar, o la anti-meta se revisa explícitamente.** El dato que la motiva sigue vivo: el C-Level lleva cinco meses entre 9,5% y 13,3% mientras el PM pasó de 1,8% a 11,9%.
2. **El KR de penetración se fijó con el corte por origen todavía abierto.** Era el único bloqueo declarado en este archivo. **No es un error:** la regla de decisión de `06-kpi-tree` está escrita de antemano y dice que el KR se puede escribir en los dos desenlaces. Lo que el Corte A decide ahora **no es si el KR existe, sino si se reporta en una línea o en dos** (MAIA por chat / MAIA por banner). Sigue siendo la consulta más desbloqueante del repo.
3. **La meta del KR1 se apoya en un baseline de otro universo** — ver la salvedad de denominador arriba. Correr el Corte E la convierte en una meta medida.
4. **Todo KR persigue un resultado, no un entregable.** Se bajaron a iniciativas varios candidatos que eran milestones: instrumentar un evento, corregir cálculos, poner workflows en producción, definir un modelo de negocio. **El trabajo sigue siendo necesario, pero no se mide como resultado** (→ `08-roadmap`).

### Seis costuras que agregaron las reescrituras de O1 y O2

_Las tres primeras se cargaron el 2026-08-21; la cuarta, el 2026-08-27; la quinta y la sexta, el 2026-08-31. Las cuatro de arriba siguen vigentes y son todas de O2._

5. **La numeración de los KRs de O1 colisiona con su propia regla.** El documento fuente dice "los IDs no se reutilizan" **y** numera los cuatro KRs vivos como KR1–KR4. Se cargó la numeración del fuente con el **mapeo viejo→nuevo escrito** (ver O1). **Toda referencia a "O1-KRn" anterior al 21-ago apunta a otro KR:** actas, dashboards y el propio historial de este repo.
6. **Se retiró el único KR que fallaba por falta de dueño, no por falta de valor.** La precisión verificada era el KR más caro del set y **el retiro cierra un pendiente sin resolverlo**: el hueco de medición de verdad **queda abierto y ahora sin candidato**. Está registrado en O1 como tal, con el mismo lenguaje que la deuda de cálculos.
7. **Dos KRs nuevos nacen con meta y sin evidencia.** El de archivos es `[HIPÓTESIS]` —**no hay ni un dato del flujo en el repo**— y el de performance apoya su referencia en un promedio que puede ser de **otra arquitectura** (Orquestador, 22-jul-26). **Las metas son de criterio; el primer baseline las recalibra.**
8. **Tercera versión de "O1-KR1" en menos de una semana** _(2026-08-27)_. El KR1 original era **precisión verificada** (retirado el 21-ago), el del 21-ago era **cobertura de respuesta** y el del 27-ago es **conversaciones limpias**. El repo ya tenía una colisión de IDs declarada; **esta la agrava.** Regla operativa: **este KR se cita por nombre, no por número.** Ver la tabla de mapeo. 🔤 _El renombre del 31-ago a **conversaciones sin fricciones por error** **no** es una cuarta versión: mismo criterio, mismo alcance, mismo baseline._
9. **Cuarta vez que este repo pisa un problema de denominador** _(2026-08-31)_. **806 usuarios E+MM activos en agosto contra 373 en julio: 2,2x en un mes**, y sobre ~3.775 asientos darían **21,4% de penetración** — el KR de Alcance casi cumplido antes de arrancar. Dos hipótesis, ninguna distinguible con lo disponible: **el segmento filtra por tamaño de company pero no por rol** (metiendo Colaboradores post-release), o **incluye companies nuevas** que el panel congelado debería excluir. **Si el segmento cambia, se mueven los baselines de Alcance y de Uso intensivo a la vez.** Los tres anteriores: el 11,6% sobre el universo completo · el 7,3% de Risk Management con el denominador de MAIA · los 413 vs. 373 del histograma. **Es un patrón del repo, no un accidente** — y la foto del panel congelado, que lo habría cerrado, está vencida.
10. **El 25% aparece tres veces sobre tres denominadores distintos** _(2026-08-31)_ — Alcance, Uso intensivo y Sustitución del flujo de horas. **Cada uno tiene fundamento propio**, pero juntos en una slide **pueden leerse como un número elegido por redondo**. Los fundamentos están escritos en la declaración Roofshot/Moonshot: **tenerlos a mano en el review.**

## Marco de priorización

Producto prioriza combinando dos ejes:

1. **Alineación a las 3 prioridades del plan** (apertura de nuevos verticales, thought leadership por vertical, deploy de AI en clientes) — una iniciativa pesa más si sirve directamente a alguna de las tres.
2. **Valor vs. esfuerzo** — dentro de lo alineado, se prioriza por relación de impacto esperado sobre costo de implementación.

No es un framework formalizado tipo RICE con scoring numérico, sino un criterio cualitativo de dos ejes.

## Pendientes — input interno

- [x] ✅ **OKRs de la vertical de AI — cargados el 2026-08-19, revisados el 2026-08-31.** O1 (**ejecución sin fallas, 3 KRs**) y O2 (adopción validada, **4 KRs sobre dos universos**); **O3 queda ⏸️ en revisión** por depender de pricing, que no decide Producto. Ver "OKRs del trimestre". _Los cinco bloques de evidencia que sostienen O2 —baseline, anti-metas, distribución, dormidas y Crowe— estaban cargados desde el 17 al 19 de agosto. **Los cuatro KRs de O1, en cambio, no tienen baseline cargado.**_ 🔄 **KR1 redefinido el 2026-08-27: "conversaciones limpias", sin meta y con instrumento existente.** Sigue sin baseline cargado, pero **es el único de O1 que se puede medir sin construir nada.**
- [ ] **OKRs de los otros ejes/squads** (Coherencia de dinero y negocio, Coherencia de datos, Fundamentals COR, GGN-GUT) — siguen sin definir. **No inventarlos.**
- [ ] ⏰🔴 **VENCIDO — era antes del release del 24-ago: congelar el panel Enterprise + Midmarket e instrumentar la activación con marca de cohorte.** Las dos son consultas, no desarrollo. **La primera sigue siendo lo que separa *mejora* de *dilución* en toda la serie posterior** — y su ausencia es parte de por qué hoy no se puede decidir si los 806 usuarios de agosto son el panel. **La segunda ya no bloquea un KR** —activación de cohorte se retiró el 31-ago— **pero sí bloquea el nodo leading del árbol de Alcance y el KPI del tablero.** → `06-kpi-tree`.
- [ ] 🔴 **Correr el Corte A (solapamiento MAIA / banner)** — ya no bloquea escribir el KR de penetración, pero **decide si se reporta en una línea o en dos**. Sigue siendo la consulta más desbloqueante del repo. → `06-kpi-tree`.
- [ ] **Resolver la tensión entre KR1 de O2 y la anti-meta 1:** el KR es un número único (25%) y la anti-meta pide metas diferenciadas por rol. **Desagregar al reportar, o revisar la anti-meta explícitamente.** No dejarlo implícito.
- [x] ~~**Asignar dueño con nombre al KR1 de O1 (precisión verificada).**~~ ⚠️ **Cerrado el 2026-08-21 por retiro del KR, no por resolución.** Se retiró justamente porque nunca tuvo dueño y no había forma automática de medirlo. **El hueco que dejó —nadie mide si MAIA dice la verdad— está registrado en la sección de O1 y sigue abierto.**
- [x] ~~**Fijar las metas de los cuatro KRs de O1 que decían "por definir".**~~ ✅ **Cerrado el 2026-08-21: los cuatro KRs tienen meta** (75% · 80%→95% · 80% · ≥95%). 🔄 **Parcialmente reabierto el 2026-08-27:** el 75% se cayó con la redefinición del KR1, que **queda sin meta hasta la primera corrida**. **Hoy son tres metas puestas y una por medir.** ⚠️ **Con la salvedad que reemplaza al pendiente: las cuatro son provisorias, fijadas por criterio y no contra una medición.** Ninguno tiene baseline cargado.
- [ ] 🔁 **Recalibrar las metas contra su primer baseline, EN LAS DOS DIRECCIONES**, en la revisión del **30 de septiembre**, dejando registrado el número viejo al lado del nuevo. ⚠️ **La regla de las dos direcciones se aprendió caro el 31-ago:** la meta de *éxito de ejecución* era 80% y el baseline volvió en **85%** — **el KR estaba cumplido antes de empezar y, leído literal, pedía empeorar.** _(Reformulado el 2026-08-31: quedan por recalibrar **performance** —sin baseline— y **sustitución del flujo de horas** —cuyo 0% es pre-propuesta y no sirve de ancla—. Fricciones, ejecución y uso intensivo ya se fijaron contra dato medido.)_
- [x] ~~⚠️ **Definir el scope del KR1 de O1 (cobertura de respuesta): por entidades o por especialistas.**~~ 🔄 **Se disuelve el 2026-08-27: cambió el denominador del KR.** La clasificación **dentro/fuera de dominio sigue siendo necesaria para el input de roadmap**, pero **ya no bloquea un KR**. **Cerrado por redefinición, no por resolución** — mismo criterio con el que se cerró el pendiente de dueño de precisión verificada.
- [ ] 🔴 **Asignar dueño con nombre y cadencia al KR de conversaciones sin fricciones por error.** 💡 **Hay candidato:** el export viene sin ID de conversación, así que **alguien ya hizo la reconstrucción del baseline del 50%** — esa persona es la natural. **Es el pendiente que reemplaza al del scope.** ⚠️ **El KR1 tiene la misma estructura de costo que precisión verificada —lectura humana de una muestra— y esa fue la causa del retiro.** Las diferencias a favor son reales (**método fijo, tooling, dueño estructural con palanca sobre código y prompt**), pero **sin nombre y sin cadencia muere igual.**
- [x] ~~🟢 **Correr la primera medición del KR1 y fijar la meta contra ese número.**~~ ✅ **Cerrado el 2026-08-31: baseline 50%, meta 70%**, validado en criterio (excluye `datos`/`capacidad`/`feature`) y en unidad (conversación reconstruida). ⚠️ **El número empeora respecto de lo que se suponía: no estaba inflado por fricciones de alcance. Una de cada dos conversaciones se rompe.**
- [ ] 🔴 **Pedir la apertura del 50% en `bug` / `nlu` / `incompleta`.** **Es el dato que decide el plan del trimestre:** si domina `nlu` el trabajo es prompt y ruteo; si domina `bug`, es ingeniería. **Son dos trimestres distintos y hoy no se sabe cuál.**
- [ ] ⚠️ **Ajustar la regla multi-tipo del método antes de la primera corrida:** de "la fricción más grave" a **"al menos una fricción técnica"**. Con la regla vieja, una conversación con `nlu` + `capacidad` se tipea `capacidad` y **la falla técnica desaparece del KR**. **Después de la primera corrida no se puede cambiar sin romper la serie.**
- [ ] **Escribir la frontera entre el KR1 y el KR2 de O1.** La severidad `crítica` incluye **"datos mal escritos en COR"**, que también es KR2. **No está mal que un incidente aparezca en los dos** —KR2 es automático y por evento, KR1 es muestral y por lectura— **pero si no queda escrito, en el review van a decir que se cuenta dos veces.**
- [x] ~~⛔ **Especificar e instrumentar los eventos del flujo de archivos (KR3 de O1).**~~ 🔄 **El KR se retiró el 2026-08-31 y el número 3 queda vacante.** La medición **baja de categoría, no desaparece**: corte del árbol de *Éxito de ejecución* y KPI del tablero.
- [ ] 🟡 **Decidir con el squad de AI si generar un artefacto pasa por aprobación de Governance.** **Decide si el flujo de archivos es corte del árbol de ejecución o solo KPI del tablero:** el KR mide *acciones aprobadas*, y **si no comparte denominador, no puede colgar del árbol.**
- [ ] 🟡 **Medir el baseline de performance post-release — percentil, no promedio, cortado por origen.** ⚠️ **La referencia de 1,5–2,5s no sirve, y no solo por vieja: no es un percentil.** El KR pide *% de consultas bajo 3s* y la referencia es latencia típica; además es **pre-Orquestador y pre-release**. **Sale de una consulta de Amplitude y no espera a septiembre.** **Decide si el guardrail es Roofshot o Moonshot.** Y si hay mediciones a ambos lados del 22-jul-26, **la resta es el costo en latencia del Orquestador** — insumo del eje capacidad vs. superficie de `08-roadmap`.
- [ ] 🔴 **Verificar que el segmento de Amplitude del histograma de agosto sea el panel E+MM.** **806 usuarios activos en agosto contra 373 en julio son 2,2x en un mes** y darían **21,4% de penetración: el KR de Alcance casi cumplido antes de arrancar.** **Si el segmento cambia, se mueven los baselines de Alcance y de Uso intensivo a la vez.** Detalle en `06-kpi-tree`.
- [ ] 🔴 **V1 del evento de acción aplicada.** Sin esto, *éxito de ejecución* **no tiene ni lagging ni leading** — su leading declarado sale del mismo evento. **Es lo único bloqueante del set.**
- [ ] ⏰🔴 **Instrumentar el evento de carga vía MAIA, el share en ventana de 28 días y el embudo de amplitud (expuestos → activados → abandono). FECHA VENCIDA** _(era "antes de septiembre"; al 2026-09-02 no existe)_. El KR6 arranca en 0% y **se lee por trayectoria: la medición tiene que existir ya.** 🔄 **La ventana móvil agrava el costo del retraso:** cada día sin evento **no arruina un punto de la serie, arruina las 28 lecturas que lo contienen**. **El cierre del 06-sep es el baseline y no se reconstruye después.**
- [ ] 🔴 **Correr el tamaño del denominador del KR6: horas cargadas totales, asientos elegibles y cuántos de ellos cargan horas en una ventana de 28 días.** **No necesita instrumentación nueva** — sale del backend de horas. **Es la población sobre la que corre la identidad del árbol** (amplitud × profundidad): sin ese número, la descomposición no se puede calcular y **no se sabe cuál de los dos factores se movió**. ⚠️ **Y es el dato que resuelve si el ~90x se sostiene.** **Antes del cierre del 27-sep**, para llegar a la recalibración con el dato y no con la discusión.
- [ ] 🟡 **Resolver en la spec del evento si la tasa de finalización de la carga asistida vive en una sola fuente.** Si el evento cubre las dos puntas (intento iniciado / carga completada), la tasa es válida; **si no, cruza el log de Metabase con el backend de horas y viola la regla 4**, y se reemplaza por el abandono medido en Amplitude. **Es decisión de spec, no de reporte.**
- [ ] 🟡 **Construir el widget de NPS in-app de tres preguntas** — instrumento del KR5. **La tasa de respuesta se reporta como variable de control, no como leading.**
- [ ] 🟡 **Declarar el tipo Roofshot/Moonshot que queda pendiente** (*percepción de valor*) en la revisión del 30-sep, y **confirmar la mutación del guardrail de performance** contra su baseline.
- [x] Cómo laddera Producto a "Deploy de AI en clientes": ¿qué métrica de producto la mide? _(Resuelto 2026-08-17: **penetración sobre asientos elegibles**, con metas diferenciadas por rol. Ver sección dedicada. Sigue abierto el laddering de las otras dos prioridades.)_
- [ ] **Definir outcome y meta para lo que del portafolio de AI sigue sin métrica** — entregan valor en trabajo ejecutado, no en consultas, así que la vara de MAIA no les sirve. Queda adentro de esta lista: **workflows/automatizaciones** (sin ninguna métrica), la **creación** de agentes en Marketplace, y el **valor entregado** de Risk Management. _(Marketplace salió por consumo el 2026-08-18; **Risk Management salió por alcance el 2026-08-18**, aunque su penetración quedó en pausa el 2026-08-19 por denominador.)_
  - ⚠️ **Depende de una definición previa, ya resuelta para dos de tres:** Marketplace es feature hermana, **Risk Management es pilar de MAIA con activación separada** (FA propio, pero **exige el FA de Chat de MAIA** — resuelto el 2026-08-18 en `01-producto`). ⚠️ _El fundamento original decía "mismo denominador": **eso es falso** (2026-08-19). Risk Management tiene **base propia de 119 companies**, subconjunto de las 128 de MAIA. La resolución se sostiene por la dependencia del FA, no por el denominador._ **Falta solo workflows.**
- [ ] **Instrumentar el evento de acción aplicada desde una respuesta de riesgo** — junto con la aprobación de Governance, es el camino a medir valor entregado en lugar de uso. Pedido cargado en `06-kpi-tree`.
  - 📐 _**Especificación acordada el 2026-08-19** (esto es la spec, no el outcome — el outcome sigue pendiente arriba): el evento registra **los IDs de las entidades afectadas** o un `batch_id` que las agrupe, **no solo el conteo**. Un evento de "acción revertida" **se propuso y se retiró**, y no por prioridad: las acciones de Risk Management son **ediciones ordinarias** de proyectos y tareas, así que si el producto no tiene un "deshacer", el evento **no tiene nada que lo dispare**. Con los IDs, el retroceso se lee después contra el backend. La **ventana de re-edición no se fija de antemano** (7 / 14 / 30 días): sale de mirar la distribución real. Detalle en `06-kpi-tree`._
  - ⚠️ _Tres preguntas al **squad de AI** condicionan el arranque: si existe un "deshacer" sobre esas ediciones, **si hay registro de backend que permita reconstruir histórico** —si lo hay, el baseline puede arrancar antes del primer mes de instrumentación— y la estimación de la V1. Cargadas en `06-kpi-tree`._
- [ ] **Definir el modelo de negocio de MAIA** más allá del servicio de consultoría, resolviendo la tensión de cotizar por licencia un valor que se concentra en 1 a 3 personas.
- [x] Marco de priorización de Producto. _(Alineación a las 3 prioridades del plan + valor vs. esfuerzo; no es un framework formal tipo RICE.)_
- [x] Propagar la expansión de verticales/EMEA a `03-personas` y `04-mercado`. _(Hecho.)_
