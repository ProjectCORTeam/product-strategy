# 07 — Discovery (COR)

> **Última actualización:** 2026-08-18
> **Owner:** Product Manager, área de Producto
> **Contexto para IA:** Insights curados de entrevistas, encuestas y datos, para buscar evidencia al tomar una decisión. Cada insight debe tener **evidencia y fuente**; distinguir hallazgos de *research primario* de supuestos o claims de marketing. No inventar insights: si un tema no tiene evidencia cargada, marcarlo como pregunta abierta.

## Formato de un insight

Cada insight se carga con esta estructura:

- **Insight:** el hallazgo en una línea.
- **Evidencia:** qué lo respalda (cita, dato, patrón).
- **Fuente:** entrevista / encuesta / datos de producto / soporte / MAIA / ventas / CS.
- **Confianza:** alta / media / baja (según cantidad y calidad de evidencia).
- **Implicación:** qué significa para producto.
- **Vinculado a:** persona, oportunidad, feature o ítem de roadmap.

## Fuentes de evidencia

- **Entrevistas de usuario** → estructurar con la skill **`interview-snapshot`** del proyecto.
- **Fricciones del agente MAIA** → procesar exports con la skill **`maia-friction-analysis`** (qué no pudo responder/ejecutar, errores, malentendidos, features inexistentes pedidas).
- **Datos de producto** (adopción, uso de features, cobertura de time tracking).
- **Encuestas** (NPS, CSAT, pulsos).
- **Soporte / CS / Ventas** (patrones de tickets, motivos de churn, objeciones de deals).

> _Este archivo es un **repositorio vivo**: se alimenta de forma continua desde esas fuentes. Las dos skills de arriba convierten material crudo (notas de entrevistas, exports de MAIA) en insights listos para curar acá._

## Temas abiertos de discovery (ligados a la estrategia)

> _Preguntas prioritarias a responder con evidencia. Hoy son **preguntas**, no hallazgos — se completan a medida que llega research._

### Adopción y onboarding
- ¿Dónde está la mayor fricción de onboarding? ¿Qué rol adopta primero y cuál se resiste?
- **Time tracking:** ¿por qué la carga de horas se percibe como tediosa? ¿Qué la mejora (calendario, MAIA, recordatorios)?

### Rentabilidad (core de valor)
- ¿Los clientes actúan sobre los insights de rentabilidad, o solo los miran? ¿Qué los lleva a actuar?
- ¿Qué tan confiable perciben el dato de rentabilidad (que depende de la precisión de horas)?

### MAIA
- ¿Qué esperan de MAIA vs. qué reciben? (alimentar con `maia-friction-analysis`).
- ¿Qué agentes/acciones generan valor real y cuáles se abandonan?

> _Dos preguntas nuevas (2026-08-17), derivadas del análisis de adopción. **Son los dos targets de research mejor definidos que tenemos hoy**, porque el dato cuantitativo llega hasta acá y no más: la evidencia está en `06-kpi-tree` (sección de AI) y lo que falta es el porqué. Alimentan directamente el tema 2 del roadmap (`08`)._

- 🎯 **¿Por qué las cuentas grandes probaron MAIA y no volvieron?** Ocho cuentas Enterprise concentran 543 asientos con 18 usuarios activos y una intensidad de 1 a 2,2 interacciones mensuales — el patrón no es "uso bajo" sino **no-retorno tras el primer contacto**. ¿Qué pasó en ese primer uso? ¿Falta de onboarding, expectativa incumplida, ausencia de champion, permisos, desconocimiento de que existe? _(Cuentas: TBWA Multisponsor, Ganem Group, Encender, Garnier Agency, Fahrenheit DDB, MASS DIGITAL, Anagram LATAM, DeNicolas.)_
- 🎯 **¿Qué pasó en Crowe Global?** Alta en jun-26, escala comparable (123 asientos) y **23,6% de penetración con 8,7 interacciones por usuario** — el resultado opuesto al del grupo anterior. Es el caso de éxito más limpio disponible y la base para un **playbook de activación**. ¿Hubo champion? ¿Rollout dirigido? ¿Acompañamiento de CSM? ¿Un caso de uso puntual que prendió?
  > ⚠️ **La pregunta cambia con el dato de Risk Management (2026-08-18).** Crowe es la **2ª cuenta por uso de banners de riesgo: 47 consultas, 24 usuarios**. Es decir que **una parte del 23,6% que queríamos explicar puede ser Risk Management y no MAIA conversacional**. No preguntar "¿por qué adoptaron MAIA?" sino **"¿qué los trajo — el chat o el banner del proyecto?"**. Si la respuesta es el banner, el playbook de activación que salga de acá es un playbook de superficie, no de chat.
