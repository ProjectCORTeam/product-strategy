# 01 — Producto (COR)

> **Última actualización:** 2026-08-13
> **Owner:** Product Manager, área de Producto (reporta al Head de Producto)
> **Contexto para IA:** Este archivo describe qué es COR, qué hace y para quién. Es el punto de partida para entender el producto antes de leer cualquier otro archivo.

## Visión de producto

> **Que la rentabilidad sea una decisión diaria y no un hallazgo de fin de mes.**

> ⚠️ **Estatus: propuesta, no oficial (ago-2026).** Redactada por el owner de este repo (PM de Producto). **Pendiente de validación con Nicolás Ocampo (VP Product).** Hasta que se valide, usar como hipótesis de dirección — no citarla como la visión oficial de COR. Antes de esto, COR no tenía visión de producto formalizada.

### Qué dice, en concreto

El enemigo es **la latencia**: hoy la rentabilidad se descubre tarde, cuando ya no se puede hacer nada con ella. La visión no promete más reportes, promete **acortar la distancia entre que algo se desvía y que alguien decide**. Dos palabras cargan el peso:

- **decisión** — no "visibilidad" ni "dashboard": alguien tiene que poder actuar. Ver la rentabilidad sin poder cambiarla no cumple la visión.
- **diaria** — la rentabilidad como ritmo operativo, no como cierre contable.

Es coherente con la tesis ya escrita en el posicionamiento: _la mayoría del software registra lo que ya pasó; COR busca cambiar lo que pasa mientras el trabajo está en curso._

### Cómo se usa para priorizar

**Entra:** todo lo que acorta el ciclo señal → decisión. Esto incluye explícitamente los **fundamentos**: si la plataforma es lenta, si mobile no sirve o si las horas no son confiables (`07`, I-05), **no hay decisión diaria posible** — hay reconstrucción a fin de mes. Bajo esta visión, performance, mobile y confiabilidad del dato de horas no son higiene ni deuda: son **condición de posibilidad** de la visión. _(Insumo directo para la discusión fundamentos vs. expansión de `08-roadmap`.)_

**No entra:** mejorar la gestión de tareas por sí sola, sin conectar con una decisión de rentabilidad. Coherente con el anti-scope de más abajo: es justo lo que refuerza la confusión con PM genérico.

**Sobre MAIA:** la visión la convierte en **medio, no en fin**. Los insights proactivos y las alertas con plan de mitigación son la forma más directa de comprimir el ciclo señal → decisión; el marketplace de agentes solo cumple la visión en la medida en que termine en una decisión de rentabilidad.

### Tensiones abiertas que la visión destapa

1. **¿Quién decide?** La visión es muda respecto del rol. El que está todos los días en el proyecto es el **PM** — y el PM **no tiene de fábrica acceso a Presupuestos** (`03-personas`), o sea que no ve rentabilidad. El rol mejor posicionado para la decisión diaria es hoy el que no tiene los datos para tomarla, y además es el de peor NPS (−40.7). Bajo esta visión ese permiso deja de ser configuración y pasa a ser **decisión estratégica de producto**.
2. **¿"Diaria" es el ritmo real?** Se mantiene "diaria" por ahora _(decisión del owner, ago-2026)_, asumiendo que es una vara aspiracional. Falta validar contra el ritmo operativo real de un PM de agencia — si en la práctica el ciclo es semanal, la palabra se sostiene como ambición pero no como descripción.
3. **Alcance de "empresas que venden tiempo"** — la visión es agnóstica de vertical y geografía, a propósito: no choca con la expansión a nuevos verticales ni con EMEA (`05`).

### Qué NO es esta frase

No es el **posicionamiento** (eso vive más abajo: "el sistema operativo de rentabilidad para agencias modernas") ni la **ambición de mercado** (eso vive en `05-estrategia-okrs`: $10.2M ARR al cierre de 2027, liderazgo regional). Son tres artefactos distintos y conviene no fundirlos.

## Qué es COR

COR es un software de gestión con IA para agencias y firmas de servicios profesionales, que permite gestionar finanzas, recursos y proyectos en un solo lugar y en tiempo real, y calcular y estimar la rentabilidad de los proyectos. Su foco son los negocios cuyo principal activo es el valor por hora de trabajo.

