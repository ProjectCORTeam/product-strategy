# 03 — Personas (COR)

> **Última actualización:** 2026-09-05
> **Owner:** Product Manager, área de Producto
> **Contexto para IA:** Perfiles de usuario y segmentos de COR, para diseñar features y evaluar impacto. COR es B2B: el **cliente es la agencia**, y dentro conviven varios **roles-usuario**, cada uno con su capa de permisos. Distinguir **comprador** (quién decide/paga) de **usuarios** (quién opera el producto).

## Segmentos (ICP)

### Estado actual
- **Foco geográfico:** LATAM, países de habla hispana y Brasil.
- **Segmento prioritario: Enterprise** — concentra ~**70% del revenue**.
- **Cortes de segmento (confirmados):**

| Segmento | Corte |
|---|---|
| **Retail** | Menos de 15 personas/licencias. |
| **SMB** | Menos de USD 850 MRR. |
| **Mid Market** | Entre 40 y 70 personas/licencias. |
| **Enterprise** | Más de 70 personas/licencias **o** más de USD 2.500 MRR. |

> ⚠️ _Los criterios son mixtos: Retail y Mid Market se definen por **tamaño de equipo** (licencias), mientras que SMB se define por **MRR** y Enterprise por **cualquiera de los dos** (tamaño o MRR). Además hay una zona sin cubrir entre Retail (<15 personas) y Mid Market (40-70 personas) si se mira solo por headcount — probablemente ahí el corte real lo da el MRR (SMB), no el tamaño de equipo. Vale la pena confirmar cómo se resuelve una cuenta que cae, por ejemplo, en 20 personas pero bajo MRR, o viceversa._
- **Tipos de empresa:** agencias de marketing y publicidad, consultoras, productoras, desarrolladores de software, estudios de diseño y arquitectura, y firmas legales y contables. *Sweet spot* en agencias de más de 40 personas.

### Expansión 2026–2027 (Business Plan — ver `05`)
El core de **agencias LatAm no alcanza para crecer +50% YoY**, por eso el plan abre nuevos **verticales** y **geografías**:

- **Verticales:** Agencias (core), **IT Consulting**, **Law & Accounting**, **Brands** y **Media**.
- **Geografías:** LatAm y Brasil (validados) + **EMEA** (nuevo).

> _Implicación de personas: cada vertical nuevo trae **comprador y usuarios distintos** (un socio de un estudio jurídico o un director de IT no se comportan como una agencia). Las 6 roles-usuario de COR (permisos) probablemente se mantienen, pero los perfiles de comprador y los jobs-to-be-done cambian por industria. Requiere trabajo de personas dedicado por vertical (ver pendientes)._

## Comprador / Decisor

Quien evalúa y firma la compra de COR es el **CFO** o el **líder de Operaciones** de la organización. Le importan la rentabilidad agregada, el control operativo y el ROI. *(Distinto de los usuarios que operan el producto día a día.)*

## Roles de usuario en COR

COR tiene 6 roles de usuario (base, fijos — no se crean roles nuevos), cada uno con una **capa de permisos** distinta. Los **heavy users** son **Colaborador** y **Project Manager**.

**Cómo funciona el sistema de permisos** (fuente: documentación interna de producto): se arma en 3 capas — (1) el **rol** define el perfil base; (2) **permisos por módulo y acción** (Ver/Editar/Crear/Eliminar/Archivar/Facturar, según el módulo); (3) **alcance de visibilidad** sobre cada permiso de Ver (Todos la empresa / Equipo / Solo suyos). Cada empresa puede personalizar el template de permisos de cada rol; lo que sigue es el **estándar de fábrica** con el que arranca una cuenta nueva.

