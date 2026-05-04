# Camino · PM Tracker

> Un agente de IA que revisa tu board de Trello cada mañana y te envía un briefing de roadmap por email — sin que tengas que abrir Trello.

**🌐 Landing page:** [miasanchezro.github.io/oc-agent-camino](https://miasanchezro.github.io/oc-agent-camino)

---

## ¿Qué es esto?

Camino es un agente personal construido con [OpenClaw](https://openclaw.ai) como parte de un reto de 7 días de aprendizaje. El objetivo: construir algo útil para el rol de Product Owner sin ser developer.

El problema que resuelve: cada mañana un PO pierde entre 15 y 30 minutos reconstruyendo manualmente el estado del sprint en Trello. Camino automatiza eso y lo entrega directo al email.

---

## Misión del agente

> Revisar las cards del board de roadmap activo cada mañana y enviar un resumen de avance por email para que el PO pueda arrancar el día con claridad total sobre el estado del sprint **sin abrir Trello**.

---

## Capacidades (v1)

| # | Capacidad | Detalle |
|---|-----------|---------|
| 1 | **Lee el board activo** | Conecta con la Trello API y descarga todas las cards — listas, fechas, asignados y etiquetas |
| 2 | **Detecta lo crítico** | Identifica cards vencidas, sin actividad reciente o bloqueadas |
| 3 | **Envía el briefing** | Redacta un resumen tipo standup en lenguaje natural y lo envía por email |

---

## Stack técnico

- **[OpenClaw](https://openclaw.ai)** — motor del agente
- **[Trello API](https://developer.atlassian.com/cloud/trello/)** — fuente de datos
- **Email SMTP** — canal de salida (Gmail)
- **[GitHub Pages](https://pages.github.com)** — deploy de la landing (gratuito)

---

## Reglas del agente

**Nunca hace:**
- Incluir cards de otros boards que no sean el roadmap activo
- Enviar resumen si no hay nada relevante que reportar
- Comentar ni modificar cards en Trello por su cuenta

---

## Plan de ejecución · 7 días

```
Día 1 → Setup de OpenClaw + primera conexión a Trello
Día 2 → Construcción del Skill de Trello (get_cards, filter_overdue, get_blocked)
Día 3 → Lógica de detección de alertas
Día 4 → Integración del LLM para redacción del briefing
Día 5 → Canal de salida: Email SMTP
Día 6 → Heartbeat diario + ajuste de tono
Día 7 → Prueba end-to-end con board real + retrospectiva
```

---

## Ficha del empleado

| Campo | Valor |
|-------|-------|
| **Nombre** | Camino |
| **Rol** | PM Tracker |
| **Tono** | Directo · orientado a decisión · sin adornos |
| **Canal** | Email SMTP |
| **Frecuencia** | Diaria · mañana (heartbeat) |
| **Funciona si** | Recibo el briefing al menos 5 veces por semana con info correcta y accionable |
| **No funciona si** | El resumen incluye cards irrelevantes o llega sin consistencia horaria |

---

## Estado del proyecto

- [x] Día 1 — Diseño del agente y ficha completa
- [ ] Día 2 — Skill de Trello
- [ ] Día 3 — Lógica de alertas
- [ ] Día 4 — Integración LLM
- [ ] Día 5 — Email SMTP
- [ ] Día 6 — Heartbeat
- [ ] Día 7 — Producción

---

*Construido con OpenClaw · Reto 7 días · Product Owner → AI Agent Builder*