Posicionamiento actual (en evolución): de plataforma PSA a **el sistema operativo de rentabilidad para agencias modernas** — una plataforma diseñada para exponer la realidad operativa en tiempo real, para que las agencias actúen antes de que la rentabilidad desaparezca. La tesis de fondo: la mayoría del software registra lo que ya pasó; COR busca cambiar lo que pasa mientras el trabajo está en curso.

## Propuesta de valor / problema que resuelve

El dolor central: los márgenes se pierden no por falta de reportes financieros, sino porque las señales operativas llegan tarde. COR ataca eso dando visibilidad en vivo de horas, tareas en riesgo y rentabilidad. Dato de respaldo del propio COR: el 60% de las empresas, antes de usar COR, gestionaban sus proyectos con más de 3 herramientas.

## A quién sirve (ICP)

Los negocios que más se benefician son agencias de marketing y publicidad, consultoras, productoras, desarrolladores de software, estudios de diseño y arquitectura, y firmas legales y contables. El *sweet spot* se inclina hacia agencias de más de 40 personas, donde el desafío real pasa a ser la visibilidad y el control operativo más que tener herramientas.

> _Verificar con el ICP interno real: tamaño, industria y región prioritaria._

## Qué COR NO es (anti-scope)

Delimitar el alcance evita respuestas confundidas. Hay que distinguir dos cosas: **la confusión real del mercado** (una sola, y es la que importa) y los **límites de alcance** del producto (varios, verdaderos pero que casi nunca generan confusión).

### La confusión real: COR ≠ project management genérico

> ✅ _Confirmado con el owner (ago-2026): de todas las categorías adyacentes, **la única con la que se confunde a COR de forma frecuente en ventas, demos y soporte es el project management genérico.**_

- **No es un project management genérico** (tipo Asana, ClickUp, monday, Trello) — aunque incluye gestión de proyectos y tareas, el foco de COR es **la rentabilidad y el control operativo**, no la gestión de trabajo en general. _(`04-mercado` los lista como competidores indirectos, sobre todo en SMB.)_

**Por qué esta distinción importa más que las otras:** es la confusión más cara. Si el prospecto entra pensando "PM tool", compara tableros y tareas contra herramientas gratuitas o mucho más baratas, y COR pierde en un terreno que no es el suyo. El *reframe* correcto es que la gestión de proyectos en COR es **el medio para capturar el dato** (Cliente → Proyecto → Tarea → Hora), y el producto es **la rentabilidad que sale de ese dato**. Un PM genérico no puede responder "¿este cliente me deja plata?".

_Implicancia para producto: una iniciativa que se parece a "mejorar la gestión de tareas" sin conectar con rentabilidad refuerza la confusión en lugar de disolverla._

### Límites de alcance (verdaderos, pero no fuente de confusión)

> _Confirmado con el owner (ago-2026): estas categorías **no** aparecen como confusiones frecuentes en la práctica. Se mantienen como delimitación de alcance, no como objeciones a trabajar en el pitch._

- **No es un ERP ni un software contable** en sí mismo — se integra con QuickBooks y Alegra para eso.
- **No es un CRM** — se integra con HubSpot para la parte comercial.
- **No es una herramienta de diseño/creatividad ni un DAM.**
- **No es solo un time tracker** (tipo Toggl, Harvest, TimeCamp) — el registro de horas es un insumo para el cálculo de rentabilidad, no el producto en sí.
- **No es una herramienta de resource/capacity management standalone** (tipo Float, Runn) — la planificación de recursos vive integrada al ciclo Cliente → Proyecto → Tarea → Hora → Rentabilidad, no como módulo aislado.

_(Tampoco surgen como confusiones frecuentes facturación/billing, RRHH/presentismo ni BI/reporting a medida — chequeado con el owner, ago-2026.)_

## Funcionalidades núcleo

### Gestión del tiempo
- **Time tracking automático:** registro de horas vía integración con calendarios (Google, Outlook, Microsoft), identificación de palabras clave, lógica de reuniones y asistentes que sugieren entradas, para reducir carga administrativa y mejorar la precisión del dato.
- **Licencias, vacaciones y carga de horario laboral:** gestión de ausencias, vacaciones y la jornada laboral de cada persona, insumo que alimenta la capacidad y disponibilidad reales.

### Gestión de proyectos y tareas
- **Gestión de proyectos:** planificación, vista Gantt/timeline, reportes de progreso, controles de acceso y permisos.
- **Gestión de tareas y archivos en tareas:** creación, asignación y seguimiento de tareas, con archivos adjuntos dentro de cada tarea.
- **Plantillas de proyectos:** conjunto de tareas preestablecidas que permiten generar proyectos de forma rápida, en base a los servicios estandarizados de la agencia.

