---
title: "ADR-001: Posicionamiento agnóstico de modelo de IA"
version: "1.0"
date: "2026-05-19"
audience: "equipo interno"
status: "Approved"
---

# ADR-001: Posicionamiento agnóstico de modelo de IA

**Fecha**: 2026-05-19
**Estado**: Aceptada
**Decisores**: equipo fundador

## Contexto

Al definir el posicionamiento del producto, hay una decisión bisagra: ¿Cimiento se acopla a un proveedor de IA específico (OpenAI, Anthropic, Google) o se mantiene agnóstico, dejándole al cliente elegir y poder cambiar el modelo subyacente?

Los competidores directos del mercado argentino (Argus Legal, ArchivosYa, LEXIUS) están todos atados a un proveedor — la mayoría a OpenAI por debajo. Por otro lado, el ritmo de cambio entre modelos es muy alto: lo que es el mejor modelo hoy no necesariamente lo será en seis meses, y el cliente que se ata a un proveedor termina con costo de migración alto.

La decisión define el discurso comercial, la arquitectura técnica y el contrato con el cliente.

## Decisión

**Cimiento se mantiene agnóstico de modelo.** Nuestro producto es la preparación de los archivos del cliente para que cualquier modelo competente pueda consultarlos. Ofrecemos una capa por encima del modelo, no atada a uno.

En la práctica esto significa:
- Los archivos del cliente quedan en formato estándar (texto plano + metadatos + embeddings en un vector store estándar).
- Soportamos como mínimo dos proveedores desde el día 1: Anthropic Claude y OpenAI GPT.
- El cliente puede elegir cuál usar, y cambiar después sin perder su preparación.
- Nuestro material comercial nunca recomienda "el mejor modelo" sin condicionarlo a un caso de uso.

## Alternativas consideradas

### Opción A — Atarse a OpenAI

- Pro: el más conocido y aceptado por los profesionales hoy; menor fricción de venta.
- Contra: dependencia total de su pricing, sus condiciones y su roadmap. Riesgo si cambia su política de privacidad.
- Por qué la descartamos: el ahorro inicial no compensa el riesgo estratégico de quedar atados.

### Opción B — Construir nuestro propio modelo

- Pro: máxima diferenciación, control total.
- Contra: requiere millones de dólares de inversión en compute y datos, no es realista para nuestra etapa.
- Por qué la descartamos: irrelevante para nuestra escala y momento.

### Opción C — Agnóstico (la elegida)

- Pro: mensaje comercial único en el mercado local, resiliencia ante cambios de proveedor, libertad del cliente.
- Contra: complejidad técnica adicional, costo de mantener integraciones con múltiples proveedores, posiblemente mensaje comercial más difícil de explicar al principio.

## Consecuencias

### Positivas

- Mensaje comercial diferenciado: "no te vendemos otra IA, te dejamos listo para usar la que quieras". Eje principal de pitch.
- Resiliencia: si OpenAI sube precios o Anthropic saca un modelo mejor, podemos pivotear sin migrar al cliente.
- Posicionamiento de socio neutral y de largo plazo, no de revendedor de IA.

### Negativas / Trade-offs

- Más complejidad de mantenimiento: hay que probar contra al menos dos proveedores, los prompts difieren entre modelos, hay que mantener compatibilidad de embeddings.
- El cliente puede sentirse abrumado por la decisión de "cuál modelo". Tenemos que tener una recomendación default clara para cada caso de uso.
- Costo extra en testing y QA.

### Lo que esta decisión hace más difícil revertir

Si después de varios meses decidimos "en realidad nos conviene atarnos a un proveedor", podemos hacerlo. El path inverso (de atado a agnóstico) es muchísimo más caro porque implica rearmar arquitectura y discurso.

Por lo tanto, agnóstico es la opción que **preserva opciones futuras**, no las cierra.

## Revisión

Revisar esta decisión:
- Si algún proveedor saca un producto enterprise con condiciones tan favorables que el ahorro económico supere la pérdida de flexibilidad.
- Al cierre de Fase 1, evaluar si el mensaje agnóstico está convirtiendo en ventas o está confundiendo al cliente.

## Referencias

- `docs/vision.md` — el agnosticismo es uno de los tres ejes de diferenciación documentados.
- `docs/research/competidores.md` — análisis que muestra que ningún competidor local se posiciona así.
- DesignRush, *AI Pricing 2026*, sobre el fenómeno de "shadow AI" y costos de proliferación.
