# 08 — Roadmap (COR)

> **Última actualización:** 2026-08-31
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
| **Superficie y descubribilidad** | **Sí** | Poco | Mayo-26 (*kick actions* derivadas de las tools de abril, sin capacidad nueva): **2,05x** ⚠️ _confounder: **Risk Management se habilitó el 14-may** — ver abajo_. Junio-26 (*MAIA en tareas*, superficie nueva): 1,33x. **Julio-26 (Orquestador, 22-jul): test en curso — ver abajo** |
| **Calidad del modelo** | **Sí** | No | Marzo-26 (cambio a Sonnet 4.5 + mejoras de UX de base): **1,90x**, el segundo mayor salto de la serie |
| **Nada** | **Retrocede** | — | Diciembre-25, sin iteraciones: **0,38x** — pero ver la salvedad de estacionalidad abajo |

**El experimento natural de abril y mayo** es el caso más limpio: en abril se soltó un conjunto considerable de tools de acción y la penetración no se movió; en mayo, con **esas mismas tools ya en producción**, se duplicó. Lo único que cambió fue el agregado de *kick actions* — la superficie que hace que la capacidad se descubra sin que el usuario sepa pedirla.

> ⚠️ **Confounder detectado el 2026-08-19: Risk Management se habilitó el 14-may-2026.** "Lo único que cambió" era falso. El salto de mayo puede no ser de las *kick actions*.
>
> ```
> MAIA:  abr 104  →  may 219 (+115)  →  jun 323 (+104)  →  jul 373 (+50)
> RM:    abr   0  →  may 119         →  jun 232 (+113)  →  jul 234  (+2)
> ```
>
> **Los incrementos de MAIA y los aportes de Risk Management coinciden casi exactamente tres meses seguidos**, incluido el freno de julio. **La hipótesis del eje no se cae** —*kick actions* y banner de riesgo son las dos superficie, así que las dos empujan en la misma dirección— **pero el ejemplo que la ilustra está mal atribuido**, y es la evidencia principal del lado de superficie.
>
> **Acción:** marcar el **14-may-2026** en la serie como marca de release, igual que se hizo con el Orquestador del 22-jul-26. **Sin esa marca, mayo no sirve como test de nada.**

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

> 💡 **Un tercer dato para este test, que apareció el 2026-08-21 con la reescritura de O1.** El Orquestador **agregó un hop antes del primer token**, así que el KR4 de O1 (performance, TTFT) lo mide de costado: **si hay mediciones de TTFT a ambos lados del 22-jul-26, la resta es el costo en latencia del Orquestador.** Eso convierte al test en una cuenta de dos lados —**cuánta superficie compró y cuánta latencia costó**— en lugar de solo la primera mitad. **Y si la referencia disponible de 1,5–2,5s es anterior al 22-jul, no es baseline de nada: es de otra arquitectura.** Pedido cargado como **Corte H** en `06-kpi-tree`.
>
> ⚠️ **Con lo que hay hoy, el Orquestador apunta en contra por los dos lados:** no movió alcance, y sumó un hop en el camino al primer token de una base que llega con **95% de menciones negativas sobre performance**.

#### Caso de contraste: Marketplace quedó del lado equivocado de la hipótesis

> _Cargado el 2026-08-18 con el baseline de Marketplace (`06-kpi-tree`)._

Marketplace es **capacidad sin superficie**, y es el caso más extremo disponible: el agente existe, pero **queda fuera de la orquestación** — MAIA no lo deriva, el usuario tiene que saber que existe y elegirlo a mano del selector. Es exactamente el modelo que MAIA abandonó el 22-jul.

**Lo que muestra el dato:** **1,40% de penetración** en jul-26 sobre 57 companies habilitadas, **0,44% si se saca MullenLowe Delta**, y **36 de 57 companies sin un solo usuario en diez meses**. Al mismo tiempo, **intensidad 17,7 contra 6,2 de MAIA**: quien lo encuentra lo usa mucho más.