### Planificación de recursos y capacidad
- **Planner:** vista para planificar, distribuir y controlar el tiempo de los recursos mediante la alocación de tareas en un rango de tiempo específico. Ofrece una visión centralizada de la disponibilidad de los usuarios, ayudando a evitar la sobre-ocupación y el tiempo ocioso que podría ser facturable.
- **Capacity Planning:** permite asignar el tiempo de un recurso a un proyecto.
- **Gestión de posiciones y rate card:** creación y edición de posiciones/puestos del equipo, con asignación del valor hora de cada uno. Permite controlar las horas trabajadas frente a las vendidas por posición a un cliente, y entender el costo de cada persona.

### Finanzas y rentabilidad
- **Rentabilidad en tiempo real:** márgenes de contribución, desvíos de tiempo y presupuesto, y cálculo de rentabilidad futura en base al backlog de proyectos.
- **Presupuestos:** centraliza en un solo lugar todas las cotizaciones de productos y servicios ofrecidos a los clientes, y permite asociarlas a los proyectos y tareas en curso.

### Colaboración y reporting
- **Acceso a cliente:** portal para que los clientes sigan el avance de sus proyectos, colaboren y aprueben en un entorno organizado y transparente.
- **Dashboards por rol:** tableros de carga de trabajo, precisión de estimaciones y métricas de performance para roles operativos y C-level.

### Integraciones
- **Zapier:** conector sin código a miles de apps. COR expone *triggers* (crear / actualizar / eliminar: Cliente, Proyecto, Tarea, Hora, Factura, Usuario, Producto, Brand) y *actions* para operar esas entidades.
- **Integraciones nativas** (Configuración → Integraciones): Jira (asociación de tableros y tareas), Microsoft Teams, GitHub (asociar PRs a tareas), QuickBooks y COR–AdvertMind.
- **Contable / facturación:** QuickBooks (nativo) y Alegra (vía Zapier) — las facturas generadas en COR se envían para su procesamiento contable.
- **CRM:** HubSpot (vía Zapier) sincroniza clientes y tareas.
- **API:** API HTTP de COR (JSON o XML) para integraciones a medida con otros software, clientes externos o apps móviles.
- **MCP:** herramientas externas (Gmail, Drive, HubSpot) dentro de los flujos de MAIA, más un conector MCP de Claude para operar COR desde Claude.

> _ERPs: no hay conectores nativos a ERPs pesados (ej. SAP, Oracle); esa integración correría vía API o Zapier. Confirmar si aplica algún caso puntual._

## Plataformas y acceso

- **Web** y **mobile** (app). **No** hay extensión de navegador.
- **Time tracking:** se carga desde la web o la app.
- **Integraciones de calendario:** Google Calendar y Microsoft Calendar.

## Glosario y modelo de datos

Entidades núcleo de COR y cómo se relacionan (vocabulario a usar de forma consistente):

- **Cliente:** empresa a la que la agencia le presta servicios. Agrupa proyectos.
- **Brand / Marca:** marca que puede asociarse a un cliente, pero **no es obligatoria**. Los Productos se asocian a una Marca.
- **Proyecto:** unidad de trabajo para un cliente. Agrupa tareas, presupuesto y estimaciones.
- **Tarea:** unidad de trabajo dentro de un proyecto; se asigna a usuarios, acumula horas y admite archivos adjuntos. **Es la única entidad a la que se cargan horas.**
- **Hora (registro de horas):** tiempo que un usuario carga **contra una tarea** (nunca directo a un proyecto). Base del cálculo de rentabilidad.
- **Usuario:** persona del equipo. Tiene una **posición** asignada y pertenece a un equipo o a ninguno.
- **Equipo:** agrupación de usuarios, y nada más — no se asigna a proyectos ni clientes. Un usuario pertenece a un solo equipo o a ninguno.
- **Área:** agrupación de posiciones. Entidad distinta de Equipo (Equipo = grupo de trabajo; Área = clasificación de la posición).
- **Posición:** puesto/rol dentro de un área, con un **valor hora** asociado.
- **Rate card:** valor hora por posición. Distingue **costo interno** (cuánto cuesta la hora de esa posición) de la **tarifa de venta al cliente** (a cuánto se vende).
- **Presupuesto / Cotización:** cotizaciones de productos y servicios ofrecidos al cliente, asociables a proyectos y tareas.
- **Producto:** ítem estandarizado que la agencia ofrece y cotiza. Se asocia a una **Marca**. Un Cliente puede tener Marcas y Productos.
- **Plantilla de proyecto:** conjunto de tareas preestablecidas para generar proyectos rápido.
- **Estimación:** horas/costo estimados que luego se contrastan con lo ejecutado.

