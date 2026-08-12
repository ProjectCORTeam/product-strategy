# 06 — KPI Tree (COR)

> **Última actualización:** 2026-08-10
> **Owner:** Product Manager, área de Producto
> **Contexto para IA:** Árbol de métricas de COR, desde la North Star hasta las métricas operativas y de producto, para definir el éxito de una feature o analizar resultados. Las métricas de **negocio** vienen confirmadas del Business Plan 2026–2027 (`05`); las de **producto** están inferidas y marcadas como hipótesis hasta confirmarlas.

## Cómo leer este árbol

North Star (arriba) → palancas de negocio → métricas operativas → métricas de producto (drivers). Cada nivel debería "explicar" el de arriba.

## North Star

- **De negocio (confirmada):** **ARR** — meta $10.2M para cierre 2027.
- **De producto (pendiente):** todavía no hay una North Star de producto definida. Candidatas sin confirmar: **rentabilidad gestionada activamente** (clientes/proyectos usando COR para actuar sobre el margen) o **heavy users activos** (colaboradores + PMs con uso recurrente).

> _Pendiente: definir eventualmente la North Star de producto (y posiblemente otras métricas cabecera por eje/squad, ver `02-equipos`)._

## Nivel 1 — Métricas de negocio (confirmadas, del Business Plan)

- **ARR** — meta $10.2M (Exit 2027). Hoy ~$5.48M; goal 2026 $6.8M.
- **ARR Annual Growth:** 51%.
- **NRR (Net Revenue Retention):** 115%.
- **GRR (Gross Revenue Retention):** 90%.

## Nivel 2 — Palancas de negocio

### Adquisición (Net New — $2.38M plan 2027)
- New logos por **vertical** y **geografía** (Agencias LatAm/Brasil/EMEA, IT Consulting, Law & Accounting, Brands, Media).
- **Pipeline** por vertical y **conversion rate** por vertical *(desafío explícito del plan)*.
- **Whales** (cuentas grandes de ticket alto) y **ACV / ticket promedio**.

### Retención y expansión (sostiene NRR 115% / GRR 90% — Installed Base $1.02M plan 2027)
- **Churn** (de logos y de revenue) *(riesgo explícito del plan: "blindaje 2027")*.
- **Expansion revenue** (upsell / cross-sell en la base instalada).
- **Health score** de cuenta (uso, retrabajos, rentabilidad del cliente).
- **NPS / CSAT** como *leading indicators* de retención. **Baseline medido (Retently, ago-26):** NPS global **−27.8** (n=808); CSAT de soporte **4.67/5** (n=81). Ver `07-discovery`.

### Monetización
- **ACV**, estructura de **pricing** (por licencia).
- **Monetización de MAIA** — modelo aún no definido (beta).

## Nivel 3 — Métricas de producto (drivers)

> _Mayormente inferidas de `01` y `03`. Las que tienen **baseline** vienen medidas de Retently (`07`); el resto sigue como hipótesis a confirmar._

### 3.a — Satisfacción por rol (medida — baseline ago-2026)

Único bloque con datos reales hoy. Los **heavy users** son los peor rankeados, y ahí es donde la métrica debería moverse:

| Rol | NPS | n |
|---|---:|---:|
| Freelancer | +17.9 | 39 |
| Director | −11.7 | 77 |
| C-level | −11.9 | 42 |
| Colaborador | −29.0 | 390 |
| Cliente | −33.3 | 12 |
| **Project Manager** | **−40.7** | 248 |

- **NPS de heavy users (PM + Colaborador):** **−33.5** — candidata a métrica de seguimiento propia, por ser el 79% del volumen.
- **Delta onboarding → adopción:** hoy **negativo en Colaborador** (−15.2 → −34.5). Un producto sano debería mejorar con el uso; sirve como métrica de "el producto no desgasta".

### 3.b — Calidad de servicio (drivers de los dolores medidos)

> _Sugeridas a partir de los topics negativos dominantes (`07`): performance 95% neg, bugs 100% neg, mobile 96% neg. Confirmar si se trackean hoy._

- **Performance:** tiempos de carga (p50/p95), tasa de errores, disponibilidad/caídas.
- **Calidad:** bugs reportados y reabiertos, tickets por cuenta.
- **Mobile:** crash rate, uso mobile vs. web, satisfacción mobile.
- **Notificaciones:** ratio de notificaciones accionadas vs. ignoradas (señal/ruido).

### 3.c — Adopción y valor

**Engagement (medido — baseline ago-2026, fuente: Amplitude, evento "Any Active Event"):**

| Métrica | Valor | Detalle |
|---|---:|---|
| **DAU** (promedio días hábiles, jul-2026) | **~7.790** | Cae a ~670 en fin de semana — coherente con un producto B2B de uso en días hábiles. |
| **WAU** | **~11.000–11.900**, estable desde feb-2026 | Última semana completa (03-ago-2026): 11.879. |
| **MAU** | **13.048–14.484** | Pico en jul-2026 (14.484); ago-2026 parcial (13.048, mes en curso). |
| **Stickiness DAU/MAU** (jul-2026, DAU promedio días hábiles) | **~54%** | Alto para un producto B2B — indica uso recurrente, no esporádico. |
| **Stickiness WAU/MAU** (jul-2026) | **~79%** | La mayoría de los usuarios mensuales vuelve semana a semana. |

> _Nota: son valores agregados de toda la base ("All Users"), no cortados por rol/heavy user todavía — sería valioso cruzarlos con `03-personas` (Colaborador + PM) para ver si el engagement de los heavy users es distinto al agregado._