### 1. Colaborador — *heavy user*
- **Quién:** miembro del equipo que ejecuta el trabajo.
- **Permisos (estándar de fábrica):** Tareas con CRUD completo (alcance Todos); Horas con CRUD completo pero **solo las suyas**; Proyectos solo en modo Ver y solo los suyos; Vacaciones y Licencias propias; Notificaciones, Gantt y Agentes AI en modo Ver. **Sin acceso a:** Presupuestos, Clientes, Contratos, Personas, Configuración, Negocio, Salario mensual.
- **Jobs-to-be-done:** cargar horas rápido y sin fricción, tener claras sus tareas.
- **Dolor:** la carga de horas se siente como una tarea administrativa tediosa — **confirmado con evidencia** (`07`, I-02d): es el rol que concentra las quejas de *carga de horas* (48 de 70 menciones negativas), sumando fallas de confiabilidad (horas que no computan o se pierden).
- **Satisfacción (Retently, ago-26):** **NPS −29.0** (n=390). **Se desgasta con el uso:** −15.2 en onboarding → −34.5 en adopción.
- **Relación con COR:** time tracking (web/app, integración de calendario), tareas y archivos.

### 2. Project Manager — *heavy user*
- **Quién:** planifica y controla los proyectos del equipo (lado agencia).
- **Permisos (estándar de fábrica):** gestión amplia con alcance **Todos** en Tareas, Horas, Gantt, Planner, Capacity Planning y Deadlines — no acotado a su equipo. Proyectos con alcance "solo suyos" pero puede crear/editar/archivar (no eliminar). Clientes en Ver/Editar/Crear. **Sin acceso a:** Presupuestos (por eso no ve rentabilidad/performance de proyectos), Personas, Configuración, Negocio, Salario mensual.
- **Jobs-to-be-done:** del brief al proyecto, cumplir deadlines y presupuesto, asignar recursos sin sobrecargar (Planner/capacity), detectar desvíos a tiempo.
- **Dolor:** re-planificación manual, poca visibilidad de capacidad, desvíos que aparecen tarde. **Evidencia (`07`, I-02b/c/d):** es el rol **más insatisfecho de todos** y ya arranca mal en onboarding; sus quejas top son usabilidad, performance y **app mobile**.
  > ⚠️ _Posible factor estructural: de fábrica, el PM no tiene acceso a Presupuestos, que es el permiso que habilita ver la **rentabilidad/performance de proyectos** (`06-kpi-tree`). Si esto no se ajusta por cuenta, el PM opera el proyecto sin ver el indicador de rentabilidad que en teoría debería guiar sus decisiones — una hipótesis a cruzar con discovery._
  > _**Reforzado el 2026-08-18 con Risk Management:** el permiso de Presupuestos también condiciona el desvío de **costo vs. ingresos**, el único de los 10 riesgos con lectura financiera. El PM es el rol que más abre banners (147 usuarios en jul-26) y es el que no puede ver ese riesgo. Ver "Adopción de Risk Management por rol", más abajo._
- **Satisfacción (Retently, ago-26):** **NPS −40.7** (n=248) — el peor de los 6 roles. Onboarding −46.8 → adopción −38.7.
- **Relación con COR:** núcleo operativo del producto + automatización con MAIA.

### 3. Director
- **Quién:** liderazgo de área o de cuentas dentro de la agencia.
- **Permisos (estándar de fábrica):** gestión transversal con alcance **Todos** en casi todos los módulos (Proyectos, Presupuestos, Tareas, Clientes, Personas, Horas, Vacaciones, Plantillas de proyecto), incluye Negocio (Ver/Editar) y Agentes AI (Ver/Editar/Crear, sin Eliminar). **Sin acceso a:** Salario mensual.
- **Jobs-to-be-done:** cuidar la salud de las cuentas, controlar retrabajos y rentabilidad por cliente, mostrar performance del equipo.
- **Dolor:** retrabajos que erosionan el margen sin notarse a tiempo.
- **Satisfacción (Retently, ago-26):** **NPS −11.7** (n=77) — de los mejores; **mejora con el uso** (−33.3 onboarding → −8.8 adopción). Su queja distintiva es la **búsqueda**.
- **Relación con COR:** rentabilidad por cliente, "Analyze with MAIA", dashboards.