- ¿Qué explica que el **C-Level** tenga la intensidad más alta (8,2 int./usuario) y a la vez cinco meses de meseta en penetración? Es la pregunta que decide si su curva plana es saturación real o falta de valor específico para el rol — hoy es hipótesis en `06` y **de eso depende si se invierte en valor para C-Level**.

> _Dos targets nuevos (2026-08-18), derivados del análisis de Risk Management. El primero **vale más que cualquier corte adicional de Amplitude**: el dato cuantitativo ya dice qué pasa y no puede decir por qué._

- 🎯 **La feature engancha en el momento y no genera vuelta. ¿Por qué?** **Continuidad de conversación en 42,6% (agosto)** —de lo poco en todo el repo que mejora mes a mes— contra **83% de los usuarios que aparecen en un solo mes** y 59% que hizo una sola consulta en tres meses. Las dos cosas juntas describen algo **útil pero no incorporado a la rutina**: el usuario que lo toca conversa, y no vuelve. ¿Qué le faltó para volver — que le avise, que resuelva, que le muestre que el riesgo se cerró? _(Recordar: hoy no hay notificación y no hay aviso cuando el riesgo se resuelve — `01-producto`.)_
- 🎯 **¿Importa que la misma pregunta devuelva otra respuesta?** **118 de 130 repeticiones devuelven texto distinto sobre datos idénticos**: mismo usuario, mismo proyecto, mismos números, redacción diferente — en un caso a 30 minutos de distancia. **Es una pregunta de confianza, no de contenido:** ¿el usuario lo nota? ¿lo lee como que el dato cambió? ¿deja de creerle? _(La causa técnica está identificada y va por el canal de la documentación funcional, no por acá.)_

> 📐 **Dato de concentración para diseñar el muestreo** (2026-08-18): el uso de banners se reparte en **73 companies**, y el **top 5 concentra ~32% de las filas del log** — DDB Centro 64, **Crowe Global 47**, Super 35, InPulse Digital 33, CATCH 28. Una muestra que solo entreviste al top 5 describe a un tercio del uso; una que los ignore pierde a los únicos usuarios con volumen suficiente para tener opinión formada.
> ⚠️ _Está calculado sobre las **653 filas** del log, no sobre las **523 consultas distintas** que impone la regla 6 de la convención de fuentes. Sobre consultas distintas el share sube a ~40%. Sirve para diseñar el muestreo; no citarlo como métrica de concentración._

### Verticales nuevos (IT Consulting, Law & Accounting, Brands, Media)
- ¿Qué tan bien encaja el producto agency-first en cada vertical? ¿Qué "Product Adjustments" pide cada uno?
- ¿Cuáles son los jobs-to-be-done y objeciones propias de cada industria?

### Churn y retención (blindaje NRR 115%)
- ¿Cuáles son los motivos reales de churn? ¿Señales tempranas?
- ¿Qué diferencia a las cuentas que expanden de las que se van?

## Insights curados

> _Primera carga de research primario: **Retently** (NPS + CSAT + topics), export del 2026-08-09. Base: **889 respuestas de 206 empresas** (808 NPS / 81 CSAT), mayoría LatAm hispanohablante (Colombia, México, Argentina, Venezuela, Guatemala). Los datos vienen tagueados por **rol (role-1…role-6)** y por **lifecycle (onboarding / adoption)**._
>
> ✅ _Mapeo de roles confirmado: **role-1 = C-level · role-2 = Director · role-3 = Project Manager · role-4 = Colaborador · role-5 = Cliente · role-6 = Freelancer.**_