**Jerarquías principales:**
- Trabajo: **Cliente → Proyecto → Tarea → Hora** (Marca opcional, colgando de Cliente).
- Catálogo: **Cliente → Marca → Producto** (un Cliente puede tener Marcas y Productos; el Producto se asocia a una Marca).
- Roles: **Área → Posición**, y el **Usuario** tiene una Posición.
- Organización: **Equipo → Usuarios** (independiente de Área/Posición).

## MAIA — la capa de AI de COR

**Posicionamiento:** MAIA es el **sistema operativo de AI de COR** — concentra toda la IA de la agencia en un solo lugar: agentes que ejecutan trabajo real, insights de proyecto en segundos, todo medido, gobernado y conectado a la rentabilidad. Se organiza en tres pilares.

> _Capacidad confirmada (live hoy): MAIA accede a datos de tareas, proyectos y clientes._

### Pilar 1 — Automatización

Automatiza tareas manuales y repetitivas. Hoy funciona **a pedido**: acciones conversacionales — le pedís a MAIA en lenguaje natural que ejecute una tarea.

> ⚠️ **Aún no disponible (marketing, no producto):** los *agentic workflows* automáticos —que se dispararían ante un evento definido y correrían en segundo plano— figuran en la landing pero **todavía no están implementados**. Tratar como roadmap, no como capacidad actual.

Incluye un **Marketplace de agentes** listos para usar (ej. Brief Specialist, Concept Generator, Blog Draft Builder, Project Specialist) y creación de agentes **sin código** por dos vías: un editor manual (nombre, instrucciones de hasta 5.000 caracteres, modelo, base de conocimiento y accesibilidad) o de forma conversacional, donde MAIA hace 4 preguntas y diseña el agente en menos de 2 minutos.

**Multi-modelo y MCP:** es **LLM-agnóstico** — se elige el modelo de mejor rendimiento por tarea (Anthropic Claude, OpenAI GPT, Gemini, DeepSeek, Mistral) y COR mantiene el control sin importar cuál se use. Un conector MCP de Claude permite operar COR desde Claude (crear proyectos, asignar tareas, consultar datos operativos) sin salir de ahí. La conexión de herramientas externas vía MCP (Gmail, Drive, HubSpot) dentro de un flujo automático —ej. crear un proyecto en COR cuando se cierra una venta— depende de los *agentic workflows*, que aún no están disponibles (ver nota arriba).

### Pilar 2 — Rentabilidad en tiempo real

Insights proactivos: cuando MAIA detecta un desvío, no solo emite la alerta sino que propone un plan de mitigación basado en el conocimiento de la industria. Se adapta por rol:

- **PMs:** del brief al proyecto, con tareas, deadlines y recursos asignados.
- **Directores de cuenta:** "Analyze with MAIA" — retrabajos, salud de clientes, rentabilidad real y performance del equipo.
- **Colaboradores:** resumen de mensajes y carga de horas en segundos.

Para dirección expone rentabilidad real por proyecto y cliente, performance operativa del equipo, y análisis de qué agentes y modelos generan más valor y dónde está el ROI de la inversión en AI. **Risk Management** está disponible **en fase beta**: cubre 10 riesgos **a nivel proyecto** y solo se accede desde dentro de un proyecto (las áreas de riesgo abarcan Fechas, Horas, Rentabilidad, Recursos y Retrabajo).

### Pilar 3 — Governance

*Human in the loop*: cada acción crítica —crear agente, crear tareas, asignar usuarios— requiere aprobación explícita antes de ejecutarse. Suma:

- **Accesibilidad por agente** en tres niveles: toda la compañía, clientes específicos, o solo vos.
- **Trazabilidad** completa con historial auditable.
- **Zero Data Retention** con Anthropic y OpenAI: la data no se almacena en sus servidores ni entrena sus modelos.
- **Seguridad enterprise** con certificaciones tipo SOC e ISO.

