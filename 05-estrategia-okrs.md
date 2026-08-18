# 05 — Estrategia y OKRs (COR)

> **Última actualización:** 2026-08-18
> **Owner:** Product Manager, área de Producto
> **Contexto para IA:** Visión, pilares estratégicos, KPIs y OKRs, para priorizar y alinear iniciativas. Base principal: **Business Plan 2026–2027** (presentado internamente). Es un plan de negocio/GTM: fuerte en revenue y go-to-market, liviano en estrategia de producto. Los **OKRs de producto (objetivos + key results)** aún no están cargados — no inventarlos.

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

### La métrica que mide la prioridad

**Penetración = usuarios únicos ÷ asientos elegibles** (PM + Director + C-Level de las cuentas con MAIA habilitada). Reemplaza el conteo de usuarios activos absolutos, que se movía con el denominador.

| Referencia | Valor |
|---|---|
| Baseline jul-26, base completa | **11,6%** _(provisorio — ver salvedad de instrumentación en `06`)_ |
| Baseline jul-26, panel cerrado de cuentas 2025 | **14,6%** |
| **Techo observado hoy** (mejores cuentas) | **>23%** |
| Piso observado (8 cuentas Enterprise "dormidas") | **3,3%** |

### Cuatro anti-metas — errores de KR que la evidencia ya descarta

Esto es lo más accionable del análisis para este archivo: **no** fijar KRs sobre estas bases.

1. **No fijar una meta única de penetración para los tres roles.** El C-Level lleva cinco meses entre 9,5% y 13,3% mientras el PM pasó de 1,8% a 11,9% en cinco meses. Una meta común castiga a un rol posiblemente cerca de su techo y subestima a los otros dos. **Metas diferenciadas por rol.**
2. **No usar volumen de interacciones como KR.** El 6% de los usuarios genera ~43% de las interacciones: mover ese número equivale a mover a dos docenas de personas. La métrica de salud es **la forma de la distribución**.
3. **No usar calidad percibida (thumbs up/down) como KR.** La tasa de feedback explícito es del **1,5%**; el ratio 9:1 a favor mide quién se molesta en calificar, no si MAIA es buena. Requiere instrumentar otra cosa.
4. **No confundir alcance con intensidad.** Son dos palancas separables que responden a tipos de release distintos (→ `08-roadmap`). Un solo número no las captura, así que un KR único los promedia y esconde el movimiento real.

### Dos huecos que la estrategia tiene que cubrir

**Ninguna métrica actual mide valor entregado, solo uso.** Nada de lo medido dice si una interacción cambió una decisión operativa, evitó un desvío o protegió un margen. El candidato más directo: el evento de **aprobación explícita de acciones** del pilar de Governance, que existe en el producto y no se está registrando.

**El portafolio de la vertical de AI está medido a medias: dos features con baseline, el resto sin instrumentar.** _(Corregido el 2026-08-18, dos veces: este bloque decía primero que "no tiene ninguna métrica", y después encuadraba el problema como "fuera de MAIA". MAIA es un miembro del portafolio, no el portafolio — ver la tabla en `01-producto`.)_

- **Marketplace (agentes custom) sí tiene baseline:** 57 companies habilitadas, **1,40% de penetración en jul-26 con intensidad 17,7** — poca gente muy metida, el perfil inverso al de MAIA. Pero **es consumo, no creación**: el funnel de creación de agentes está instrumentado y sin pullear, así que no se sabe si la penetración baja viene de que no se crean agentes o de que los creados no se usan.
- **Workflows, automatizaciones y risk management no tienen ninguna métrica.** Entregan valor en **trabajo ejecutado**, no en consultas — un chat se evalúa razonablemente por frecuencia de uso, un workflow automatizado no.

> ⚠️ **Marketplace no se puede sumar ni comparar de frente contra MAIA:** otra base habilitada (57 companies contra 128), otro universo de roles (incluye Colaborador) y una definición de interacción más estricta. Detalle en `06-kpi-tree`.

### Modelo de negocio de MAIA — estado real

MAIA es **gratuita para toda la base de beta testers** (128 companies al 13-ago-2026). El **único revenue** asociado proviene de un servicio de **consultoría de AI** ejecutado entre Producto y CSM, cobrado como extra por licencia sobre tres clientes que ya son de COR (Sancho BBDO, Publicis, Robin). **No hay todavía casos de upsell de licencias por uso de MAIA** fuera de ese marco.

> **Tensión de pricing a resolver:** el servicio se cotiza **por licencia**, pero produce 1 a 3 usuarios muy profundos por cuenta en lugar de adopción amplia — las cuentas de Sancho tienen la intensidad más alta de toda la base (10 y 20 interacciones por usuario) con penetración de 1,5% y 3,8%. Si eso se sostiene, **el valor entregado y el precio cobrado se apoyan sobre bases distintas**. Marcado como hipótesis en `06`: n = 4 cuentas.
>
> **Hipótesis asociada, con muestra de tres:** los tres contratos se cerraron en momentos en que MAIA **pasó de responder a accionar** (Sancho justo después del MVP de la tool para crear tareas; Publicis y Robin con el bloque de tools de acción ya maduro). Si se sostiene, la variable que predice disposición a pagar no sería cuánto se usa MAIA sino **si ejecuta trabajo**. → `08-roadmap`.

### Decisiones abiertas de la vertical de AI

