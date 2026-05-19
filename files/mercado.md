---
title: "Investigación de Mercado"
version: "0.1"
date: "2026-05-19"
audience: "equipo interno"
status: "Draft"
---

# Investigación de Mercado

> Síntesis de la investigación inicial. Las fuentes están citadas con link al final de cada sección o ítem.

## El mercado de IA aplicada a profesiones jurídicas y contables

### Tamaño y crecimiento

- El mercado global de consultoría en IA estaba valuado en USD 14 mil millones en 2024 y se proyecta a USD 72,8 mil millones para 2030 (CAGR 31,6%). Fuente: Classic Informatics, *Top AI Consulting Companies 2026*.
- En LATAM, el sector legaltech está creciendo a doble dígito. Fuente: Coderhouse, *IA para abogados en Argentina y LATAM*.

### Adopción en el sector legal

- **82%** de los abogados de firmas líderes ya usa o planea usar IA en los próximos 12 meses. Fuente: Thomson Reuters, citado en Coderhouse.
- **86%** de los profesionales legales en América Latina cree que la IA tendrá impacto alto o transformacional en su profesión en los próximos 5 años. Fuente: Thomson Reuters, *Future of Professionals 2025*.
- Pero cuando se les pregunta cuánto cambio esperan en su propio estudio este año, ese número cae a **35%**. Hay brecha entre la expectativa general y la acción concreta.
- **Solo el 22%** de las firmas legales tiene una estrategia de IA visible. De ese 22%, el **71% ya está experimentando retorno de inversión**. Fuente: ídem.

**Lectura para Cimiento**: hay demanda latente alta, ejecución baja, y los que ejecutan ganan. Espacio claro para un servicio que reduzca la barrera de entrada.

### Adopción en el sector contable

- En México (referencia regional), se estima que **80% del tiempo de un contador** se va en validar facturas CFDI, verificar RFC, sellos digitales y complementos de pago. Trabajo altamente automatizable. Fuente: Magokoro, *IA en Contabilidad y Finanzas México 2026*.
- Hay caso documentado de una cadena de restaurantes en Guadalajara que pasó de un cierre contable mensual de 12 días a 3 días con IA aplicada. Mismo principio que en legal: la traba no es el modelo, es la organización de los datos de entrada.

## El cuello de botella: preparación de datos

Esto es lo más importante para validar nuestra hipótesis central:

- **30–50%** del presupuesto total de un proyecto de IA se va en preparación de datos. Fuente: Riseup Labs, *The True Cost of Implementing AI in Business 2026*.
- Otra fuente menciona **15–25%** del presupuesto, todavía la partida más grande después del modelo en sí. Fuente: InformationWeek vía Insightful AI.
- **66% de las empresas encuentran errores y sesgos en sus datasets de entrenamiento**, que toman entre 80 y 160 horas en limpiar para un dataset de 100.000 muestras. Fuente: Coherent Solutions.
- **Frase clave del mercado**: "La mayoría de los pilotos de IA legal fracasan porque la IA no tiene datos limpios, cumplidos y recuperables." Fuente: AWS Marketplace, *RAG Ready Legal Data Foundation Pack*.

**Lectura para Cimiento**: la categoría de servicio existe a nivel enterprise; nosotros la traemos al SME profesional.

## Precios de referencia

| Servicio | Rango | Fuente |
|---|---|---|
| Pilot AI project (small) | USD 5.000–50.000 | Riseup Labs 2026 |
| Implementación AI mid-market año 1 | ~USD 80.000 | The Consultancy World |
| Consultor IA SME (UK) | £950–£1.500 / día | UK Government Marketplace |
| RAG Foundation Pack legal (AWS, 4 semanas) | enterprise | AWS Marketplace |
| Argus Legal (suscripción AR) | ARS 149.000 / mes (~USD 130) | arguslegal.ai |

## Tendencias relevantes para el posicionamiento

### 1. Shadow AI y proliferación de herramientas
"A medida que múltiples equipos adoptan herramientas de IA de forma independiente, se termina pagando dos veces por capacidades similares. Este gasto en *shadow AI* puede inflar presupuestos silenciosamente." (DesignRush, 2026).
→ Refuerza nuestra propuesta de "infraestructura agnóstica de modelo".

### 2. Confidencialidad como freno
Los Colegios de Abogados en Argentina recomiendan no comprometer la confidencialidad del cliente al usar herramientas de IA de terceros. Fuente: Coderhouse.
→ Refuerza nuestra propuesta de "el cliente es dueño de su información".

### 3. Casos reales de alucinaciones con consecuencias
La Cámara de Apelación en lo Civil y Comercial de Rosario advirtió formalmente sobre el uso de IA en escritos tras detectar citas jurisprudenciales inventadas. Fuente: iProUP.
→ Refuerza la necesidad de un sistema que cite fuentes verificables.

### 4. Localización del producto enterprise
Thomson Reuters lanzó CoCounsel Core en Argentina en español. Es el primer país en recibir el producto en español. Fuente: AUNO Abogados.
→ Confirma que el mercado argentino está siendo tomado en serio por los grandes. Hay tiempo limitado para construir posición local.

### 5. Brecha entre grandes y chicos
Las herramientas enterprise (Harvey, CoCounsel, Argus Legal) están agarrando los estudios grandes. Los profesionales independientes y estudios chicos quedan sin opciones adecuadas. Es nuestro target natural.

## Datos sobre confidencialidad y riesgo

- En Argentina no hay prohibición legal de usar IA, pero los Colegios de Abogados recomiendan revisar términos de servicio antes de cargar documentos sensibles.
- Las versiones empresariales de ChatGPT y Claude ofrecen mayores garantías (no entrenamiento con datos del cliente), pero requieren contratos enterprise.
- Hay riesgo reputacional y profesional concreto para el abogado que use IA mal: el caso Rosario sentó precedente.

## Fuentes para profundizar

- Thomson Reuters, *Future of Professionals 2025*.
- McKinsey Global Institute sobre automatización en sector legal (cita: 22% de tareas legales automatizables).
- AUNO Abogados — coverage local del lanzamiento de CoCounsel.
- iProUP — cobertura legaltech LATAM.
- Coderhouse — guía amplia de IA para abogados en LATAM.

## Lo que falta investigar

Items abiertos para próximas iteraciones de este documento:

- Tamaño exacto del mercado de abogados independientes y estudios chicos en Argentina (CABA, GBA, principales ciudades).
- Mismo análisis para contadores y escribanos.
- Análisis comparativo de la regulación de IA en jurisdicciones argentinas relevantes.
- Disposición a pagar real, no declarada. Esto se valida con entrevistas de Fase 0.
