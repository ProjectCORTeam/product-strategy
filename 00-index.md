# 00 — Índice del Contexto de Producto (COR)

> **Última actualización:** 2026-08-17
> **Owner:** Product Manager, área de Producto
> **Contexto para IA:** Este archivo es el mapa del "Product Brain" de COR. Leélo siempre primero para entender qué archivos de contexto existen y cuándo usar cada uno. No hace falta cargar todos: identificá los relevantes para la pregunta y leé solo esos.

---

## Cómo usar este contexto

1. Leé **este índice primero** para saber qué hay disponible y cuándo aplica cada archivo.
2. Identificá qué archivos son relevantes para la pregunta puntual — no cargues los 9 de una si no hace falta.
3. Respondé **basándote solo en lo que está en los archivos**. Si algo no está, decilo explícitamente. No inventes contexto de COR.
4. Si detectás información **contradictoria entre archivos**, señalalo en vez de elegir en silencio.
5. **La sección de AI de `06-kpi-tree` usa etiquetas de evidencia** — `[HECHO]`, `[HALLAZGO]`, `[HIPÓTESIS]` y `[BAJA]`, definidas dentro de esa sección. **Respetá la etiqueta al citar:** un `[HALLAZGO]` se cita con su salvedad, un `[HIPÓTESIS]` no justifica una decisión de capacidad, y un `[BAJA]` es una afirmación **retirada** que no debe volver a circular. Si encontrás una de las afirmaciones dadas de baja repetida en otro archivo o en un deck, señalalo. _(Convención acotada a esa sección por ahora.)_
6. Estos archivos viven como contexto del **Proyecto de Claude "COR – Product Context"**. Al actualizarlos, subí la nueva versión al proyecto.

---

## Mapa de archivos

| Archivo | Qué contiene | Cuándo usarlo |
|---|---|---|
| `00-index.md` | Este mapa | Siempre primero |
| `01-producto.md` | Qué es COR, propuesta de valor, funcionalidades, MAIA | Para entender qué hace el producto |
| `02-equipos.md` | Estructura de squads, roles, responsabilidades | Para saber quién hace qué |
| `03-personas.md` | Segmentos, perfiles de usuario, comportamientos | Al diseñar features o evaluar impacto |
| `04-mercado.md` | Competidores, posicionamiento, oportunidades y amenazas | Al evaluar oportunidades o riesgos de mercado |
| `05-estrategia-okrs.md` | Visión, pilares estratégicos, OKRs del trimestre | Al priorizar o alinear iniciativas |
| `06-kpi-tree.md` | Árbol de métricas: de north star a métricas operativas | Al definir éxito de una feature o analizar resultados |
| `07-discovery.md` | Insights curados de entrevistas, encuestas y datos | Al buscar evidencia para una decisión |
| `08-roadmap.md` | Qué construimos, por qué y cuándo | Al evaluar prioridades o explicar la dirección |

---

## Estado de completitud

_(Marcá el avance a medida que vamos armando cada archivo. "Base" = estructura y contenido cargado; quedan pendientes internos marcados dentro de cada archivo.)_

- [x] `01-producto.md` — casi completo (pendiente: validar la visión con Nicolás Ocampo). **Actualizado 2026-08-17:** capacidades reales de MAIA al día, elección de modelo como palanca de producto, y el revenue real de MAIA (solo consultoría, 3 clientes).
- [x] `02-equipos.md` — **completo**. Organigrama interno confirmó C-level real (CEO/COO/CTO, sin CFO visible — a confirmar), VP Product (Nicolás Ocampo), y todas las áreas fuera de Producto (Marketing, Sales & Revenue, Client Services, Client Support, Administration & People, Cloud Solutions).
- [x] `03-personas.md` — casi completo, cortes de segmento confirmados (pendiente: rollout/qué rol ejerce de champion, personas por vertical nuevo). **Actualizado 2026-08-17:** adopción de MAIA por rol corregida (los tres roles adoptan igual; el C-level es el más intensivo) + propuesta de valor de MAIA para el Colaborador como pendiente nuevo.
- [x] `04-mercado.md` — competidores reales confirmados, LATAM hispano confirmado sin jugadores locales (pendiente: vertical nuevo, precio, BV, cruce con churn de HubSpot — a compartir).
- [x] `05-estrategia-okrs.md` — marco de priorización + Industry Leads confirmados. **Actualizado 2026-08-17:** cargado el laddering de "Deploy de AI en clientes" con baseline, **cuatro anti-metas** para los KRs y el estado real del modelo de negocio de MAIA (pendiente: OKRs de producto por eje, laddering de las otras dos prioridades, métrica de la vertical de AI fuera de MAIA).
- [x] `06-kpi-tree.md` — North Star de negocio y engagement (DAU/WAU/MAU) con baseline real. **Sección de AI reescrita el 2026-08-17:** la métrica pasó de conteos absolutos a **penetración sobre asientos elegibles** (baseline jul-26 **11,6%**, provisorio), con definiciones, **etiquetado de evidencia** y **dos afirmaciones dadas de baja** ("MAIA es una herramienta de PM" y "91% de calidad percibida"). Pendiente: North Star de producto, calidad de servicio, fórmulas exactas, health score, y 10 pedidos de datos de AI (dos bloqueantes).
- [x] `07-discovery.md` — repositorio estructurado, gaps de proceso identificados (pendiente: corte por segmento/vertical, research cualitativo existente a ubicar, curar el discovery semanal hacia acá, priorizar tema abierto). **Actualizado 2026-08-17:** tres targets de research de MAIA bien definidos (cuentas dormidas, Crowe Global, meseta del C-level).
- [x] `08-roadmap.md` — estructura + temas candidatos; el roadmap real sigue vacío. **Actualizado 2026-08-17:** cargado el **segundo eje de reparto dentro de AI** (capacidad vs. superficie, como hipótesis con test) y un tema candidato nuevo — **activación de la base ya habilitada de MAIA**, ~+45 usuarios sin construir nada, con verificación de churn como bloqueante. Sigue pendiente el roadmap real y el balance fundamentos/expansión con el Head de Producto.
