# 08 — Roadmap (COR)

> **Última actualización:** 2026-08-17
> **Owner:** Product Manager, área de Producto
> **Contexto para IA:** Qué construye COR, por qué y cuándo, para evaluar prioridades y explicar la dirección. El **roadmap real** aún no está cargado; los temas de abajo están **derivados de la estrategia** (`05`) y marcados como candidatos a validar, no como el roadmap oficial. No inventar fechas ni compromisos.

## Cómo leer este roadmap

Cada ítem debería tener: **qué** (la iniciativa), **por qué** (la prioridad/OKR que sirve), **cuándo** (horizonte) y **métrica de éxito** (`06-kpi-tree`). Horizontes: **Now / Next / Later** (o por trimestre).

## Tensión a resolver: plan de negocio vs. evidencia de clientes

> _Insumo para la discusión de priorización, no una decisión tomada._

El **Business Plan** (`05`) empuja hacia **expansión** (nuevos verticales, EMEA, deploy de AI). La **evidencia de clientes** (`07`, Retently ago-26) muestra una **base con problemas de fundamentos**: NPS global −27.8, heavy users en −33.5 (PM −40.7), performance 95% de menciones negativas, bugs 100%, mobile 96%.

Las dos cosas chocan en un punto concreto: el plan depende de **NRR 115% y GRR 90%** (el +$1.02M de installed base), y la retención se apoya en una base de usuarios hoy insatisfecha. Expandir a nuevos verticales con un producto que los heavy users del core califican mal traslada el problema a mercados nuevos.

**Pregunta a resolver con el Head de Producto:** ¿cuánta capacidad va a *fundamentos* (performance, UX, mobile, confiabilidad de horas) vs. a *expansión* (verticales, AI)? Hoy el plan no lo explicita. _(Confirmado con el owner: esta conversación todavía no se dio — sigue pendiente.)_

### Segundo eje de reparto, dentro de AI: capacidad vs. superficie

> `[HIPÓTESIS FUERTE — no usar como hecho para repartir capacidad todavía]`
> _Cargada el 2026-08-17 desde *MAIA — Análisis de adopción y penetración v3.0*. Es la conclusión más accionable del análisis y la que descansa sobre la evidencia más fina, así que entra como hipótesis con test asociado. Métrica y salvedades en `06-kpi-tree`._

Cruzando la cronología de releases de MAIA contra las series de penetración e intensidad aparece un patrón que separa dos palancas hasta ahora confundidas en un solo número:

| Tipo de release | ¿Mueve alcance? | ¿Mueve intensidad? | Evidencia observada |
|---|---|---|---|
| **Tools y capacidades nuevas** | No | **Sí** | Abril-26: penetración 1,02x (de 40 a 41 usuarios en el panel fijo), pero intensidad de 4,6 a 6,0 — el salto más grande de la serie — y **nace el bucket de 51-100 interacciones**, que había estado en cero cinco meses |
| **Superficie y descubribilidad** | **Sí** | Poco | Mayo-26 (*kick actions* derivadas de las tools de abril, sin capacidad nueva): **2,05x**. Junio-26 (*MAIA en tareas*, superficie nueva): 1,33x. **Julio-26 (Orquestador, 22-jul): test en curso — ver abajo** |
| **Calidad del modelo** | **Sí** | No | Marzo-26 (cambio a Sonnet 4.5 + mejoras de UX de base): **1,90x**, el segundo mayor salto de la serie |
| **Nada** | **Retrocede** | — | Diciembre-25, sin iteraciones: **0,38x** — pero ver la salvedad de estacionalidad abajo |

**El experimento natural de abril y mayo** es el caso más limpio: en abril se soltó un conjunto considerable de tools de acción y la penetración no se movió; en mayo, con **esas mismas tools ya en producción**, se duplicó. Lo único que cambió fue el agregado de *kick actions* — la superficie que hace que la capacidad se descubra sin que el usuario sepa pedirla.

> **Por qué importa para el reparto:** construir capacidad **no expande la base de usuarios por sí solo**. La expande la superficie donde esa capacidad se vuelve visible. Y aplica igual a workflows, marketplace y risk management, no solo a MAIA.
>
> **Por qué todavía no es un hecho:** el mes crítico son ~40 usuarios en un panel de 34 cuentas; pasar de 40 a 41 puede ser una sola cuenta activando gente. Granularidad mensual, sin control ni aleatorización, y varios meses combinan más de un tipo de cambio. Es además el claim de **mayor carga** del análisis — se lo va a usar para repartir capacidad del squad, así que la barra es la más alta.
> **Qué la refutaría:** un release de superficie que no mueva alcance, o uno de capacidad que sí lo mueva.
> **Tests disponibles:** (1) el Orquestador, abajo; (2) las interacciones desagregadas por tool/agente — **el registro de qué especialista intervino ya existe** (queda guardado para análisis y debug según la documentación funcional), así que el pedido a Data pasa de "instrumentar" a **"refinar y extraer"**, confirmado con el owner. Sigue pendiente en `06`.