| Decisión | Evidencia disponible |
|---|---|
| ¿Cuál es la meta de penetración, y es la misma para los tres roles? | C-Level 5 meses entre 9,5% y 13,3%; PM de 1,8% a 11,9% en cinco meses; mejores cuentas >23% |
| ¿Cómo se reparte capacidad entre construir **capacidades** y construir **superficie**? | Ver `08-roadmap`: abril (capacidades) movió intensidad y no alcance; mayo (superficie) duplicó alcance |
| ¿Qué se hace con los **543 asientos dormidos**? | 8 cuentas, intensidad 1 a 2,2. Crowe Global, escala y antigüedad similares, llegó a 23,6% |
| ¿Se **libera MAIA a toda la base**, y bajo qué criterio? | 12% de las cuentas habilitadas nunca registró un usuario. Liberar multiplica el denominador sin evidencia de que mueva el numerador. **Ya no es del todo hipotético por rol:** el Orquestador (22-jul-26) le dio acceso al Colaborador desde header y tareas — la ampliación empezó por producto antes de que existiera la decisión de negocio |
| ¿Cuál es la propuesta de valor para el rol **Colaborador**? | **El acceso ya existe** (header y tareas, desde el Orquestador); lo que falta es la propuesta de valor y la métrica. Excluido de la medición por decisión de scope, no por falta de acceso. Son 5.605 asientos — más que todo el universo elegible actual (3.775) |
| ¿Cuál es el **modelo de negocio** de MAIA fuera de la consultoría? | El único revenue actual produce 1 a 3 usuarios profundos por cuenta. Hay cuentas gratuitas con penetración muy superior |
| ¿Qué rol juega la **elección de modelo**? | El cambio a Sonnet 4.5 en marzo coincide con el segundo mayor salto de penetración de la serie (→ `01-producto`) |
| ¿Cómo se miden las **otras features del portafolio**? | Marketplace ya tiene baseline de consumo (1,40% jul-26); le falta la **creación**. Workflows y risk management no tienen ninguna métrica: entregan valor en trabajo ejecutado, no en consultas |
| ¿Qué se hace con **Marketplace**? ¿Es una apuesta de producto o una feature de nicho? | 57 companies habilitadas, 1,40% de penetración en jul-26. **MullenLowe Delta es el 87% de las interacciones** y una sola persona ahí explica ~un tercio del volumen total. **36 de 57 companies nunca registraron un usuario** (49% de los asientos). El Director es el único rol con penetración de dos dígitos (29,1%, sobre 55 asientos — señal, no magnitud). Falta todo el dato de creación de agentes |

## OKRs del trimestre

> ⚠️ **Pendiente — confirmado con el owner:** todavía no existen OKRs de Producto definidos por eje/squad (`02-equipos`: Coherencia de dinero y negocio, Coherencia de datos, AI, Fundamentals COR, GGN-GUT). Cuando se carguen, probablemente vengan estructurados **por eje** en lugar de (o además de) un set único de Producto. Cargar acá apenas estén definidos, con este formato:

### O1 — _(Objetivo)_
- **KR1:** _(métrica: valor actual → meta)_
- **KR2:** …

_(agregar los objetivos que apliquen, idealmente etiquetados por eje/squad)_

## Marco de priorización

Producto prioriza combinando dos ejes:

1. **Alineación a las 3 prioridades del plan** (apertura de nuevos verticales, thought leadership por vertical, deploy de AI en clientes) — una iniciativa pesa más si sirve directamente a alguna de las tres.
2. **Valor vs. esfuerzo** — dentro de lo alineado, se prioriza por relación de impacto esperado sobre costo de implementación.

No es un framework formalizado tipo RICE con scoring numérico, sino un criterio cualitativo de dos ejes.

## Pendientes — input interno

- [ ] OKRs de producto del trimestre (objetivos + key results con valor actual y meta) — pendiente, probablemente vengan por eje/squad.
  - ⚠️ **Para el eje de AI ya hay baseline y cuatro anti-metas** (ver sección "Cómo laddera Producto a Deploy de AI en clientes"). **Bloqueo:** no fijar el KR de penetración hasta recalibrar el 11,6% con el corte por solo `AI_CHAT_SEND` (pendiente en `06-kpi-tree`).
- [x] Cómo laddera Producto a "Deploy de AI en clientes": ¿qué métrica de producto la mide? _(Resuelto 2026-08-17: **penetración sobre asientos elegibles**, con metas diferenciadas por rol. Ver sección dedicada. Sigue abierto el laddering de las otras dos prioridades.)_
- [ ] **Definir outcome y meta para las features del portafolio de AI todavía sin métrica** (workflows/automatizaciones, risk management, y la **creación** de agentes en Marketplace) — entregan valor en trabajo ejecutado, no en consultas, así que la vara de MAIA no les sirve. _(Marketplace tiene baseline de **consumo** desde el 2026-08-18; sale de esta lista por consumo y sigue adentro por creación.)_
  - ⚠️ **Depende de una definición previa:** si workflows y risk management son features hermanas o pilares de MAIA (ver criterio de Feature Access en `01-producto` → "El portafolio de la vertical de AI"). De eso depende si llevan métrica propia o se miden dentro de MAIA.
- [ ] **Definir el modelo de negocio de MAIA** más allá del servicio de consultoría, resolviendo la tensión de cotizar por licencia un valor que se concentra en 1 a 3 personas.
- [x] Marco de priorización de Producto. _(Alineación a las 3 prioridades del plan + valor vs. esfuerzo; no es un framework formal tipo RICE.)_
- [x] Propagar la expansión de verticales/EMEA a `03-personas` y `04-mercado`. _(Hecho.)_