> **Por qué importa para el reparto:** es el patrón que la hipótesis predice —capacidad alta, alcance mínimo, intensidad alta— en una feature entera y no en un mes suelto. Y a diferencia del experimento de abril-mayo, no depende de mover 40 usuarios a 41.
>
> **Por qué no cierra la hipótesis:** es correlación estructural, no un test. Marketplace también tiene menos base habilitada, permisos de creación más restrictivos (de fábrica solo Director y C-Level crean) y un caso de uso menos obvio que "preguntale algo de tu proyecto". No se puede aislar la falta de superficie de esas otras tres explicaciones.
>
> ⚠️ **Verificación previa:** falta el funnel de creación de agentes (🔴 en `06`). Si resulta que casi no se crean agentes, el problema es de creación y no de descubribilidad, y este caso **no aplica a la hipótesis**. No usarlo como evidencia antes de ese chequeo.

**Tema candidato derivado —** no cargar como iniciativa todavía, depende de la verificación de arriba: **poner los agentes custom dentro de la orquestación**, para que MAIA derive a un agente de la empresa cuando la consulta es de su dominio, en lugar de exigir que el usuario lo busque en el selector. Sería el test más limpio posible de la hipótesis: misma capacidad, superficie nueva.

#### Caso a favor: Risk Management es superficie casi pura

> `[HIPÓTESIS FUERTE]` — _misma etiqueta que el eje, sujeta al cruce de solapamiento. Cargado el 2026-08-18 con el baseline de Risk Management (`06-kpi-tree`)._

Es **el caso más limpio disponible del lado de superficie**, y el complemento exacto de Marketplace: **cero capacidad nueva sobre MAIA** —el backend ya calculaba los desvíos, MAIA solo los narra y ofrece acciones— y **54-72% del alcance mensual de MAIA** en la serie may-jul-26 (63% en julio, que es el mes **más bajo** de los tres).

| | Marketplace | Risk Management |
|---|---|---|
| Capacidad nueva | Alta (agentes a medida) | **Cero** (el backend ya calculaba) |
| Superficie | **Mínima** — fuera de la orquestación, hay que buscarlo en el selector | **Máxima** — banner dentro del proyecto, donde el usuario ya está |
| Alcance | 1,40% de penetración, 0,44% sin MullenLowe | **⏸️ penetración en pausa (ver `06`) · 63% del alcance de MAIA** en jul-26 (54-72% en la serie may-jul) |
| Intensidad | **17,7** | **2,0** |

Las dos features apuntan en la misma dirección desde extremos opuestos: **la capacidad sin superficie no expande la base; la superficie sin capacidad nueva sí la expande, pero produce contacto corto.**

> **Por qué importa para el reparto:** es evidencia de feature entera, no de un mes suelto, y no depende de mover 40 usuarios a 41. Si se sostiene, **sube de prioridad el tema candidato ya anotado** —meter los agentes custom dentro de la orquestación—, porque sería aplicarle a Marketplace exactamente lo que le funcionó a Risk Management.
>
> **Por qué todavía no es un hecho:** falta el cruce de **solapamiento MAIA / banner por usuario** (🔴 en `06`). Si casi todos los usuarios de banner ya usaban MAIA por otra vía en el mismo mes, **el banner reencauzó tráfico en lugar de crear alcance** y el 63% deja de ser evidencia de expansión. Es una sola consulta de Amplitude.
>
> **Salvedad de lectura — corregida el 2026-08-19:** la intensidad de 2,0 y el reparto **54-72% de los usuarios contra 19-32% de las interacciones** dicen que la superficie es **puerta de entrada, no puerta de paso**: trae mucha gente y casi nadie sigue hacia el resto de MAIA. _(La versión anterior sostenía esto con el "83% aparece en un solo mes". **Ese número quedó retirado como evidencia de no-retorno** — no controla por fecha de alta, ver `06-kpi-tree`. La conclusión se mantiene por otra vía.)_
>
> ⚠️ **Y hay un dato en contra del entusiasmo:** entre junio y julio la base de Risk Management se multiplicó por 3,5 y **los usuarios quedaron planos (232 → 234)**. Las 79 companies habilitadas en julio **no aportaron usuarios netos**. La superficie funcionó para las primeras 15 companies; **no se replicó al escalar**. Eso es un problema de activación y va como target de discovery en `07` — pero también matiza cuánto se le puede pedir a "poner superficie" como palanca genérica.