### 4. C-level
- **Quién:** dirección ejecutiva de la agencia.
- **Permisos (estándar de fábrica):** acceso total (Ver/Editar/Crear/Eliminar, y Archivar/Facturar donde aplica) a **todos** los módulos con alcance Todos, incluyendo **Salario mensual** — es el único rol con visibilidad completa de sueldos de fábrica — y Agentes AI. Editar el template de permisos de un rol (Configuraciones → Permisos) está reservado exclusivamente a C-Level.
- **Jobs-to-be-done:** rentabilidad real del negocio, KPIs por proyecto/cliente, ROI (incluido el de la inversión en AI).
- **Satisfacción (Retently, ago-26):** **NPS −11.9** (n=42). Valora el acompañamiento del **CSM**.
- **Relación con COR:** dashboards ejecutivos e insights de dirección de MAIA.

### 5. Rol Cliente
- **Quién:** el cliente externo de la agencia.
- **Permisos (estándar de fábrica):** solo **Ver**, y solo sobre Proyectos, Tareas y Clientes con alcance "solo suyos" (los proyectos donde fue invitado), más Notificaciones. Sin acceso a ningún otro módulo. Un usuario Cliente sin proyectos asignados no ve nada al entrar al producto.
- **Jobs-to-be-done:** seguir el avance de sus proyectos, colaborar y aprobar.
- **Relación con COR:** portal de acceso a cliente.

### 6. Freelancer
- **Quién:** colaborador externo o temporal.
- **Permisos (estándar de fábrica):** Tareas solo **Ver + Crear** (sin Editar/Eliminar, alcance solo suyas), Horas con CRUD completo (solo suyas, igual que Colaborador), Proyectos y **Clientes** en modo Ver (solo suyos), Notificaciones y Gantt (solo suyos), Contraseñas (Ver, solo suyas). **Sin acceso a:** Presupuestos, Deadline de tareas, Contratos, Personas, Configuración, Negocio, **Capacity Planning**, **Vacaciones y Licencias**, Operación, Plantillas de proyecto, Salario mensual, **Agentes AI**.
- **Diferencia real vs. Colaborador (confirmado):** Freelancer no puede editar ni eliminar sus propias tareas (solo verlas y crearlas), y no tiene Vacaciones y Licencias, Capacity Planning ni Agentes AI — permisos que Colaborador sí tiene. A cambio, Freelancer sí ve Clientes (solo los suyos), algo que Colaborador no tiene. En conjunto, Freelancer es un perfil más acotado y "de solo ejecución" que Colaborador — coherente con ser un rol externo/temporal.
- **Jobs-to-be-done:** ejecutar sus tareas y cargar sus horas.
- **Satisfacción (Retently, ago-26):** **NPS +17.9** (n=39) — **el único rol con NPS positivo**. Hipótesis: uso más acotado y superficial ⇒ menos exposición a la fricción operativa. _(n chico: tratar como señal.)_
- **Relación con COR:** tareas asignadas y time tracking.

## Comportamientos y adopción

**Evidencia de satisfacción por rol** (Retently, ago-2026 — detalle en `07-discovery`):

| Rol | NPS | n | Lectura |
|---|---:|---:|---|
| Freelancer | **+17.9** | 39 | Único positivo (uso acotado) |
| Director | −11.7 | 77 | Mejora con el uso |
| C-level | −11.9 | 42 | Capa de reporting, menos fricción |
| Colaborador | −29.0 | 390 | *Heavy user* — se desgasta con el uso |
| Cliente | −33.3 | 12 | n muy chico |
| Project Manager | **−40.7** | 248 | *Heavy user* — el peor; malo desde onboarding |

### Adopción de MAIA por rol (2026-08-17)

