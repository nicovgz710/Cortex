---
title: "Cimiento"
version: "0.1"
date: "2026-05-19"
status: "Draft"
---

# Cimiento

> Preparamos los archivos de profesionales para que cualquier IA pueda trabajar con ellos de forma ordenada, segura y eficiente.

## ¿Qué es esto?

Cimiento es un servicio (con producto en construcción) que toma los archivos dispersos y desordenados de un profesional — abogado, contador, escribano — y los deja listos para que una IA los consulte de forma confiable. No vendemos otra IA: ordenamos la información del cliente para que funcione con la IA que él elija, hoy y mañana. Mercado inicial: Uruguay.

Este repositorio es la base de conocimiento del proyecto. Acá vive la visión, el roadmap, la investigación de mercado, las decisiones estratégicas, y más adelante también la metodología (playbooks), las plantillas y el código de las herramientas.

## Estructura del repositorio

```
cimiento/
├── README.md              ← Estás acá
└── docs/
    ├── vision.md          ← Norte del proyecto, problema, solución, diferenciación
    ├── roadmap.md         ← Fases del proyecto y hitos
    ├── business-model.md  ← Pricing, modelo de ingresos, márgenes
    ├── research/
    │   ├── mercado.md     ← Datos del mercado y validación de la oportunidad
    │   ├── competidores.md ← Análisis de competencia directa e indirecta
    │   └── entrevistas/   ← Notas de calls con profesionales (template incluido)
    └── decisions/         ← Architecture Decision Records (ADRs)
        ├── _template.md
        └── ADR-001-model-agnostic.md
```

Más adelante se sumarán:
- `playbooks/` — la metodología propia (nuestro principal activo de IP).
- `templates/` — estructuras de carpetas tipo, prompts, contratos modelo.
- `tools/` — código de automatización (OCR, indexado, validación).
- `knowledge-base/` — fuentes oficiales curadas (IMPO, BJN, DGI).
- `sales/` y `brand/` — material comercial y de identidad.

## Cómo navegar la documentación

- **Si entrás por primera vez**: leé `docs/vision.md` y después `docs/roadmap.md`. En 10 minutos tenés el panorama completo.
- **Si vas a hablar con un cliente**: pasá por `docs/research/competidores.md` y `docs/business-model.md`.
- **Si vas a tomar una decisión estratégica**: revisá los ADRs en `docs/decisions/` para no contradecir decisiones previas.

## Estado actual

**Fase 0 — Validación.** Estamos definiendo el alcance, armando el caso piloto con un abogado como design partner, y documentando la metodología que surge del proceso.

## Convenciones

- **Idioma**: español (rioplatense). Tecnicismos en inglés cuando no hay traducción establecida (RAG, prompt, vector store).
- **Formato**: Markdown para todo. Frontmatter YAML al inicio de cada documento.
- **Nombres de archivo**: `kebab-case.md`. Los ADRs llevan numeración: `ADR-NNN-titulo-corto.md`.
- **Datos sensibles**: **nunca** subir archivos de clientes al repo. Para eso, `clients/` está en `.gitignore` desde el día 1.

## Equipo

_A completar cuando el equipo esté formado._

## Licencia

Propietario. Repositorio privado.