**Salvedad sobre diciembre.** El "0,38x sin releases" tiene un confounder no tratado: **diciembre en LATAM es mes de vacaciones**, y el documento fuente no menciona estacionalidad. Test barato con datos que ya tenemos: mirar el DAU/MAU global de COR en dic-25 (`06-kpi-tree`) — si cayó toda la plataforma, el claim se cae solo. Hasta entonces, "la base decae sin releases" es `[HIPÓTESIS]`.

## Temas candidatos (derivados de la estrategia y de la evidencia — validar contra el roadmap real)

> _Inferidos de `05-estrategia-okrs` y `07-discovery`. Son hipótesis de hacia dónde *debería* apuntar producto, NO el roadmap comprometido._

> 🚨 **Marca de release que reordena todo este bloque: la semana del 24-ago-2026 MAIA se libera a toda la base de COR** (~300 clientes, ~172 companies nuevas, incorpora al rol Colaborador). _(Cargado el 2026-08-19 con los OKRs.)_ **La decisión se tomó fuera de Producto**, así que la cobertura deja de ser una variable que el área controla; lo que queda por demostrar es la validación.
>
> **Qué le hace a estos temas:**
> - El **tema 0** deja de ser "deuda a resolver antes de escalar" y pasa a ser **deuda expuesta a toda la base**. Su prioridad sube sin que haya cambiado ninguna evidencia.
> - El **tema 2** (activación) se vuelve el más urgente: **172 companies entrando el mismo día es el experimento de activación más grande que COR va a correr**, y el precedente de julio dice que habilitar no activa. Hay **dos cosas que instrumentar antes del release** o el experimento se pierde (ver pendientes).
> - El **valor relativo de las ocho cuentas dormidas sube justo cuando todo lo demás se diluye** por el salto de denominador (la penetración cae de 11,6% a ~2,6% el mismo día sin que nada empeore).
>
> ✅ **Y estos temas ya no son solo hipótesis de dirección: los OKRs de la vertical de AI están fijados** (`05-estrategia-okrs`, 2026-08-19). O1 cubre el tema 0, O2 cubre el tema 2. **Varios candidatos a KR se bajaron deliberadamente a iniciativa por ser milestones y no resultados** — instrumentar un evento, corregir los cálculos de nivel proyecto, poner workflows en producción, definir el modelo de negocio. **El trabajo sigue siendo necesario; lo que no es, es un KR.**

