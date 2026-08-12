# 08 — Roadmap (COR)

> **Última actualización:** 2026-08-10
> **Owner:** Product Manager, área de Producto
> **Contexto para IA:** Qué construye COR, por qué y cuándo, para evaluar prioridades y explicar la dirección. El **roadmap real** aún no está cargado; los temas de abajo están **derivados de la estrategia** (`05`) y marcados como candidatos a validar, no como el roadmap oficial. No inventar fechas ni compromisos.

## Cómo leer este roadmap

Cada ítem debería tener: **qué** (la iniciativa), **por qué** (la prioridad/OKR que sirve), **cuándo** (horizonte) y **métrica de éxito** (`06-kpi-tree`). Horizontes: **Now / Next / Later** (o por trimestre).

## Tensión a resolver: plan de negocio vs. evidencia de clientes

> _Insumo para la discusión de priorización, no una decisión tomada._

El **Business Plan** (`05`) empuja hacia **expansión** (nuevos verticales, EMEA, deploy de AI). La **evidencia de clientes** (`07`, Retently ago-26) muestra una **base con problemas de fundamentos**: NPS global −27.8, heavy users en −33.5 (PM −40.7), performance 95% de menciones negativas, bugs 100%, mobile 96%.

Las dos cosas chocan en un punto concreto: el plan depende de **NRR 115% y GRR 90%** (el +$1.02M de installed base), y la retención se apoya en una base de usuarios hoy insatisfecha. Expandir a nuevos verticales con un producto que los heavy users del core califican mal traslada el problema a mercados nuevos.

**Pregunta a resolver con el Head de Producto:** ¿cuánta capacidad va a *fundamentos* (performance, UX, mobile, confiabilidad de horas) vs. a *expansión* (verticales, AI)? Hoy el plan no lo explicita. _(Confirmado con el owner: esta conversación todavía no se dio — sigue pendiente.)_

## Temas candidatos (derivados de la estrategia y de la evidencia — validar contra el roadmap real)

> _Inferidos de `05-estrategia-okrs` y `07-discovery`. Son hipótesis de hacia dónde *debería* apuntar producto, NO el roadmap comprometido._

0. **Fundamentos: performance, calidad y mobile** ⬅️ _nuevo, con evidencia_
   - *Qué:* velocidad y estabilidad de la plataforma, reducción de bugs, experiencia mobile, señal/ruido de notificaciones.
   - *Por qué:* son los dolores #1 medidos (`07`: performance 95% neg, bugs 100% neg, mobile 96% neg) y **erosionan la promesa de "tiempo real"** que sostiene el posicionamiento. Impacta directo en NRR/GRR.
   - *Métrica de éxito:* NPS de heavy users (−33.5 → meta), p95 de carga, crash rate mobile.

1. **Madurez de MAIA**
   - *Qué:* llevar los *agentic workflows* de roadmap a producto; Risk Management de **beta** a GA (y más allá del nivel proyecto); definir el **modelo de negocio de MAIA**.
   - *Por qué:* prioridad "Deploy de AI en clientes" + monetización pendiente.

2. **Product Adjustments para verticales nuevos**
   - *Qué:* adaptar el producto *agency-first* a IT Consulting, Law & Accounting, Brands y Media.
   - *Por qué:* apertura de verticales y el desafío explícito de acelerar la conversión en cada uno.

3. **Valor en la base instalada (Deploy de AI)**
   - *Qué:* features que suban adopción y valor entregado en clientes existentes.
   - *Por qué:* sostener/superar **NRR 115%** y blindar el churn 2027.

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
- [ ] Métrica de éxito por iniciativa.
- [ ] "Product Adjustments" concretos por vertical.
- [ ] Estado de MAIA en el roadmap (agentic workflows, Risk Management GA, monetización).
- [ ] Principios de priorización del roadmap.