**Pendiente de cargar (compartido por el owner, en camino):** cobertura y precisión del time tracking, uso de features clave.

- **Activación / onboarding:** time-to-value, % de cuentas que llegan al "aha" (ej. primer proyecto con horas cargadas). _(hipótesis, sin baseline)_
- **Cobertura y precisión del time tracking:** % de horas esperadas efectivamente cargadas, y a tiempo (dato base de toda la rentabilidad). _Prioritaria: `07` (I-05) reporta horas que no computan o se pierden — riesgo directo sobre la confiabilidad del dato de rentabilidad._ _(pendiente — el owner va a compartir el dato)_
- **Uso de features de valor:** rentabilidad en tiempo real, Planner/capacity, dashboards por rol, portal de cliente. _(hipótesis, sin baseline — pendiente)_
- **Adopción por vertical** (a medida que se abren): activación y uso fuera del core de agencias. _(hipótesis, sin baseline)_

## Métrica de producto para "Deploy de AI en clientes" (medida — baseline ago-2026, fuente: Amplitude)

> _Contexto clave: MAIA está habilitada solo para un segmento de **beta testers** — no más de **115 empresas**, sobre una base de **+300 clientes** de COR (~38% del total). Cualquier % de adopción debe leerse sobre la base elegible (115), no sobre el total de clientes._

**Crecimiento de uso (interacciones mensuales con MAIA — evento AI_CHAT_SEND/SELECT_FAQ/OPEN/SUGGESTED_ANSWER):**

| Mes 2026 | Interacciones totales | Usuarios únicos activos | Interacciones / usuario |
|---|---:|---:|---:|
| Ene | 113 | 22 | 5.1 |
| Feb | 136 | 28 | 4.9 |
| Mar | 318 | 69 | 4.6 |
| Abr | 625 | 104 | 6.0 |
| May | 1.329 | 219 | 6.1 |
| Jun | 1.583 | 325 | 4.9 |
| Jul | 2.463 | 413 | 6.0 |
| Ago (parcial) | 952 | 178 | 5.3 |

- **Usuarios únicos mensuales activos en MAIA creció ~19x** entre enero (22) y julio (413) — fuerte señal de adopción dentro de la base beta.
- El **promedio de interacciones por usuario activo se mantiene estable (~5–6/mes)**: el crecimiento viene de sumar usuarios nuevos, no de que cada usuario use más MAIA.

**Composición del uso (período 13-may a 11-ago-2026):**
- **Por rol:** Project Manager 454 (56%), Director 191, C-Level 105, Colaborador 59. El PM es, por lejos, el rol que más usa MAIA — coherente con el pilar "del brief al proyecto" de `01-producto`.
- **Por segmento:** Enterprise 467 (58%), Mid Market 212, SMB 109, Retail 13 — el uso de MAIA sigue de cerca la concentración de revenue en Enterprise (`03-personas`: ~70% del revenue).

**Profundidad de uso (usuarios que enviaron consultas, may–ago 2026, n=815):**
- **30% de los usuarios (244) usó MAIA una sola vez** en la ventana de 3 meses; 149 la usaron 2 veces, 91 tres veces.
- Solo el **~8% (64 usuarios) es "power user"** (11+ interacciones/mes).
> ⚠️ _Esto es una señal de posible fricción de retención **dentro de** MAIA — mucha prueba inicial, poca continuidad. Vale la pena cruzarlo con `07-discovery` (¿qué esperan de MAIA vs. qué reciben?)._

**Calidad percibida (feedback explícito, ene–ago 2026):** 73 "thumbs up" vs. 7 "thumbs down" (91% positivo) y 19 respuestas copiadas — señal de calidad positiva, aunque el volumen de feedback explícito (99 acciones) es muy bajo frente al volumen de interacciones (miles), así que hay que tomarlo como dirección, no como medición robusta.

**Candidatas a métrica oficial de "Deploy de AI en clientes":** % de cuentas beta con al menos 1 usuario activo mensual (adopción dentro de la base elegible), usuarios únicos activos/mes (ya con baseline y tendencia arriba), y % de power users vs. usuarios de un solo uso (proxy de retención de valor).

## Enlaces entre archivos

- KPIs de negocio y metas → `05-estrategia-okrs`.
- Heavy users y roles → `03-personas`.
- Features que estas métricas miden → `01-producto`.
- Adopción de MAIA (arriba) responde a la prioridad "Deploy de AI en clientes" de `05-estrategia-okrs`.

## Pendientes — input interno

- [x] North Star de negocio. _(ARR, confirmada.)_
- [ ] North Star de producto — todavía sin definir.
- [ ] Qué métricas de producto se trackean hoy y sus **valores actuales / baseline**. _(Ya cargado: NPS por rol y CSAT de soporte de Retently; DAU/WAU/MAU y stickiness de Amplitude. Falta: cobertura de time tracking, uso de features clave — en camino.)_
- [ ] ¿Se trackean hoy las métricas de **calidad de servicio** (performance, crash rate, bugs)? Son los dolores #1 según `07`.
- [ ] Definiciones y fórmulas exactas (cómo calcula COR NRR, GRR, churn, activación).
- [x] Métrica que mide la prioridad **"Deploy de AI en clientes"**. _(Cargado con baseline real de Amplitude: crecimiento de usuarios activos de MAIA, composición por rol/segmento, profundidad de uso y calidad percibida. Ver sección dedicada arriba.)_
- [x] Health score: confirmado que **no existe hoy**. Queda pendiente definirlo (qué lo compondría: uso, retrabajos, rentabilidad del cliente, NPS, etc.).