0. **Fundamentos: performance, calidad y mobile** ⬅️ _nuevo, con evidencia_
   - *Qué:* velocidad y estabilidad de la plataforma, reducción de bugs, experiencia mobile, señal/ruido de notificaciones.
   - *Por qué:* son los dolores #1 medidos (`07`: performance 95% neg, bugs 100% neg, mobile 96% neg) y **erosionan la promesa de "tiempo real"** que sostiene el posicionamiento. Impacta directo en NRR/GRR.
   - *Evidencia nueva (2026-08-18) — la calibración de Risk Management:* **el desvío promedio supera el umbral "Alto" en las diez métricas del backend que lo tienen configurado** —la undécima directamente no tiene umbral cargado— (1,5x a 2,6x en las de nivel tarea, órdenes de magnitud en las de proyecto). Bajo y Medio existen en la tabla de umbrales y casi no existen en la base, así que **la jerarquía de severidad no informa**: el donut, el badge y el orden de la tarjeta quedan vacíos de contenido. Sumado a eso, **cuatro cálculos de nivel proyecto producen porcentajes imposibles** (hasta 24.814.759.071%). **Es deuda de producto, no de infraestructura**, y afecta directamente a la feature que más alcance aporta hoy (63% de los usuarios de MAIA). Detalle en `06-kpi-tree`.
   - *Métrica de éxito:* NPS de heavy users (−33.5 → meta), p95 de carga, crash rate mobile. **Sumar:** % de detecciones que caen en Bajo/Medio (hoy ~0) como proxy de que la severidad discrimina. **Y desde el 2026-08-21, para la parte de MAIA: TTFT <3s en ≥95% de las consultas** (KR4 de O1) — con la salvedad de que **la referencia de 1,5–2,5s puede ser de otra arquitectura**, ver abajo.
   - ✅ *Cubierto por **O1** — 🔄 **revisado el 2026-08-31** (`05-estrategia-okrs`).* El objetivo pasa a llamarse **"Ejecución sin fallas"** y baja a **tres KRs**: **conversaciones sin fricciones por error (50% → 70%, críticas = 0)**, **éxito de ejecución (85% → 95%)** y **performance sostenida durante el escalamiento (≥95% con primer token <3s, todos los meses, manda el peor)**. **El KR de archivos se retiró** y baja a corte del árbol de ejecución y KPI del tablero. **El KR1 dejó de medir alcance de capacidades y pasa a medir calidad de ejecución** — criterio: ***MAIA tenía cómo y falló***. _(El objetivo se llama "Ejecución confiable" desde la reescritura del 21-ago, cuando pasó de cinco KRs a cuatro.)_ **El release sigue siendo su justificación explícita:** la deuda de calidad pasa de "resolver antes de escalar" a **exponerse a ~300 clientes**, con una base que ya llega con NPS −27,8.
   - 🎯 *Lo que la redefinición del KR1 le suma a este tema (2026-08-27):* **es el único KR de O1 que se puede medir sin construir nada** —el instrumento existe— y **el único con dueño natural claro: el equipo técnico/QA**, que tiene palanca sobre código *y* prompt. ⚠️ **Lo que le falta es lo que mató al KR anterior de esta familia: nombre propio y cadencia.**
   - 🚨 *Y lo que le suma el baseline del 2026-08-31, que es el dato más duro que tiene este tema:* **una de cada dos conversaciones se rompe técnicamente (50%)** — y **el número no estaba inflado por fricciones de alcance**: excluye `datos`, `capacidad` y `feature`. **El tema 0 deja de apoyarse en NPS y menciones negativas y pasa a tener una tasa de falla medida.** ⚠️ **Con la meta cumplida (70%), 3 de cada 10 conversaciones siguen fallando: es una escala, no un destino.**
   - 🔴 *El dato que decide cuánta capacidad pide este tema:* **la apertura de ese 50% en `bug` / `nlu` / `incompleta`.** **Si domina `nlu`, el trabajo es prompt y ruteo; si domina `bug`, es ingeniería. Son dos trimestres distintos y hoy no se sabe cuál** — no se puede dimensionar el tema 0 sin eso.
   - 🎯 *Lo que la reescritura del 21-ago le suma a este tema:* **el 95% de menciones negativas sobre performance tiene por primera vez un KR enfrente** (TTFT <3s) — el único KR de O1 con referencia numérica. ⚠️ **Cubre MAIA, no la plataforma:** p95 de carga y crash rate mobile de COR siguen sin KR y sin trackear.
   - 🚫 *Y le suma un hueco:* **se retiró la precisión verificada, así que ningún KR mide si MAIA dice la verdad.** Los cuatro miden si *hizo* algo, ninguno si lo que hizo era *correcto*. **Se registra al lado de la deuda de cálculos y por el mismo motivo: las dos apoyan su prioridad en convicción y no en medición** — y ahora son la misma cosa. La conversión de apertura y los tickets por 100 usuarios también se retiraron; los tres retiros están registrados en `05-estrategia-okrs`.
   > 🔁 **Nuevo input estructurado de roadmap (2026-08-27).** Las fricciones de tipo `datos` (el usuario quiere **saber** algo que las tools no traen), `capacidad` (quiere que MAIA **haga** algo que no puede) y `feature` (pedido explícito de funcionalidad) **salieron del KR1** y pasan a alimentar directamente esta sección. **Salen de la misma corrida que el KR —no cuestan una medición aparte—** y traen los cortes que antes eran del KR: **por dominio** (qué especialista tiene el hueco) y **por tipo de fallo de acceso** (el dato no existe / existe pero el especialista no llega / permisos), que es el corte que separa **un pedido a Data** de **un desarrollo del squad**.
   >
   > ⚠️ **No son KRs de O2.** O2 tiene sus cuatro KRs fijados desde el 2026-08-19 y **no se toca**. Estos tres tipos son **drivers cualitativos de O2**: son la respuesta al *"por qué probaron MAIA y no volvieron"* que hoy es el target de research más urgente del repo (`07-discovery`). **Queda escrito porque, si no, en el primer review alguien los va a proponer como KR.**
   - 🚫 *Lo que deliberadamente **no** lleva KR:* **los cuatro cálculos de nivel proyecto y la calibración de umbrales.** Se decidió dejarlos como iniciativa. **Registrarlo con todas las letras: con el release exponiendo esto a toda la base, su prioridad se apoya en convicción y no en medición.** Si el tema 0 compite por capacidad contra algo que sí tiene KR, esta parte va a perder por construcción.