Corrige una lectura previa: **los tres roles con MAIA habilitada adoptan a tasas equivalentes.** Normalizada por asientos, la penetración de jul-26 es **PM 11,5% · Director 10,8% · C-Level 13,3%**. La aparente dominancia del PM (56% de los usuarios) era un **efecto de tamaño de base** — hay 1.917 asientos de PM contra 458 de C-Level — y quedó dada de baja en `06-kpi-tree` (`[BAJA-01]`).

Lo que sí distingue a los roles es la **intensidad**:

| Rol | Int./usuario (acum.) | Lectura |
|---|---:|---|
| **C-level** | **8,2** | El más intensivo. 18% de los usuarios, 25% de las interacciones. Penetración estancada desde marzo |
| Project Manager | 5,2 | Indistinguible del Director en comportamiento; la diferencia es volumen de asientos |
| Director | 5,2 | Ídem |

**Implicancia para personas:** el rol que más profundamente usa MAIA es el **C-level**, no el PM — lo opuesto a lo que sugiere el volumen bruto. Y su curva de penetración lleva cinco meses plana, lo que abre una pregunta abierta de discovery (`07`): ¿es saturación real del rol, o falta de valor específico para él?

> ⚠️ _El rol **Colaborador** está excluido de esa medición y se mide sobre denominador propio: son **5.605 asientos**, más que todo el universo hoy elegible para MAIA (3.775). 🔄 **Actualizado el 2026-08-31: ya no es un rol sin propuesta de valor** — ver la ficha, abajo._

#### El Colaborador y MAIA — ficha propia _(decidida el 2026-08-19 · **fundamento reemplazado el 2026-08-31**)_

> 🔄 **Cambio de fondo el 2026-08-31: el fundamento por el que este rol estaba fuera de los KRs venció.** Este archivo decía que **el rol no tenía propuesta de valor definida** y que **su primer paso era discovery, no un KR**. **Con la propuesta de carga de horas asistida por MAIA, el rol tiene propuesta de valor** — y pasa de **ficha sin meta** a **universo propio con KR propio**: **O2 · KR6 — sustitución del flujo de carga de horas (0% → 25%)**, sobre el denominador de **5.605 asientos** (`05-estrategia-okrs`).
>
> **El 0,27% se mantiene como dato, recalificado.** Deja de ser *"evidencia de que el rol no tiene caso de uso"* y pasa a ser **baseline pre-propuesta** — se reporta como **KPI del tablero, sin meta**, porque mide **cuánta gente toca MAIA**, no **cuánto flujo pasa por MAIA**. ⚠️ **Y no sirve como punto de partida del KR6:** describe un rol que todavía no tenía caso de uso, así que **el baseline real sale de la primera medición de septiembre.**
>
> 🚨 **La aritmética del KR6 le pone número a lo que este rol necesita.** Como *share de horas = penetración × share individual*, **no hay combinación que llegue al 25% sin que la penetración pase de 0,27% a por lo menos 25%: un salto de ~90x.** **El cuello de botella de este rol no es de producto, es de amplitud** — exposición, comunicación, activación.
> ⚠️ **`[HIPÓTESIS]` desde el 2026-09-02: el ~90x no está verificado.** Se apoya en que el segundo factor tiene techo en 100%, **y eso solo vale si los dos factores corren sobre la misma población** — hoy no corren. **Qué lo refutaría:** que una parte grande de los 5.605 elegibles **no cargue horas en una ventana de 28 días**; ahí el techo desaparece y **el multiplicador podría ser bastante menor**. Lo resuelve una consulta al backend, pedida para antes del 27-sep. Detalle en `06-kpi-tree`.
>
> 🔄 **Precisiones del 2026-09-02 (ver `05-estrategia-okrs` y `06-kpi-tree`).** El KR6 mide **horas cargadas**, no capacidad teórica; corre sobre **ventana de 28 días con lectura semanal**, no mes calendario; y su universo son los **colaboradores con MAIA habilitada** — **la habilitación es por company y su fecha se guarda**. **El 0,27% sigue siendo KPI del tablero sin meta**, y sigue sin servir como punto de partida del KR6: **el baseline real sale del cierre del 06-sep**.
>
> 📌 **El discovery no se cae: cambia de rol en el plan.** Ya no es *"el primer paso en vez de un KR"*, es **el insumo cualitativo de un KR que ya existe** — y sigue teniendo ventana.

