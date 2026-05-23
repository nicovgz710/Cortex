---
title: "Modelo de Negocio"
version: "0.1"
date: "2026-05-19"
audience: "equipo interno, futuros socios"
status: "Draft"
---

# Modelo de Negocio

> Este documento captura hipótesis, no certezas. Cada número se valida en Fase 0 y se ajusta en Fase 1.

## Resumen ejecutivo

Cimiento combina **servicio profesional** (setup inicial, alta intensidad de trabajo manual y conocimiento) con **suscripción** (mantenimiento de la biblioteca de fuentes oficiales, soporte, nuevas plantillas). El setup paga el costo de adquirir y onboardear al cliente; la suscripción genera el ingreso recurrente.

```
Cliente nuevo
   │
   ├──► Setup inicial (one-time, alto ticket) ──► cubre adquisición + onboarding
   │
   └──► Suscripción mensual ───────────────────► ingreso recurrente, margen alto
```

## Líneas de ingreso

### 1. Setup inicial

Servicio de auditoría + ordenamiento + ingesta inicial. Se cobra una sola vez.

**Modalidad**: precio fijo por proyecto, no por hora. Definido según volumen de archivos y complejidad de la práctica.

**Rangos tentativos** (a validar):

| Tamaño del cliente | Volumen aprox. | Precio setup |
|---|---|---|
| Profesional individual | < 5.000 archivos | USD 800–1.500 |
| Estudio chico (2–5 personas) | 5.000–20.000 archivos | USD 1.500–4.000 |
| Estudio mediano (6–20 personas) | 20.000–100.000 archivos | USD 4.000–10.000 |

**Razonamiento**: la consultoría de IA para SMEs en mercados maduros se cobra entre USD 950 y USD 1.500 por día. Un setup razonable son 3–10 días de trabajo. Uruguay tiene economía bimonetaria (UYU/USD), cobrar en dólares es natural y el rango se sostiene.

### 2. Suscripción mensual

Mantenimiento de la biblioteca de fuentes oficiales, soporte para consultas, actualización de plantillas, ingesta incremental de nuevos archivos del cliente.

**Rangos tentativos**:

| Plan | Incluye | Precio mensual |
|---|---|---|
| **Esencial** | Biblioteca de fuentes actualizada, soporte por mail | USD 80–150 |
| **Profesional** | + Ingesta incremental + plantillas | USD 200–350 |
| **Estudio** | + Multi-usuario + soporte prioritario + workflows custom | USD 400–800 |

**Referencia de mercado**: The Legal Tool en Uruguay cobra USD 20–50/mes. CADE cobra suscripción mensual (precio no público). Nuestro plan incluye más valor (preparación de archivos propios + fuentes oficiales + soporte), lo que justifica un precio superior.

### 3. Servicios adicionales (proyecto a proyecto)

- **Plantillas custom**: workflow específico que el cliente necesita y no está en el catálogo. USD 500–2.000 por plantilla.
- **Capacitación al equipo del cliente**: cómo hacerle las preguntas correctas a la IA. USD 300–600 por sesión.
- **Auditoría de prácticas de IA**: revisión de cómo está usando IA y qué riesgos corre. USD 1.000–3.000.

## Estructura de costos

### Costos por cliente (variable)

- **Horas de trabajo del equipo** en el setup. Es la partida más grande inicialmente; se reduce a medida que el playbook madura y se automatiza.
- **APIs de IA y embeddings** para procesamiento e indexado. Probablemente USD 20–100 por cliente según volumen.
- **Almacenamiento** (si lo hosteamos nosotros — preferentemente que viva en infraestructura del cliente).

### Costos fijos

- **Salarios del equipo fundador** (en Fase 0 y 1, probablemente cero o mínimos).
- **Infraestructura compartida** (vector DB, scrapers de IMPO/BJN/DGI). USD 100–300 al mes hasta cierta escala.
- **Herramientas internas** (Notion/Linear, GitHub, dominio, mail). USD 50–100 al mes.

### Hipótesis de margen

Setup: **margen bruto 60–75%** (mucho trabajo manual al principio, se mejora con tooling).
Suscripción: **margen bruto 80–90%** (una vez automatizada la actualización de fuentes, el costo marginal por cliente extra es muy bajo).

## Métricas que vamos a trackear

Desde el primer cliente:

- **CAC** (costo de adquisición de cliente). Empieza alto, debe bajar.
- **LTV** (valor total del cliente, suma de setup + suscripción acumulada).
- **Tiempo de entrega del setup**. Debe bajar 30–50% entre cliente 1 y cliente 5.
- **% de clientes de setup que pasan a suscripción**. Hipótesis: 60%+.
- **Churn mensual de suscriptores**. Hipótesis: < 5% mensual una vez estable.
- **Margen bruto por línea de ingreso**.

## Modelo de adquisición de clientes

**Fase 0**: red personal directa. El amigo abogado nos presenta a colegas. Cero costo de adquisición, validación cualitativa.

**Fase 1**: contenido + boca a boca. Casos de estudio publicados (con permiso), presencia en LinkedIn, charlas en el CAU (Colegio de Abogados del Uruguay), CCEAU (Colegio de Contadores) y AEU (Asociación de Escribanos).

**Fase 2**: paid + partnerships. Cuando haya unit economics validados, considerar inversión en adquisición. Partnerships con colegios profesionales como canal preferente.

## Decisiones pendientes (van a ADR cuando se tomen)

- ¿Cobramos en pesos uruguayos o en dólares? (probablemente USD — economía bimonetaria, natural para servicios profesionales).
- ¿Ofrecemos plan freemium o solo paid? (probablemente solo paid, pero con consulta inicial gratuita).
- ¿Modelo de revenue share con quien nos refiera clientes?
- ¿Expansión regional (Argentina, Chile) desde qué fase?

## Lo que este modelo NO contempla todavía

- Equity / repartición entre socios fundadores. Documento separado cuando los socios estén formalmente incorporados.
- Estructura legal (unipersonal, SAS, otra). Recomendable consultar con contador en Fase 1.
- Estrategia de salida o financiamiento externo. No relevante en este horizonte.