1. **Madurez de MAIA**
   - *Qué:* llevar los *agentic workflows* de roadmap a producto; Risk Management de **beta** a GA (y más allá del nivel proyecto); definir el **modelo de negocio de MAIA**.
   - *Por qué:* prioridad "Deploy de AI en clientes" + monetización pendiente.
   - *Evidencia nueva (2026-08-17):* el único revenue de MAIA hoy es el servicio de consultoría sobre tres clientes, y **no hay casos de upsell de licencias por uso**. Los tres contratos se cerraron en momentos en que MAIA **pasó de responder a accionar** — hipótesis con n=3, pero si se sostiene, lo que predice disposición a pagar no es cuánto se usa MAIA sino **si ejecuta trabajo**. Eso empuja los *agentic workflows* y las tools de acción por delante de las capacidades de consulta. Ver `05-estrategia-okrs`.
   - *Evidencia nueva (2026-08-18) — Risk Management GA:* este archivo pedía fechas. **Cargado como recomendación de Producto, no como dato: no está en condiciones de GA.** No por falta de features —los 10 riesgos se calculan y se muestran— sino porque **cuatro cálculos de nivel proyecto producen porcentajes imposibles** y **la severidad no discrimina** (ver tema 0). Un GA con esos dos defectos expone a toda la base a una tarjeta cuyo ordenamiento y cuyos números no son defendibles. **Condición sugerida de GA:** umbrales recalibrados con distribución real + los cuatro cálculos de proyecto corregidos + al menos un evento de **acción aplicada** instrumentado, para poder decir qué entregó.
   - *Métrica de éxito:* penetración por rol (`06`), **con corte por origen** (banner vs. resto — hoy el 63% del alcance de MAIA entra por banner), y —cuando se instrumente— **eventos de aprobación de acciones** y **acción aplicada desde una respuesta de riesgo** como proxies de trabajo ejecutado.