**Con el release del 24-ago-2026 MAIA se libera a toda la base de COR y el Colaborador entra completo.** Eso obliga a decidir cómo se lo mide, y la decisión es **no mezclarlo con los otros tres roles**:

| | Colaborador | Panel PM + Director + C-Level |
|---|---|---|
| Asientos | **5.605** _(elegibles: colaboradores con MAIA habilitada)_ | ~3.775 (128 companies, pre-release) |
| Usuarios recurrentes | **~15** | 373 (jul-26) |
| **Penetración** | **0,27%** | **11,6%** |
| Estado | 🔄 **Con propuesta de valor desde el 31-ago** (carga de horas asistida) **y KR propio: O2 · KR6** | Con caso de uso y KRs |

**El 0,27% no se leía como un problema de adopción** _(lectura del 19-ago, que se conserva porque explica de dónde viene el número)_. Estaba dos órdenes de magnitud por debajo de los roles con caso de uso definido, y **eso era exactamente lo esperable para un rol al que nadie le había dicho todavía para qué sirve MAIA**. 🔄 **Desde el 31-ago la propuesta existe, así que el mismo número pasa a ser línea de largada en vez de explicación.** Compararlo contra el 11,6% sería el mismo error de denominador de `[BAJA-01]`, con una vuelta más: acá ni siquiera es el mismo producto, porque no hay propuesta de valor que evaluar.

**Consecuencias de medición:**

1. **Denominador y métrica separados.** El Colaborador **no entra** en el panel Enterprise + Midmarket que sostiene los KRs de O2 (`05-estrategia-okrs`). Si entrara, la penetración caería de 11,6% a ~2,6% el mismo día **sin que nada empeore**.
2. 🔄 **Su primer paso ya no es "discovery en vez de un KR": tiene KR (O2 · KR6) y el discovery lo alimenta.** Con ~15 personas usándola hoy, **son 15 entrevistas posibles** — el research más barato disponible en todo el repo, y con ventana: **después del release el grupo deja de ser identificable.** → `07-discovery`.
3. ⚠️ **Ojo con el contexto de satisfacción al leer los resultados:** el Colaborador es el rol que **se desgasta con el uso** (NPS −15,2 en onboarding → −34,5 en adopción). Lo que sea que MAIA le ofrezca, entra sobre esa base.

> _Salvedad de dato: los 413 usuarios de la tabla de distribución de frecuencia de `06-kpi-tree` **sí incluyen al Colaborador** —es la única tabla que Amplitude no entrega abierta por rol—, mientras que los 373 de la serie de penetración lo excluyen. Es la razón por la que el pedido de **histograma abierto por rol** subió de prioridad._

### Qué hace cada rol con MAIA — jobs medidos `[HECHO — 2026-09-05]`

> **Fuente:** export de conversaciones del **2 al 4-sep-26** (316 conversaciones reconstruidas, 243 usuarios, 89 companies), procesado con la skill `maia-usage-insights`. ⛔ **Salvedad: el export estaba truncado en 1.000 filas — son 1,9 días hábiles, no un mes. Sirve para composición, no para frecuencia ni tendencia.** Detalle y cortes en `06-kpi-tree`.

% de conversaciones **dentro de cada rol**:

| Job | C-Level | Director | PM | Colaborador |
|---|---:|---:|---:|---:|
| Cargar horas propias | 12,5 | 15,5 | 25,9 | **62,9** |
| Riesgo (banner) | 15,6 | 14,1 | 19,0 | **0,0** |
| Crear / editar tareas y proyectos | 3,1 | 9,9 | 14,7 | 6,2 |
| Supervisar horas del equipo | **31,2** | 11,3 | 5,2 | 5,2 |
| Análisis de desvío / rentabilidad | **15,6** | 7,0 | 3,4 | 0,0 |
| Carga masiva por archivo | 0,0 | 0,0 | **7,8** | 0,0 |

**Job principal por rol:** **Colaborador → cargar horas (62,9%)** · **PM + Director → gestionar el trabajo del equipo (39,6%)** · **C-Level → enterarse del estado del negocio (65,6%)**.

**Tres cosas que esto le cambia a este archivo:**

1. ✅ **El dolor del Colaborador con la carga de horas deja de estar inferido y pasa a estar medido por comportamiento.** Ya estaba confirmado por feedback (`07`, I-02d: 48 de 70 menciones negativas de carga de horas son suyas); ahora se ve que **casi dos tercios de lo que le pide a MAIA es exactamente eso**. **Es la evidencia más fuerte que tiene la propuesta de carga asistida** (→ el KR6 de O2).
2. 🔄 **El C-Level queda caracterizado como rol que lee, no que opera:** **solo el 15,6% de sus conversaciones escribe**, y **47% es supervisión de horas del equipo más análisis de desvío y rentabilidad**. **Es el fundamento del KR nuevo de O2** —*estado del negocio consultado por MAIA*— y **la razón por la que a este rol no se lo puede medir por escritura: quedaría en cero por construcción**.
3. ⚠️ **El Director es el único rol cuya escritura es mayoritariamente estructural** (27 escrituras estructurales contra 10 de horas). **Se parece al PM en el job pero no en el perfil de escritura** — por eso el KR de gestión **se reporta con PM y Director por separado** _(anti-meta 1)_.

**Fricción por rol** `[HECHO]`, del mismo export: **C-Level 59,4%** · Colaborador 42,3% · Director 35,2% · **PM 31,9%**.

> ⚠️ **El C-Level fricciona más que ningún otro rol** — y es el rol al que se le acaba de poner un KR que depende de **repetición semanal**. **Leer sus primeros cierres con esto puesto.**
>
> 🔴 **Y hay un comportamiento de estos tres roles que no está en ningún denominador:** **25 PMs, 11 Directores y 4 C-Levels cargaron sus propias horas por MAIA en 1,9 días.** **No entra en *Sustitución del flujo de horas*** —denominador = asientos de Colaborador— **ni en *Gestión ejecutada*, que lo excluye por diseño.** ⚠️ **Es la tercera vez que este comportamiento se queda sin denominador**, y hay una decisión abierta en `05-estrategia-okrs`.

### Patrón central: intensidad de uso vs. satisfacción

Cuanto **más intensivo** es el uso del producto, **peor** la satisfacción. Los roles operativos (PM + Colaborador) son el 79% del volumen de feedback y los más críticos; los roles de lectura/agregado están claramente mejor. El dolor vive en la operación diaria, no en el reporting.

_(Es una lectura del bloque de NPS de arriba, no del bloque de Risk Management que sigue.)_

### Adopción de Risk Management por rol (2026-08-18)

Risk Management (los banners de riesgo dentro del proyecto) tiene el **mismo universo de roles que MAIA**: PM, Director y C-Level. **Colaborador, Freelancer y Cliente no ven banners.**

**Usuarios de banners por rol, jul-26** `[HECHO]` — **penetración ⏸️ en pausa** `[SIN VALOR PUBLICABLE]`

| Rol | Usuarios únicos | Composición | Penetración |
|---|---:|---:|---|
| Project Manager | 147 | 63% | ⏸️ en pausa |
| Director | 59 | 25% | ⏸️ en pausa |
| C-level | 29 | 12% | ⏸️ en pausa |