### I-01 — El NPS global es negativo (−27.8)
- **Evidencia:** NPS = **−27.8** sobre n=808 respuestas (promotores 9-10 vs. detractores 0-6); rating promedio 4.7/10. Distribución: 465 negativas, 312 positivas, 112 neutras.
- **Fuente:** Retently, NPS Español/Inglés/Onboarding, últimos ~12 meses. **Confianza: alta** (n grande, 206 empresas).
- **Implicación:** hay un problema de satisfacción de base, no un ruido puntual. Choca de frente con el objetivo de **NRR 115% / GRR 90%** y el "blindaje 2027" del plan (`05`).
- **Vinculado a:** `05` (riesgo de churn), `06` (NPS como leading indicator de retención).

### I-02 — La satisfacción **empeora con el uso**, no mejora
- **Evidencia:** NPS en **onboarding = −20.9** (n=201) vs. **adoption = −30.1** (n=607).
- **Fuente:** Retently, tags de lifecycle. **Confianza: alta.**
- **Implicación:** el problema no es (solo) el arranque: el uso sostenido erosiona la percepción. Sugiere fricción operativa acumulada más que curva de aprendizaje.
- **Vinculado a:** `03` (adopción), `08` (prioridad de fricción/UX).


### I-02b — Los **heavy users son los más insatisfechos** (hallazgo central)
- **Evidencia:** NPS por rol — **Project Manager −40.7** (n=248), **Cliente −33.3** (n=12), **Colaborador −29.0** (n=390), **C-level −11.9** (n=42), **Director −11.7** (n=77), **Freelancer +17.9** (n=39, único positivo). PM + Colaborador concentran el **79% del volumen** de respuestas y arrojan un NPS combinado de **−33.5**.
- **Fuente:** Retently, tags de rol. **Confianza: alta** en PM/Colaborador (n grande); **baja** en Cliente y Freelancer (n<40).
- **Implicación:** los dos roles que `03-personas` define como **heavy users** son justamente los peor parados, y el peor de todos es el **Project Manager** — el rol que más valor debería extraer del núcleo del producto (proyectos, Planner, capacity). Los roles de lectura/agregado (C-level, Director) están notablemente mejor: el dolor está en **la operación diaria**, no en la capa de reporting.
- **Vinculado a:** `03` (heavy users), `06` (engagement), `08` (prioridad).

### I-02c — El Colaborador se **desgasta con el uso**; el PM arranca mal desde el día uno
- **Evidencia:** NPS onboarding → adopción por rol: **Colaborador −15.2 → −34.5 (−19.3 pp)**; **Project Manager −46.8 → −38.7** (malo ya en onboarding, mejora levemente); **Director −33.3 → −8.8** (mejora con el uso).
- **Fuente:** Retently, cruce rol × lifecycle. **Confianza: alta** en Colaborador y PM.
- **Implicación:** son **dos problemas distintos**. El Colaborador entra tolerante y se desgasta — coherente con la fricción repetitiva de cargar horas. El PM tiene una barrera desde el arranque: onboarding/complejidad inicial del rol más pesado del producto.
- **Vinculado a:** `03` (adopción por rol), `08`.

### I-02d — Cada rol duele por un motivo distinto
- **Evidencia:** top topics negativos por rol —
  - **Colaborador (n=390):** usabilidad 136, performance 66, UI 58, UX 50, **carga de horas 48**, bugs 37.
  - **Project Manager (n=248):** usabilidad 98, performance 62, UI 52, UX 42, **app mobile 26**, tareas 23, bugs 22.
  - **Director (n=77):** usabilidad 22, performance 14, UI 11, **búsqueda 8**.
  - **C-level (n=42):** usabilidad 8, **CSM 6**, performance 6, bugs 5.
  - **Freelancer (n=39):** usabilidad 9, performance 4, **archivos 4**.