#### Test en curso: el Orquestador (deploy 22-jul-2026)

> _Cargado el 2026-08-17. **Es el mejor caso de la tabla**: release aislado (no salió nada más ese día, confirmado con el owner), fecha exacta, tipo declarado **antes** de mirar el resultado y predicción explícita. Los otros cuatro casos son reconstrucciones retrospectivas donde varios meses mezclan más de un tipo de cambio._

**Qué es:** MAIA pasa a punto de entrada único y el usuario deja de elegir agente (→ `01-producto`). Es **superficie pura**: no agrega capacidades, reduce la fricción de descubrirlas.

**Predicción de la hipótesis:** debería **mover alcance y no intensidad**.

**Estado — apunta en contra.** Julio no sirve como corte (21 días sin Orquestador, 9 con; cerró en 11,6% contra 11,5% de junio, o sea plano). El primer mes limpio es **agosto**, y el parcial de 13 días marca **6,0% de penetración con 6,6 de intensidad** contra 11,6% / 6,2 de julio: camino a un mes normal en alcance, con intensidad levemente arriba. **Es el patrón inverso al predicho.** No alcanza para refutar con el mes abierto, pero es exactamente lo que la hipótesis declara que la refutaría.

**Cómo leerlo cuando cierre agosto — dos confounders:**

1. **Leer sobre el panel cerrado de 34 cuentas, no sobre el agregado.** Agosto suma 15 companies y 335 asientos elegibles; cada tanda de altas entra con penetración baja y arrastra el promedio. Sobre el agregado, el Orquestador compite contra el denominador y pierde por razones ajenas al release.
2. **Estacionalidad.** Julio-agosto son vacaciones de invierno en varios mercados de LATAM. Mismo test barato que ya está abierto para diciembre-25: contrastar contra el DAU/MAU global de COR (`06`).

**Salvedad sobre diciembre.** El "0,38x sin releases" tiene un confounder no tratado: **diciembre en LATAM es mes de vacaciones**, y el documento fuente no menciona estacionalidad. Test barato con datos que ya tenemos: mirar el DAU/MAU global de COR en dic-25 (`06-kpi-tree`) — si cayó toda la plataforma, el claim se cae solo. Hasta entonces, "la base decae sin releases" es `[HIPÓTESIS]`.

## Temas candidatos (derivados de la estrategia y de la evidencia — validar contra el roadmap real)

> _Inferidos de `05-estrategia-okrs` y `07-discovery`. Son hipótesis de hacia dónde *debería* apuntar producto, NO el roadmap comprometido._

0. **Fundamentos: performance, calidad y mobile** ⬅️ _nuevo, con evidencia_
   - *Qué:* velocidad y estabilidad de la plataforma, reducción de bugs, experiencia mobile, señal/ruido de notificaciones.
   - *Por qué:* son los dolores #1 medidos (`07`: performance 95% neg, bugs 100% neg, mobile 96% neg) y **erosionan la promesa de "tiempo real"** que sostiene el posicionamiento. Impacta directo en NRR/GRR.
   - *Métrica de éxito:* NPS de heavy users (−33.5 → meta), p95 de carga, crash rate mobile.

1. **Madurez de MAIA**
   - *Qué:* llevar los *agentic workflows* de roadmap a producto; Risk Management de **beta** a GA (y más allá del nivel proyecto); definir el **modelo de negocio de MAIA**.
   - *Por qué:* prioridad "Deploy de AI en clientes" + monetización pendiente.
   - *Evidencia nueva (2026-08-17):* el único revenue de MAIA hoy es el servicio de consultoría sobre tres clientes, y **no hay casos de upsell de licencias por uso**. Los tres contratos se cerraron en momentos en que MAIA **pasó de responder a accionar** — hipótesis con n=3, pero si se sostiene, lo que predice disposición a pagar no es cuánto se usa MAIA sino **si ejecuta trabajo**. Eso empuja los *agentic workflows* y las tools de acción por delante de las capacidades de consulta. Ver `05-estrategia-okrs`.
   - *Métrica de éxito:* penetración por rol (`06`), y —cuando se instrumente— **eventos de aprobación de acciones** como proxy de trabajo ejecutado.