> ⏸️ **Puesta en pausa el 2026-08-19.** Las cifras que estuvieron cargadas (PM 7,7% / Director ~6,9% / C-Level 6,3%) usaban los **asientos elegibles de MAIA** (1.917 / ~850 / 458). Risk Management **tiene base propia**: 119 companies, y en julio solo **32 estaban habilitadas al inicio del mes**. Es el mismo problema de denominador que puso en pausa la penetración global de la feature — ver `06-kpi-tree`. **Los conteos de usuarios y la composición no se tocan; los porcentajes sí.**

✅ **Pendiente cerrado de paso:** el denominador de asientos de **Director** ya no está inferido. El export de altas del 19-ago-26 trae dato duro: **923 asientos de Director** en la base de Risk Management (865 al 1-ago-26). _La inferencia por resta (~850) era correcta. Ojo: es la base de Risk Management (119 companies), no la de MAIA (128)._

**Confirma igual el patrón de `[BAJA-01]` en una feature distinta.** En bruto el PM parece dominar —**63% de los usuarios únicos de banners son PM**—, y esa composición replica exactamente la de MAIA, donde el mismo 56-63% resultó ser efecto de tamaño de base. **La conclusión —no leer composición como preferencia de rol— se sostiene aunque los porcentajes estén en pausa**, porque el sesgo está en el numerador bruto, no en el denominador. _(Ojo al citar: hay otro 63% dando vueltas en este análisis, el de "usuarios de MAIA que entran por banner". Son cosas distintas.)_ Es el **segundo caso registrado del mismo sesgo de denominador**, ahora en una feature que no es el chat. Registrarlo como tal: cada vez que aparezca un corte por rol en bruto, normalizar antes de leerlo.

**Refuerza el hallazgo abierto de Presupuestos** `[HALLAZGO]`**.** El desvío de **costo vs. ingresos** —el único riesgo con lectura financiera— exige el permiso de **Presupuestos**, que el PM **no tiene de fábrica**. O sea: **el rol que más entra a proyectos no puede ver el único desvío que habla de rentabilidad.** La evidencia de uso lo acompaña: **8 consultas en tres meses**, con una conversión a conversación de 12,5% contra un baseline de 31,4%. A eso se le suman otros dos estrechamientos sobre la misma métrica: aplica solo a 1.326 proyectos (los que tienen Ingreso total configurado) y solo se dibuja en pérdida real. Son **tres filtros apilados sobre el desvío que sostiene la propuesta de valor del producto**.
_⚠️ Por qué es `[HALLAZGO]` y no `[HECHO]`: **n = 8 consultas**. La dirección (el permiso estrecha el alcance del riesgo financiero) es sólida y replica el patrón ya conocido de Presupuestos; **la magnitud no se puede afirmar con esa muestra**, y el 12,5% de conversión va con la misma salvedad en `06-kpi-tree`. No usarlo para dimensionar una iniciativa._

> ⚠️ **Anomalía de agosto — pendiente de verificación, NO cargar como hallazgo.**
>
> | Rol | Interacciones jul → ago | Únicos jul → ago |
> |---|---|---|
> | Project Manager | 328 → 67 (**−80%**) | 147 → 46 |
> | Director | 109 → 26 (−76%) | 59 → 16 |
> | C-level | 42 → **40 (−5%)** | 29 → 9 |
>
> El C-Level **sostiene volumen con un tercio de los usuarios**: 4,4 interacciones por usuario en agosto contra 1,45 histórico. Con **n=9** eso pueden ser una o dos personas. Es el **único segmento que no cae** y **contradice la lectura previa de que el C-Level no se engancha con banners**. **Verificar antes de escribir cualquier conclusión de rol** — y ojo con la estacionalidad de julio-agosto, ya marcada como confounder abierto en `08-roadmap`.

## El "champion" de adopción

El **champion** es una persona **dentro de la organización cliente** (no de COR) que actúa como promotor del uso de COR puertas adentro. No es un rol-usuario formal de COR (no está entre los 6 roles de permisos) sino un papel informal que puede recaer en cualquiera de ellos. Se caracteriza por tener contacto e ida y vuelta frecuente con el **CSM** asignado a la cuenta, y es un factor clave para transmitir el valor de COR internamente y sostener la adopción.

