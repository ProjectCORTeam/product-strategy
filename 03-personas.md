# 03 — Personas (COR)

> **Última actualización:** 2026-08-12
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

**Patrón central:** cuanto **más intensivo** es el uso del producto, **peor** la satisfacción. Los roles operativos (PM + Colaborador) son el 79% del volumen de feedback y los más críticos; los roles de lectura/agregado están claramente mejor. El dolor vive en la operación diaria, no en el reporting.

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