2. **Activación de la base ya habilitada de MAIA** ⬅️ _nuevo (2026-08-17), la mejor relación valor/esfuerzo disponible_
   - *Qué:* playbook de activación para las cuentas grandes habilitadas que no arrancaron. **Ocho cuentas Enterprise concentran 543 asientos elegibles —17% del universo— con 18 usuarios activos y una intensidad de 1 a 2,2**: no son usuarios que usan poco, son personas que probaron y no volvieron. Otras 15 companies (149 asientos) nunca registraron un solo usuario en diez meses.
   - *Por qué:* llevar esos asientos al promedio de la base agregaría **~45 usuarios activos** y **no requiere construir nada nuevo**. Es también la explicación de por qué la cohorte marzo-abril rinde peor que la de 2025 (8,8% contra 14,6%): en esa tanda entraron los elefantes dormidos.
   - *Insumo disponible:* **Crowe Global** se habilitó en jun-26 con escala comparable (123 asientos) y llegó a **23,6% de penetración con 8,7 interacciones por usuario**. Misma escala, alta más reciente, resultado opuesto. Entender qué pasó ahí es el insumo más valioso para el playbook → `07-discovery`.
   - ⚠️ *Verificación previa obligatoria:* depurar el denominador con el **estado de actividad/churn por company** (pendiente en `06`). Si parte de esas ocho cuentas está dormida en COR en general, el asiento no existe y el problema no es de MAIA. **No dimensionar la iniciativa antes de ese chequeo** — es el más barato de la lista y cambia el tamaño del premio.
   - *Evidencia nueva (2026-08-19) — el problema de activación se repite en Risk Management, y es más grande:* entre el inicio de junio y el cierre de julio la base habilitada de Risk Management pasó de **15 a 111 companies** —**55 el mismo día, el 8-jul**— y los usuarios únicos quedaron en **232 → 234**. _(Medido con la convención del archivo —asientos al inicio del mes— el salto es de 32 a 111, ×3,5; el punto no cambia.)_ **Las 79 companies habilitadas en julio no aportaron usuarios netos.** Ya no es una iniciativa sobre ocho cuentas dormidas de MAIA: **es un patrón — habilitar no activa**. Y a diferencia del caso de MAIA, este **no necesita ninguna verificación previa de churn**: es aritmética sobre datos que ya están en `06-kpi-tree`. → target de research en `07-discovery`.
   - *Métrica de éxito:* penetración de las cuentas del grupo (3,3% → meta), y cantidad de cuentas habilitadas con al menos un usuario recurrente. **Sumar:** % de companies que registran su primer usuario dentro de los 30 días de habilitadas.
   - ✅ *Las dos métricas de arriba **se volvieron KRs** el 2026-08-19* (`05-estrategia-okrs`, O2): **KR3 — activación de cohorte**, con meta 40% de companies con primer usuario dentro de los 30 días (baseline ~0%, la cohorte de julio de Risk Management); y **KR4 — recuperación de dormidas**, con meta de **6 de 8 cuentas (70%) a ≥20% de penetración con ≥4 interacciones por usuario**, apoyada en que habrá **un CSM dedicado**. El umbral de intensidad está puesto a propósito: sin él, una sesión de onboarding grupal infla el alcance y la cuenta "cumple" mientras sigue dormida.
   - 🔄 *Actualizado el 2026-08-31 — este tema perdió su KR y ganó otro.* **El KR de activación de cohorte y el de recuperación de dormidas se retiraron.** La activación **baja a nodo del árbol de Alcance y a KPI del tablero**; **las 8 dormidas vuelven como candidato en Q1 2027** —siguen siendo 543 asientos, cero desarrollo y ejecutable por el CSM—. **Lo que entró en su lugar apunta a otro rol: la sustitución del flujo de carga de horas del Colaborador (0% → 25%)**, porque **la ventana del Colaborador es ahora**. 🚨 **Y su aritmética reordena el tema:** como *share = penetración × share individual*, **no hay forma de llegar al 25% sin llevar la penetración del Colaborador de 0,27% a ≥25% — ~90x. El cuello de botella no es de producto, es de amplitud:** exposición, comunicación, activación. **Este tema deja de ser "playbook para ocho cuentas" y pasa a ser "cómo se le llega a 5.605 asientos".**
   - ⏰ *Nuevo y urgente (2026-08-19):* **el release del 24-ago es este mismo problema a escala 172.** Si la activación no se instrumenta **con marca de cohorte antes de esa fecha**, no hay KR3 y **el experimento más grande de activación de COR se pierde sin medir** — exactamente lo que pasó en julio con las 79 companies. La meta se bajó de 60% a 40% justamente porque entran de golpe y **sin playbook**: el playbook que sale de Crowe Global llegaría tarde para esta cohorte, pero no para las siguientes.

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
- [ ] ⏰🔴 **VENCIDO — era antes del release del 24-ago: congelar el panel Enterprise + Midmarket e instrumentar la activación con marca de cohorte.** Las dos son consultas, no desarrollo. **Sin la primera no se distingue *mejora* de *dilución*** en toda la serie posterior — **y es parte de por qué hoy no se puede decidir si los 806 usuarios de agosto son el panel o no.** La segunda **ya no bloquea un KR** —activación de cohorte se retiró el 31-ago— **pero sí el nodo leading del árbol de Alcance y el KPI del tablero**. Pedidos cargados en `06-kpi-tree` (cortes F y E).
- [ ] 🔴 **Verificar churn/actividad por company antes de dimensionar el tema 2** (activación de cuentas dormidas) — bloqueante, pendiente en `06-kpi-tree`. **Subió de categoría el 2026-08-19: ahora bloquea un KR** (O2-KR4), no solo el dimensionamiento de una iniciativa. Si el asiento no existe, el KR es incumplible por motivos ajenos a MAIA.
- [ ] **Bajar a iniciativa con dueño y fecha lo que se decidió no medir como KR:** corregir los cuatro cálculos de nivel proyecto, recalibrar los umbrales de severidad, instrumentar el evento de acción aplicada, llevar workflows a producción. **Ninguna lleva KR a propósito** —son milestones, no resultados—, y por eso necesitan dueño explícito o van a perder contra lo que sí se mide.
  - ⬆️ *Se agregaron tres el 2026-08-21, y estas no son milestones: **son KRs retirados** de O1* (`05-estrategia-okrs`). **Auditoría de precisión** (se retiró por no tener dueño ni forma automática — **y con ella nadie mide si MAIA dice la verdad**), **conversión de apertura** (se retiró para no sostener cinco KRs, **no** por fallar el test de resultado vs. entregable) y **tickets por 100 usuarios activos** (meta descendente sin baseline). ⚠️ **La primera y los cuatro cálculos son ahora el mismo problema:** las dos apoyan su prioridad en **convicción y no en medición**, justo cuando el release las expone a ~300 clientes.