- **Fuente:** Retently topics × rol. **Confianza: alta** en Colaborador/PM.
- **Implicación:** **la carga de horas es un dolor específico del Colaborador** (48 de las 70 menciones negativas del topic) — valida el perfil de `03-personas`. **App mobile pesa sobre todo en el PM**, que necesita operar fuera del escritorio. Performance y usabilidad son transversales a todos los roles.
- **Vinculado a:** `03` (dolores por persona), `08`.

### I-03 — Performance (lentitud y caídas) es el dolor más "puro"
- **Evidencia:** 163 menciones, **95% negativas** — el topic con peor ratio entre los de alto volumen. Verbatims: *"Carga todo muy lento. Siempre presenta problemas."*, *"Se cae mucho la plataforma"*, *"Se tilda mucho en general"*.
- **Fuente:** Retently topics + verbatims. **Confianza: alta.**
- **Implicación:** no es preferencia ni falta de features: es calidad de servicio. Erosiona la promesa de "tiempo real" del posicionamiento (`01`, `04`).
- **Vinculado a:** `08` (candidato a Now).

### I-04 — Usabilidad / UI / UX es el bloque de mayor volumen
- **Evidencia:** **usabilidad** 387 menciones (71% neg), **User Interface** 175 (74% neg), **User Experience** 156 (72% neg), **navegación de proyectos** 65 (89% neg), **búsqueda** 29 (100% neg), **panel de tareas** 34 (88% neg). Verbatim: *"es complejo para una plataforma que podría ser más simple"*.
- **Fuente:** Retently topics. **Confianza: alta.**
- **Implicación:** el mayor volumen de queja es de experiencia, no de funcionalidad faltante. Encontrar proyectos/tareas y navegar es un costo recurrente.
- **Vinculado a:** `08`, `03` (heavy users).

### I-05 — La carga de horas se percibe como trabajo en sí misma *(confirma un supuesto de `03`)*
- **Evidencia:** 85 menciones, **82% negativas**. Verbatims: *"cargar horas se convierte en sí mismo un trabajo"*, *"al cargar horas deberían salir todos los proyectos disponibles"*, *"cargo horas y no las va contando como parte de la jornada"*, *"Se eliminan las horas"*.
- **Fuente:** Retently. **Confianza: alta.**
- **Implicación:** valida el dolor que en `03-personas` estaba inferido, y agrega que hay **fallas de confiabilidad** (horas que se pierden/no computan), no solo fricción de UX. Esto ataca la base del dato de rentabilidad (`06`).
- **Vinculado a:** `01` (time tracking), `06` (cobertura y precisión de horas), `08`.

### I-06 — La app mobile es un punto crítico
- **Evidencia:** 50 menciones, **96% negativas**. Verbatims: *"muy mala para usar en el celular. es clave en trabajos 100% remotos"*, *"La experiencia en móviles es muy mala"*.
- **Fuente:** Retently. **Confianza: alta** (para el volumen relevado).
- **Implicación:** COR declara web + mobile (`01`), pero mobile no está a la altura — y aparece ligado a contextos de trabajo remoto.
- **Vinculado a:** `01`, `08`.

### I-07 — Bugs y notificaciones: ruido que desgasta
- **Evidencia:** **bugs** 71 menciones **100% negativas**; **notificaciones** 40 (92% neg), con quejas de alertas irrelevantes o de tareas que ya no le competen al usuario; **archivos** 25 (96% neg).
- **Fuente:** Retently. **Confianza: alta.**
- **Implicación:** calidad y señal/ruido de notificaciones son fricción evitable; las notificaciones mal segmentadas generan fatiga.
- **Vinculado a:** `08`.

### I-08 — El soporte / CSM es una **fortaleza** clara
- **Evidencia:** CSAT de soporte **4.67/5** (n=81; 75 positivas, 3 negativas). El topic **CSM** es de los pocos mayormente positivos (56 menciones, solo 21% negativas).
- **Fuente:** Retently CSAT Customer Support. **Confianza: media-alta** (n moderado).
- **Implicación:** el equipo humano está compensando la fricción de producto. Es un activo de retención — y una señal de que el problema es de producto, no de relación con el cliente.
- **Vinculado a:** `04` (fortaleza percibida), `06` (health score).

