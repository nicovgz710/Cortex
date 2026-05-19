---
title: "Visión de Cimiento"
version: "0.1"
date: "2026-05-19"
audience: "equipo interno, futuros socios, inversores"
status: "Draft"
---

# Visión

## El problema

Los profesionales — abogados, contadores, escribanos, médicos — quieren usar inteligencia artificial para trabajar mejor. Pero la IA, en su uso real, no es mágica: necesita acceder a información ordenada. Hoy esos profesionales tienen:

- Archivos guardados en carpetas inconsistentes ("Documentos", "Escritorio", "Mis cosas", "Casos nuevos 2", "Casos nuevos 2 - final").
- Nombres de archivo sin convención: `escrito final.docx`, `escrito final ESTE.docx`, `escrito_final_REAL.docx`.
- Información duplicada en Drive, Dropbox, mail y la PC local.
- Documentos escaneados sin OCR (la IA no puede leer una imagen de un PDF).
- Datos públicos (constitución, leyes, jurisprudencia, resoluciones generales) sin integrar a su flujo.

Resultado: cuando el profesional le pregunta algo a ChatGPT o Claude sobre **sus propios casos**, no puede. La IA solo sabe lo que sabe el modelo, no lo que sabe el estudio. La promesa de la IA aplicada al trabajo profesional se cae acá.

## Por qué es un problema real

- **30–50% del presupuesto típico de un proyecto de IA se va en preparar los datos**, según múltiples consultoras. No es un detalle, es el cuello de botella.
- **23% de las horas facturables de un abogado** se van en revisión de documentos e investigación. Es exactamente lo que un buen sistema de IA con archivos bien preparados acelera.
- En LATAM, **86% de los profesionales legales cree que la IA tendrá impacto alto o transformacional** en su profesión en los próximos 5 años. Pero **solo el 22% de las firmas legales tiene una estrategia de IA visible**. Hay demanda latente y ninguna infraestructura para canalizarla.

## La solución

Cimiento toma los archivos del cliente y los deja en un estado en que cualquier IA puede consultarlos de forma confiable. Tres capas, en orden de complejidad creciente:

### Capa 1 — Servicio de ordenamiento

Auditamos los archivos del cliente, definimos una taxonomía adecuada a su práctica, renombramos según convención semántica, hacemos OCR de los escaneados, eliminamos duplicados y construimos la estructura de carpetas. Le entregamos un "antes y después" tangible. Consultoría pura.

### Capa 2 — Biblioteca de fuentes oficiales

Integramos al sistema del cliente las fuentes públicas que necesita para su práctica:
- **Abogados argentinos**: Constitución Nacional, Código Civil y Comercial, jurisprudencia de SAIJ y CSJN, Boletín Oficial.
- **Contadores**: normativa de AFIP/ARCA, resoluciones generales vigentes, CFDI/factura electrónica.

Mantenemos esas fuentes actualizadas automáticamente. El cliente puede preguntarle a su IA "qué dice la última RG sobre X" sin tener que ir a buscarla.

### Capa 3 — Plantillas y workflows

Construimos plantillas inteligentes para los documentos repetitivos de cada profesión (contratos, escritos tipo, dictámenes). El profesional rellena lo específico; la IA arma el resto usando como contexto las dos capas anteriores.

## Audiencia

**Primario**: profesionales independientes y estudios chicos a medianos (2–20 personas) en Argentina, en estas verticales por orden de prioridad:

1. **Abogados** — sector con mayor presión competitiva por IA, ROI más medible.
2. **Contadores** — alta densidad de documentos repetitivos (facturas, balances).
3. **Escribanos** — siguiente vertical natural por similitud de flujos.

**No primario por ahora**: grandes estudios (ya tienen Thomson Reuters), corporativos (compran enterprise), y profesionales totalmente analógicos (no son target todavía).

## Diferenciación

Hay competencia activa en el espacio (ver `research/competidores.md`). Cimiento se diferencia en tres ejes:

1. **Agnóstico de modelo**. La mayoría de los competidores te venden su plataforma con su IA cerrada. Nosotros preparamos los archivos del cliente para que funcionen con cualquier IA — ChatGPT, Claude, Gemini, o lo que venga. El cliente no queda atado a un proveedor.

2. **El profesional dueño de su información**. Los archivos viven donde el cliente quiere (su nube, su servidor, su PC). No los subimos a una plataforma propietaria. Esto es crítico por confidencialidad profesional.

3. **Metodología, no software**. Nuestro principal activo es el método: cómo se diagnostica, cómo se taxonomiza, cómo se valida. Eso es replicable a otras profesiones y resistente al cambio tecnológico.

## Principios

- **El cliente es dueño de su información, siempre.** Ningún archivo del cliente vive en infraestructura nuestra sin un contrato explícito.
- **Cero promesas mágicas.** La IA alucina. Lo decimos en la primera reunión y diseñamos los flujos para minimizarlo.
- **Medible o no se hace.** Cada entrega tiene métricas concretas: cantidad de archivos procesados, tiempo ahorrado estimado, calidad de respuesta antes/después.
- **Documentar es construir el producto.** Lo que aprendemos con un cliente queda en `playbooks/` y mejora la entrega al siguiente.

## Por qué ahora

- Los modelos llegaron a un nivel de calidad donde el cuello de botella ya no es el modelo, es la información que le das.
- La adopción profesional pasa de "curiosidad" a "necesidad competitiva": el abogado que no usa IA pierde frente al que sí.
- En Argentina, Thomson Reuters acaba de lanzar CoCounsel localizado, lo que marca que el mercado profesional está listo, pero también que las opciones cerradas top-of-market van a costar caro. Hueco abierto para una alternativa más accesible y más flexible.

## Por qué nosotros

- Somos programadores. Nuestro trabajo diario consiste en tener archivos ordenados; sabemos qué significa que la información esté en estado consultable.
- Tenemos acceso directo a un abogado como design partner (caso 0).
- No necesitamos entrenar modelos ni levantar millones: el negocio se sostiene desde el primer cliente.
