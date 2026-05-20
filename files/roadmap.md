---
title: "Roadmap"
version: "0.1"
date: "2026-05-19"
audience: "equipo interno"
status: "Draft"
---

# Roadmap

Plan de cuatro fases. Cada fase tiene un objetivo claro y un criterio de salida concreto. No avanzamos hasta cumplir el criterio.

---

## Fase 0 — Validación (mes 0–2)

**Objetivo**: convertir la hipótesis en un caso real y aprender la metodología.

**Actividades**:
- Caso 0 con el abogado amigo como design partner. Gratuito o costo simbólico a cambio de poder documentar todo y usarlo como caso de estudio.
- Auditoría completa de sus archivos.
- Diseño de la taxonomía inicial para práctica legal individual.
- Definición de convención de nomenclatura.
- Documentación de cada paso en `playbooks/legal/`.
- 5–10 entrevistas con otros profesionales (abogados y contadores) sobre cómo manejan sus archivos hoy. Notas en `docs/research/entrevistas/`.

**Criterios de salida**:
- Caso 0 entregado y validado por el abogado: él puede consultarle a su IA preguntas sobre sus propios casos y obtener respuestas útiles.
- Playbook de ordenamiento documentado al punto de que otro miembro del equipo puede ejecutarlo solo.
- Pricing tentativo validado contra disposición a pagar real (no hipotética).

**Entregables tangibles**:
- 1 caso piloto funcionando.
- Borrador 1.0 del playbook legal.
- Notas de las entrevistas.

---

## Fase 1 — Servicio de ordenamiento (mes 2–6)

**Objetivo**: convertir la metodología en un servicio repetible y vender los primeros clientes pagos.

**Actividades**:
- Refinar el playbook con cada cliente nuevo.
- Conseguir 3–5 clientes pagos en abogados, 1–2 en contadores.
- Construir herramientas básicas en `tools/` para automatizar lo más repetitivo (OCR masivo, renombrado, detección de duplicados).
- Armar material comercial (one-pager, pitch deck, propuesta tipo) en `sales/`.
- Definir contratos base (NDA + servicio + manejo de datos).

**Criterios de salida**:
- 5+ clientes pagos entregados.
- Tiempo de entrega por cliente reducido al menos 40% respecto al caso 0.
- Al menos 2 testimoniales explícitos y referibles.
- Margen bruto por cliente positivo y medido.

**Entregables tangibles**:
- Servicio empaquetado con SLA y precio fijo (no horas).
- Playbook v1.0 completo y validado.
- Pipeline comercial documentado.

---

## Fase 2 — Biblioteca de fuentes oficiales (mes 5–9)

**Objetivo**: agregar la capa 2 del producto y convertir clientes one-shot en suscripción.

**Actividades**:
- Construir el ingestor de IMPO y BJN (Base de Jurisprudencia Nacional) para abogados.
- Construir el ingestor de normativa de DGI para contadores.
- Definir frecuencia de actualización por fuente y mecanismo de notificación al cliente cuando hay novedades relevantes.
- Diseñar el modelo de suscripción mensual.

**Criterios de salida**:
- Al menos el 50% de los clientes de Fase 1 pasaron a suscripción mensual.
- Sistema de actualización corriendo sin intervención manual.
- Política de control de calidad de las fuentes (¿qué hacemos si IMPO o BJN falla o cambia su formato?).

**Entregables tangibles**:
- Biblioteca legal UY v1.0 (IMPO + BJN).
- Biblioteca tributaria UY v1.0 (DGI).
- Cliente puede preguntar "qué dice la última resolución de DGI sobre X" y obtener respuesta con cita.

---

## Fase 3 — Plantillas y workflows (mes 9–12)

**Objetivo**: capa 3 — productizar lo que más se repite en cada profesión.

**Actividades**:
- Identificar los 5 documentos más repetitivos por vertical.
- Construir plantilla + prompt + workflow para cada uno.
- Probar con clientes existentes antes de venderlo afuera.
- Definir si esta capa se vende como upsell o entra en el plan mensual.

**Criterios de salida**:
- 10+ plantillas validadas por uso real, no diseñadas en abstracto.
- Cada plantilla tiene métrica de ahorro de tiempo demostrable.
- Decisión tomada y documentada sobre el modelo de cobro de esta capa.

---

## Más allá de la Fase 3

Posibles direcciones, sin orden ni prioridad todavía:

- **Nuevas verticales**: escribanos, médicos, arquitectos.
- **Internacionalización**: Argentina, México y Colombia tienen mercados grandes y necesidades similares.
- **API / producto self-service**: en algún momento puede tener sentido que el cliente pueda hacer parte del trabajo solo.
- **Sello de calidad**: certificar estudios "Cimiento Ready" como diferencial para el cliente final del estudio.

Cualquier movimiento más allá de Fase 3 requiere ADR (`docs/decisions/`) antes de empezar a ejecutar.

---

## Lo que NO vamos a hacer (por ahora)

- **No entrenamos modelos propios.** Usamos los mejores modelos disponibles vía API.
- **No competimos con Thomson Reuters en grandes estudios.** Nuestro target está debajo.
- **No vendemos "IA para abogados".** Vendemos infraestructura de datos. La distinción importa para el posicionamiento.
- **No tomamos clientes que quieran tercerizar la responsabilidad profesional en nosotros.** Somos infraestructura; la responsabilidad sigue siendo del profesional.