> _Pendiente: cómo arranca el rollout típico en una cuenta nueva y si hay un patrón de qué rol suele ejercer de champion (¿el comprador/CFO? ¿el PM? ¿otro?)._

## Pendientes — input interno

- [x] Validar/ajustar la capa de permisos real de cada rol. _(Cargado el estándar de fábrica por rol, fuente: documentación interna de producto. Nota: cada empresa puede personalizar su template — esto es el punto de partida, no necesariamente lo que tiene cada cuenta hoy.)_
- [x] Diferencia concreta entre **Freelancer** y **Colaborador**. _(Ver sección 6 — Freelancer no edita/elimina tareas propias y no tiene Vacaciones, Capacity Planning ni Agentes AI; sí ve Clientes, a diferencia de Colaborador.)_
- [x] Definición del segmento "Retail". _(Menos de 15 personas/licencias.)_
- [x] Cortes exactos de los segmentos: SMB, Mid Market, Enterprise. _(Ver tabla arriba. Criterios mixtos tamaño/MRR — zona gris entre Retail y Mid Market a confirmar.)_
- [x] Quién es el "champion" de adopción. _(Persona interna del cliente, no un rol formal de COR; con contacto frecuente con el CSM.)_
- [ ] Cómo arranca el rollout típico en una cuenta nueva, y qué rol suele ejercer de champion.
- [ ] **Personas por vertical nuevo** (IT Consulting, Law & Accounting, Brands, Media): comprador, usuarios y jobs-to-be-done propios de cada industria.
- [x] ~~**Propuesta de valor de MAIA para el rol Colaborador**~~ ✅ **Resuelto el 2026-08-31: carga de horas asistida por MAIA**, con KR propio (O2 · KR6) sobre los 5.605 asientos. ⚠️ **Lo que queda abierto no es la propuesta sino la amplitud:** la aritmética del KR pide llevar la penetración de 0,27% a ≥25%, **~90x**, y eso es exposición y comunicación, no producto. _Historia del pendiente:_ ⚠️ _Actualizado el 2026-08-19: **ya no condiciona la liberación a toda la base — el release se decidió igual, fuera de Producto, para la semana del 24-ago.** El pendiente no se cierra: se vuelve más urgente, porque ahora el rol tiene acceso completo sin que exista la propuesta. **Ficha de medición propia cargada arriba** (0,27%); el primer paso acordado es **discovery sobre los ~15 usuarios actuales**, con ventana antes del release (`07-discovery`)._
- [ ] **¿La meseta del C-level es saturación o falta de valor para el rol?** Ver `07-discovery` (tema abierto de MAIA) y `06-kpi-tree` (hipótesis etiquetada).
  - ⚠️ **Dato nuevo en tensión (2026-08-18):** en Risk Management el C-Level es el **único rol que no cae en agosto** (−5% de interacciones contra −80% del PM), sosteniendo 4,4 int./usuario contra 1,45 histórico. Con n=9 no alcanza para nada, pero **apunta en dirección contraria a "el C-Level no se engancha"**. Verificar antes de cerrar la pregunta.
- [x] **Denominador real de asientos de Director.** _(Resuelto 2026-08-19: **923 asientos** en la base de Risk Management, 865 al 1-ago-26. La inferencia por resta era correcta.)_
- [ ] **Recalcular la penetración de banners por rol** con la base propia de Risk Management y la cohorte correcta. Hoy en pausa; depende del 🔴 de `06-kpi-tree`.
- [ ] **Decidir si el acceso del PM a Presupuestos es configuración o decisión de producto.** Ya estaba abierto desde la visión (`01-producto`); Risk Management lo vuelve más concreto — el rol que más abre banners no puede ver el único riesgo financiero.