### I-09 — Lo que sí valoran: orden, visibilidad y control
- **Evidencia:** topics positivos dominantes: **organización** (59% pos), **orden** (76% pos), **amigable** (48% pos), **control** (47% pos). Verbatims de promotores: *"El orden que brinda en los procesos y la visibilidad de la data en tiempo real"*, *"permite organizar muy bien el trabajo"*.
- **Fuente:** Retently. **Confianza: alta.**
- **Implicación:** la **propuesta de valor central de COR está validada** (orden + visibilidad en tiempo real). El problema está en la ejecución (performance/UX), no en la tesis del producto.
- **Vinculado a:** `01` (propuesta de valor), `04` (posicionamiento).

### I-10 — Señal temprana: idiomas no-español con NPS mucho peor
- **Evidencia:** NPS por idioma — **es: −24.3** (n=744), **en: −64.0** (n=50), **br: −85.7** (n=14).
- **Fuente:** Retently. **Confianza: baja-media** (n chico en en/br; tratar como señal, no conclusión).
- **Implicación:** relevante para la expansión a **Brasil y EMEA** del plan (`05`): si la experiencia fuera del core hispano ya arranca peor, la expansión geográfica necesita validar producto y localización antes de escalar.
- **Vinculado a:** `05` (expansión), `04` (mercado), `03` (personas por geografía).

## Pendientes — input interno

- [x] Primera carga de research primario (Retently NPS/CSAT/topics, ago-2026). _(Hecho — I-01 a I-10.)_
- [x] Mapear `role-1`…`role-6` a los roles de COR. _(Hecho — ver I-02b/c/d.)_
- [ ] Cortar el feedback por **segmento** (Enterprise/Mid/SMB) y por **vertical**, hoy no disponible en el export. _(No hay conector MCP de Retently disponible; se necesita un nuevo export con ese corte.)_
- [ ] Complementar con research cualitativo (entrevistas) sobre performance y carga de horas. _(Confirmado que ese research **ya se hizo**, pero el owner no tiene el material a mano ahora — retomar cuando esté disponible y procesar con `interview-snapshot`.)_
- [ ] Definir cadencia de discovery y quién cura este archivo. _(Existe una práctica de **discovery semanal** en toda COR para tener contacto con usuarios, pero ese research **no se está volcando** a este repositorio hoy — falta definir quién lo cura y cómo se alimenta.)_
- [ ] Conectar el pipeline: `interview-snapshot` y `maia-friction-analysis` → insights acá. _(Decisión: por ahora no se prioriza armar esta conexión formal.)_
- [ ] Priorizar qué tema abierto atacar primero.
- [ ] **Research sobre las 8 cuentas dormidas y sobre Crowe Global** (ver 🎯 en Temas abiertos → MAIA). Bloquea el playbook de activación del tema 2 de `08-roadmap`. Procesar con `interview-snapshot`. **Ajustar el guion de Crowe:** separar chat de banner antes de atribuir el 23,6%.
- [ ] **Research sobre el no-retorno en Risk Management** (🎯, 2026-08-18) — es el target mejor definido que tenemos hoy: engancha en el momento (42,6% de continuidad) y no genera vuelta (83% de un solo mes). **Vale más que cualquier corte adicional de Amplitude.**
- [ ] **Sondear el efecto de la inconsistencia de respuesta** (118 de 130 repeticiones devuelven texto distinto sobre datos idénticos). Pregunta de confianza; se puede meter en el mismo guion que el punto anterior.
- [ ] **Cerrar el loop cuantitativo:** entre el análisis de adopción de MAIA, el de Marketplace y el de Risk Management (todos ago-2026), `06-kpi-tree` acumula **17 pedidos de datos abiertos** (10 de la vertical de AI + 7 de Risk Management, más los de Marketplace listados aparte). **Seis están marcados 🔴 como bloqueantes** de decisiones de roadmap o de KRs.
