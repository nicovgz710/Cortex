---
title: "Investigación de Mercado"
version: "0.2"
date: "2026-05-19"
audience: "equipo interno"
status: "Draft"
---

# Investigación de Mercado

> Síntesis de la investigación inicial. Foco en Uruguay como mercado primario. Las fuentes están citadas con link al final de cada sección o ítem.

## El mercado de IA aplicada a profesiones jurídicas y contables

### Tamaño y crecimiento

- El mercado global de consultoría en IA estaba valuado en USD 14 mil millones en 2024 y se proyecta a USD 72,8 mil millones para 2030 (CAGR 31,6%). Fuente: Classic Informatics, *Top AI Consulting Companies 2026*.
- En LATAM, el mercado legaltech se estima en USD 1.700 millones (2024) y podría triplicarse en menos de una década. Fuente: IMARC 2024.
- En LATAM, el sector legaltech está creciendo a doble dígito. Fuente: Coderhouse, *IA para abogados en Argentina y LATAM*.

### Adopción en el sector legal

- **82%** de los abogados de firmas líderes ya usa o planea usar IA en los próximos 12 meses. Fuente: Thomson Reuters.
- **86%** de los profesionales legales en América Latina cree que la IA tendrá impacto alto o transformacional en su profesión en los próximos 5 años. Fuente: Thomson Reuters, *Future of Professionals 2025*.
- Pero cuando se les pregunta cuánto cambio esperan en su propio estudio este año, ese número cae a **35%**. Hay brecha entre la expectativa general y la acción concreta.
- **Solo el 22%** de las firmas legales tiene una estrategia de IA visible. De ese 22%, el **71% ya está experimentando retorno de inversión**. Fuente: ídem.

**Lectura para Cimiento**: hay demanda latente alta, ejecución baja, y los que ejecutan ganan. Espacio claro para un servicio que reduzca la barrera de entrada.

### Adopción en el sector contable

- En Uruguay, la facturación electrónica (CFE) es **obligatoria desde enero 2025** para todos los contribuyentes de IVA. Los contadores ya están digitalizados en ese eje, lo cual facilita la entrada.
- La DGI publicó nuevas versiones del formato CFE con validaciones adicionales que entran en vigor en marzo 2026, lo que genera carga administrativa adicional.
- Referencia regional (México): se estima que **80% del tiempo de un contador** se va en validar facturas, verificar sellos y complementos de pago. Trabajo altamente automatizable. Fuente: Magokoro, *IA en Contabilidad y Finanzas México 2026*.

## El mercado uruguayo específico

### Tamaño del mercado profesional

Datos del INE y registros profesionales (circa 2010, probablemente mayores hoy):

| Profesión | Cantidad estimada en ejercicio | Crecimiento en década |
|---|---|---|
| Abogados | ~7.000 | +42% (2001–2010) |
| Contadores | ~7.000+ | +43% (2001–2010) |
| Escribanos | Sin dato preciso, comunidad significativa | — |

Fuente: INE, citado en LARED21.

**Características del mercado uruguayo**:
- Concentración geográfica fuerte en Montevideo.
- Estudios más chicos en promedio que Argentina — nuestro target natural.
- Es frecuente que una firma resuelva aspectos legales, tributarios y contables de forma integrada.
- Economía bimonetaria (UYU/USD) — cobrar en dólares es natural y elimina complejidad cambiaria.

### Fuentes oficiales disponibles en Uruguay

| Fuente | Contenido | Acceso |
|---|---|---|
| **IMPO** (Dirección Nacional de Impresiones y Publicaciones Oficiales) | Toda la normativa nacional desde 1830 hasta hoy | Público, gratuito, sin registro |
| **BJN** (Base de Jurisprudencia Nacional – Poder Judicial) | Jurisprudencia del Poder Judicial | Público, gratuito, sin registro |
| **DGI** (Dirección General Impositiva) | Normativa tributaria, resoluciones, CFE | Público |
| **Diario Oficial** | Publicaciones oficiales | Público |

**Lectura para Cimiento**: las dos fuentes críticas (IMPO y BJN) son de acceso libre y sin necesidad de registro. Esto facilita enormemente la construcción de la Capa 2 del producto.

### Fuentes privadas / incumbentes

| Fuente | Contenido | Modelo |
|---|---|---|
| **CADE** | 150.000+ documentos: jurisprudencia, legislación, doctrina. La base de datos jurídica privada más grande de Uruguay | Suscripción mensual (precio no público) |
| **Thomson Reuters La Ley Uruguay** | 48.000+ docs legislación (desde 1970), 200.000+ jurisprudencia y doctrina (desde 1940) | Suscripción enterprise |

## El cuello de botella: preparación de datos

Esto es lo más importante para validar nuestra hipótesis central:

- **30–50%** del presupuesto total de un proyecto de IA se va en preparación de datos. Fuente: Riseup Labs, *The True Cost of Implementing AI in Business 2026*.
- Otra fuente menciona **15–25%** del presupuesto, todavía la partida más grande después del modelo en sí. Fuente: InformationWeek vía Insightful AI.
- **66% de las empresas encuentran errores y sesgos en sus datasets de entrenamiento**, que toman entre 80 y 160 horas en limpiar para un dataset de 100.000 muestras. Fuente: Coherent Solutions.
- **Frase clave del mercado**: "La mayoría de los pilotos de IA legal fracasan porque la IA no tiene datos limpios, cumplidos y recuperables." Fuente: AWS Marketplace, *RAG Ready Legal Data Foundation Pack*.

**Lectura para Cimiento**: la categoría de servicio existe a nivel enterprise; nosotros la traemos al profesional SME uruguayo.

## Precios de referencia

| Servicio | Rango | Fuente |
|---|---|---|
| Pilot AI project (small) | USD 5.000–50.000 | Riseup Labs 2026 |
| Implementación AI mid-market año 1 | ~USD 80.000 | The Consultancy World |
| Consultor IA SME (UK) | £950–£1.500 / día | UK Government Marketplace |
| RAG Foundation Pack legal (AWS, 4 semanas) | enterprise | AWS Marketplace |
| The Legal Tool (suscripción UY) | USD 20–50 / mes | uruguai-legal.com |

## Tendencias relevantes para el posicionamiento

### 1. Shadow AI y proliferación de herramientas
"A medida que múltiples equipos adoptan herramientas de IA de forma independiente, se termina pagando dos veces por capacidades similares. Este gasto en *shadow AI* puede inflar presupuestos silenciosamente." (DesignRush, 2026).
→ Refuerza nuestra propuesta de "infraestructura agnóstica de modelo".

### 2. Confidencialidad como freno
Los profesionales legales tienen obligaciones de confidencialidad estrictas. Cargar documentos de clientes en herramientas de terceros genera riesgo profesional real.
→ Refuerza nuestra propuesta de "el cliente es dueño de su información".

### 3. Regulación de IA en Uruguay
Uruguay no tiene ley específica de IA (a 2026), pero Agesic (Agencia de Gobierno Electrónico y Sociedad de la Información) está trabajando en un marco regulatorio. Se crearon sandboxes regulatorios y un Observatorio de IA. La ley de protección de datos personales existe pero fue pensada para otra era tecnológica.
→ Hay ventana de tiempo para posicionarse antes de que el marco se endurezca.

### 4. The Legal Tool como validación del mercado
The Legal Tool (ex UruguAI Legal) alcanzó 3.000+ usuarios y tiene convenio con el Colegio de Abogados del Uruguay (CAU). Demuestra que el mercado uruguayo adopta herramientas de IA legal.
→ Confirma que hay demanda real. Pero su modelo es producto cerrado — nuestro espacio es otro.

### 5. Brecha entre grandes y chicos
Las herramientas enterprise (Thomson Reuters La Ley Uruguay, CADE) están pensadas para estudios grandes. Los profesionales independientes y estudios chicos quedan sin opciones adecuadas. Es nuestro target natural.

## Datos sobre confidencialidad y riesgo

- Uruguay tiene ley de protección de datos personales (Ley 18.331), regulada por la URCDP (Unidad Reguladora y de Control de Datos Personales).
- No hay prohibición legal de usar IA, pero los profesionales deben cuidar la confidencialidad de sus clientes.
- Las versiones empresariales de ChatGPT y Claude ofrecen mayores garantías (no entrenamiento con datos del cliente), pero requieren contratos enterprise.

## Organizaciones profesionales clave en Uruguay

| Organización | Sigla | Relevancia |
|---|---|---|
| Colegio de Abogados del Uruguay | CAU | Ya tiene convenio con The Legal Tool. Canal potencial |
| Asociación de Escribanos del Uruguay | AEU | Vertical futura natural |
| Colegio de Contadores, Economistas y Administradores del Uruguay | CCEAU | 6.500+ miembros. Canal para vertical contable |

## Fuentes para profundizar

- Thomson Reuters, *Future of Professionals 2025*.
- McKinsey Global Institute sobre automatización en sector legal (cita: 22% de tareas legales automatizables).
- El Observador — cobertura de The Legal Tool y legaltech Uruguay.
- IMPO — normativa pública uruguaya (impo.com.uy).
- BJN — jurisprudencia pública (bjn.poderjudicial.gub.uy).
- CADE — base de datos jurídica privada (cade.com.uy).

## Lo que falta investigar

Items abiertos para próximas iteraciones de este documento:

- Tamaño exacto actualizado del mercado de abogados independientes y estudios chicos en Uruguay (Montevideo y principales ciudades).
- Mismo análisis para contadores y escribanos.
- Precios actuales de CADE y Thomson Reuters La Ley Uruguay para referencia competitiva.
- Disposición a pagar real, no declarada. Esto se valida con entrevistas de Fase 0.
- Detalle del marco regulatorio de IA que está preparando Agesic — implicancias para nuestro servicio.