## Modelo de negocio / posicionamiento de empresa

B2B SaaS. Fundada en 2017 por **Santiago Bibiloni** (CEO), **José Gettas** (COO) y **Gabriel Marín** (CTO) — nació en el barrio de Once, Buenos Aires, y hoy sus fundadores operan también desde Silicon Valley. Presencia en **38 países**, sirviendo a grandes redes de agencias y holdings publicitarios globales — entre sus clientes figuran Havas, Publicis, Omnicom, Dentsu, Ogilvy, DDB, FCB, Globant, LLYC, GUT, MullenLowe Delta y Sancho BBDO.

**Ronda de inversión (jul-2026):** USD **30 millones**, liderados por **FTV Capital**, con participación de **GFC** y **500 Global** (fondos institucionales), **Marcos Galperin** (fundador de Mercado Libre, inversor inicial) y otros 7 fundadores de compañías valuadas en +US$1.000M (incluyendo ex-CEOs/CTOs de Google, Walmart y Yahoo!). Los fondos se destinan a acelerar capacidades de IA y a la expansión hacia nuevos sectores de servicios profesionales (ver `05-estrategia-okrs`, verticales 2026–2027: Law & Accounting, IT Consulting, etc.).

**Secuencia de rondas (confirmado):** esta ronda de USD 30M es **previa** a la Serie A mencionada en versiones anteriores de este documento — es decir, la Serie A todavía está por darse (o es una ronda posterior a esta), no la misma ronda.

> _Fuentes: [Infobae, 28-jul-2026](https://www.infobae.com/economia/2026/07/28/una-startup-argentina-que-nacio-en-once-y-consiguio-el-apoyo-de-galperin-levanto-usd-30-millones/) y [blog oficial de COR](https://live.projectcor.com/es/blog/cor-recibio-una-inversion-de-30-millones-de-ftv-capital)._

**Crecimiento:** 51% de crecimiento interanual en ingresos al cierre de 2025, según el blog oficial — coincide con el KPI núcleo **ARR Annual Growth: 51%** del Business Plan (`05-estrategia-okrs`).

**Packaging:** COR se vende **por licencia**. **MAIA** todavía no tiene modelo de negocio definido — al estar en fase beta tester, a veces se cobra y a veces no.

## Pendientes — input interno

Resueltos: visión (no existe una formalizada), área/rol del owner, plataformas y acceso, packaging, estado de MAIA (agentic workflows no disponibles; Risk Management en beta a nivel proyecto), nombre y relación de la entidad Producto (se asocia a Marca; Cliente puede tener Marcas y Productos), datos de empresa (funding, alcance, fundadores — confirmado con fuentes públicas, jul-2026), secuencia de rondas (la de USD 30M es previa a la Serie A).

Quedan por confirmar:

- [x] **Anti-scope:** confirmado con el owner (ago-2026). La **única confusión frecuente real** es con **project management genérico** (Asana, ClickUp, monday, Trello). El resto (ERP/contable, CRM, diseño/DAM, time tracker, resource management) son límites de alcance verdaderos pero **no** confusiones habituales en ventas/demos/soporte. Tampoco aparecen facturación/billing, RRHH/presentismo ni BI a medida.

- [ ] **Validar la visión de producto con Nicolás Ocampo (VP Product).** Cargada como propuesta el 2026-08-13: _"Que la rentabilidad sea una decisión diaria y no un hallazgo de fin de mes."_ Hasta que se valide, no citarla como visión oficial.

## Derivadas abiertas (no bloquean este archivo)

- El *reframe* "PM tool → rentabilidad" debería tener un lugar explícito en el pitch y en la demo. Confirmar con Marketing/Ventas si hoy está y cómo se dice → cruza con `04-mercado` (competidores indirectos) y con los **patrones de win/loss**, hoy pendientes en ese archivo.
- **Acceso del PM a Presupuestos** (`03-personas`): bajo la visión propuesta, revisar si el permiso de fábrica es una decisión de producto y no de configuración.
- **North Star de producto** (`06-kpi-tree`, pendiente): la visión sugiere medir **latencia entre desvío y decisión**. Derivarlo cuando se trabaje ese archivo.
- **Fundamentos vs. expansión** (`08-roadmap`): la visión da un argumento explícito para tratar performance, mobile y confiabilidad de horas como condición de posibilidad, no como deuda.