2. **Activación de la base ya habilitada de MAIA** ⬅️ _nuevo (2026-08-17), la mejor relación valor/esfuerzo disponible_
   - *Qué:* playbook de activación para las cuentas grandes habilitadas que no arrancaron. **Ocho cuentas Enterprise concentran 543 asientos elegibles —17% del universo— con 18 usuarios activos y una intensidad de 1 a 2,2**: no son usuarios que usan poco, son personas que probaron y no volvieron. Otras 15 companies (149 asientos) nunca registraron un solo usuario en diez meses.
   - *Por qué:* llevar esos asientos al promedio de la base agregaría **~45 usuarios activos** y **no requiere construir nada nuevo**. Es también la explicación de por qué la cohorte marzo-abril rinde peor que la de 2025 (8,8% contra 14,6%): en esa tanda entraron los elefantes dormidos.
   - *Insumo disponible:* **Crowe Global** se habilitó en jun-26 con escala comparable (123 asientos) y llegó a **23,6% de penetración con 8,7 interacciones por usuario**. Misma escala, alta más reciente, resultado opuesto. Entender qué pasó ahí es el insumo más valioso para el playbook → `07-discovery`.
   - ⚠️ *Verificación previa obligatoria:* depurar el denominador con el **estado de actividad/churn por company** (pendiente en `06`). Si parte de esas ocho cuentas está dormida en COR en general, el asiento no existe y el problema no es de MAIA. **No dimensionar la iniciativa antes de ese chequeo** — es el más barato de la lista y cambia el tamaño del premio.
   - *Métrica de éxito:* penetración de las cuentas del grupo (3,3% → meta), y cantidad de cuentas habilitadas con al menos un usuario recurrente.

3. **Valor en la base instalada (Deploy de AI)**
   - *Qué:* features que suban adopción y valor entregado en clientes existentes.
   - *Por qué:* sostener/superar **NRR 115%** y blindar el churn 2027.
   - *Evidencia nueva (2026-08-17):* **los tres roles adoptan MAIA a tasas equivalentes** (PM 11,5% / Director 10,8% / C-Level 13,3% en julio) — la lectura anterior de "MAIA es una herramienta de PM" era un efecto de tamaño de base y quedó dada de baja en `06`. No priorizar valor de AI asumiendo que el PM es el usuario dominante.

4. **Fricción de onboarding y time tracking** _(reforzado con evidencia)_
   - *Qué:* reducir el costo de cargar horas y **corregir la confiabilidad** (`07`, I-05: horas que no computan o se pierden). Atacar dos problemas distintos: el **Colaborador se desgasta con el uso** (−15.2 → −34.5) y el **PM arranca mal en onboarding** (−46.8).
   - *Por qué:* activación y retención; el dato de horas es la base de toda la rentabilidad — si no es confiable, el core de valor de COR queda comprometido.
   - *Métrica de éxito:* delta NPS onboarding→adopción del Colaborador; cobertura y precisión de horas.

## Roadmap (real — a completar)

> _Cargar los ítems reales con: qué / por qué (prioridad u OKR) / cuándo / métrica de éxito / owner._

### Now — _(Qx 2026)_
- _(pendiente)_

### Next
- _(pendiente)_

### Later
- _(pendiente)_

## Principios de roadmap / cómo se decide

> _Pendiente: cómo se decide qué entra al roadmap (alineación a las 3 prioridades, criterio del Head de Producto, capacidad de squads, deuda técnica). Enlaza con el marco de priorización de `05`._

## Enlaces entre archivos

- Prioridades y OKRs que el roadmap debe servir → `05-estrategia-okrs`.
- Métrica de éxito de cada iniciativa → `06-kpi-tree`.
- Evidencia que justifica cada apuesta → `07-discovery`.

## Pendientes — input interno

- [ ] Roadmap real (iniciativas y horizontes/fechas).
- [ ] Validar o reemplazar los temas candidatos.
- [ ] **Definir el balance fundamentos vs. expansión** (ver tensión arriba) — decisión de capacidad con el Head de Producto.
  - Sumar a esa conversación el **segundo eje de reparto dentro de AI**: capacidad vs. superficie (ver arriba). Cargado con evidencia el 2026-08-17, todavía como hipótesis.
- [ ] Métrica de éxito por iniciativa. _(Parcial: los temas 1, 2 y 4 ya tienen métrica; el 0 y el 3 no.)_
- [x] Estado de MAIA en el roadmap. _(Cargado 2026-08-17 con el análisis de adopción: baseline de penetración, evidencia de monetización y la iniciativa de activación de la base ya habilitada. Sigue pendiente el estado de los agentic workflows y de Risk Management GA como fechas de roadmap real.)_
- [ ] Principios de priorización del roadmap.
- [ ] 🔴 **Verificar churn/actividad por company antes de dimensionar el tema 2** (activación de cuentas dormidas) — bloqueante, pendiente en `06-kpi-tree`.
- [ ] **Testear la hipótesis capacidad vs. superficie** antes de usarla para repartir capacidad. Dos vías abiertas: (a) **cerrar la lectura de agosto** para el test del Orquestador, sobre el panel cerrado y controlando estacionalidad; (b) las interacciones desagregadas por tool/agente — el registro existe, hay que refinarlo y extraerlo (`06`).
- [ ] **Chequear la estacionalidad de diciembre** contra el DAU/MAU global (`06`) para confirmar o descartar "la base decae sin releases".