- [ ] ⛔ **Especificar el flujo de archivos de MAIA — es un KR (O1-KR3, meta 80%) sin spec y sin un solo dato en el repo.** Entrada y salida como dos líneas desde el primer mes, y el criterio de éxito de tres condiciones al lado de la meta. ⚠️ **La única señal cercana que existe —archivos, 25 menciones, 96% negativas (`07`, I-07)— es de adjuntos en tareas de COR, no de MAIA, y no se cita como evidencia de este KR.** Pedido cargado como **Corte I** en `06-kpi-tree`.
- [ ] **Testear la hipótesis capacidad vs. superficie** antes de usarla para repartir capacidad. **Cuatro** vías abiertas: (a) **cerrar la lectura de agosto** para el test del Orquestador, sobre el panel cerrado y controlando estacionalidad; (b) las interacciones desagregadas por tool/agente — el registro existe, hay que refinarlo y extraerlo (`06`); (c) 🔴 **el solapamiento MAIA / banner por usuario**, que decide si Risk Management creó alcance o reencauzó tráfico; (d) ⚠️ _nueva (2026-08-21)_ **el TTFT a ambos lados del 22-jul-26**, que pone precio en latencia al hop que agregó el Orquestador (Corte H de `06`). **(c) es la más barata de las cuatro: una consulta de Amplitude.**
- [ ] **Decidir el GA de Risk Management** con la recomendación del tema 1 sobre la mesa: hoy Producto recomienda **no ir a GA** hasta corregir los cuatro cálculos de nivel proyecto y recalibrar los umbrales. Es una decisión de Producto, no de IT.
- [ ] **Chequear la estacionalidad de diciembre** contra el DAU/MAU global (`06`) para confirmar o descartar "la base decae sin releases".
- [ ] **Marcar el 14-may-2026 (habilitación de Risk Management) como release en la serie**, igual que el Orquestador del 22-jul. Sin esa marca, mayo no sirve como test del eje capacidad vs. superficie — el salto de 2,05x que hoy se atribuye a las *kick actions* tiene un confounder del mismo signo.
- [ ] 🔥 **Llevar a la conversación de roadmap las dos cosas que conviven mal:** MAIA depende de Risk Management para **54-72% de su alcance mensual**, y Risk Management es la feature sobre la que Producto recomienda **no ir a GA**. Es una decisión conjunta, no dos decisiones.
  - ⚠️ *Agravante del 2026-08-19:* **con el release, esa deuda se expone a ~300 clientes haya GA o no.** Y hay una tensión declarada entre los dos objetivos: **recalibrar la calidad de las detecciones (O1) va a disparar menos alertas, y eso puede bajar el alcance de MAIA (O2) en el corto plazo** — una buena noticia con forma de mala. **Anticiparlo en el primer review** en lugar de descubrirlo cuando el número baje.
