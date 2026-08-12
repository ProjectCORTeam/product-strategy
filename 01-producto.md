# 01 — Producto (COR)

> **Última actualización:** 2026-08-12
> **Owner:** Product Manager, área de Producto (reporta al Head de Producto)
> **Contexto para IA:** Este archivo describe qué es COR, qué hace y para quién. Es el punto de partida para entender el producto antes de leer cualquier otro archivo.

## Visión de producto

> _Al momento **no existe una visión de producto formalizada**. No inferir ni inventar una; si se necesita, se construye explícitamente._

## Qué es COR

COR es un software de gestión con IA para agencias y firmas de servicios profesionales, que permite gestionar finanzas, recursos y proyectos en un solo lugar y en tiempo real, y calcular y estimar la rentabilidad de los proyectos. Su foco son los negocios cuyo principal activo es el valor por hora de trabajo.

Posicionamiento actual (en evolución): de plataforma PSA a **el sistema operativo de rentabilidad para agencias modernas** — una plataforma diseñada para exponer la realidad operativa en tiempo real, para que las agencias actúen antes de que la rentabilidad desaparezca. La tesis de fondo: la mayoría del software registra lo que ya pasó; COR busca cambiar lo que pasa mientras el trabajo está en curso.

## Propuesta de valor / problema que resuelve

El dolor central: los márgenes se pierden no por falta de reportes financieros, sino porque las señales operativas llegan tarde. COR ataca eso dando visibilidad en vivo de horas, tareas en riesgo y rentabilidad. Dato de respaldo del propio COR: el 60% de las empresas, antes de usar COR, gestionaban sus proyectos con más de 3 herramientas.

## A quién sirve (ICP)

Los negocios que más se benefician son agencias de marketing y publicidad, consultoras, productoras, desarrolladores de software, estudios de diseño y arquitectura, y firmas legales y contables. El *sweet spot* se inclina hacia agencias de más de 40 personas, donde el desafío real pasa a ser la visibilidad y el control operativo más que tener herramientas.

> _Verificar con el ICP interno real: tamaño, industria y región prioritaria._

## Qué COR NO es (anti-scope)

Delimitar el alcance evita respuestas confundidas:

- **No es un ERP ni un software contable** en sí mismo — se integra con QuickBooks y Alegra para eso.
- **No es un CRM** — se integra con HubSpot para la parte comercial.
- **No es una herramienta de diseño/creatividad ni un DAM.**
- **No es un project management genérico** (tipo Asana, ClickUp, monday, Trello) — aunque incluye gestión de proyectos y tareas, el foco de COR es la rentabilidad y el control operativo, no la gestión de trabajo en general. _(`04-mercado` los lista como competidores indirectos, sobre todo en SMB.)_
- **No es solo un time tracker** (tipo Toggl, Harvest, TimeCamp) — el registro de horas es un insumo para el cálculo de rentabilidad, no el producto en sí.
- **No es una herramienta de resource/capacity management standalone** (tipo Float, Runn) — la planificación de recursos vive integrada al ciclo Cliente → Proyecto → Tarea → Hora → Rentabilidad, no como módulo aislado.

> ⚠️ _Propuesta armada por inferencia cruzando `04-mercado` (categorías de competidores adyacentes/indirectos), no confirmada aún con el equipo. Confirmar si estas son efectivamente las confusiones más frecuentes en ventas/soporte/demos, o si hay otras más relevantes en la práctica._

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

- [ ] **Anti-scope:** propuesta cargada (project management genérico, time tracker, resource management) — confirmar si son las confusiones reales en ventas/soporte/demos, según lo hablado con el equipo.
