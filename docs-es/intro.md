

---
description: >-
  Una visión general de qué es W&B junto con enlaces sobre cómo comenzar
  si eres un usuario nuevo.
slug: /guías
displayed_sidebar: default
---

# ¿Qué es W&B?

Weights & Biases (W&B) es la plataforma para desarrolladores de IA, con herramientas para entrenar modelos, afinar modelos y aprovechar modelos base.

Configura W&B en 5 minutos, luego itera rápidamente en tu pipeline de aprendizaje automático con la confianza de que tus modelos y datos están rastreados y versionados en un sistema de registro confiable.

![](@site/static/images/general/architecture.png)

Este diagrama describe la relación entre los productos W&B.

**[Modelos W&B](/guías/modelos.md)** es un conjunto de herramientas ligeras e interoperables para profesionales de aprendizaje automático que entrenan y afinan modelos.
- [Experimentos](/guías/track/intro.md): Seguimiento de experimentos de aprendizaje automático
- [Registro de Modelos](/guías/registro_de_modelos/intro.md): Gestión centralizada de modelos en producción
- [Lanzamiento](/guías/lanzamiento/intro.md): Escalado y automatización de cargas de trabajo
- [Barridos](/guías/barridos/intro.md): Ajuste de hiperparámetros y optimización de modelos

**[Prompts W&B](/guías/prompts/intro.md)** es para la depuración y monitoreo de LLM, incluido el uso de la API GPT de OpenAI.

**[Plataforma W&B](/guías/plataforma.md)** es un conjunto central de potentes bloques de construcción para rastrear y visualizar datos y modelos, y comunicar resultados.
- [Artefactos](/guías/artefactos/intro.md): Versionamiento de activos y seguimiento de linaje
- [Tablas](/guías/tablas/intro.md): Visualizar y consultar datos tabulares
- [Reportes](/guías/reportes/intro.md): Documentar y colaborar en tus descubrimientos

## ¿Eres un usuario nuevo de W&B?

<iframe width="100%" height="330" src="https://www.youtube.com/embed/tHAFujRhZLA" title="Demostración End-to-End de Weights &amp; Biases" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

Empieza a explorar W&B con estos recursos:

1. [Notebook de Introducción](http://wandb.me/intro): Ejecuta código de muestra rápido para rastrear experimentos en 5 minutos
2. [Inicio rápido](../inicio_rápido.md): Lee una visión general rápida de cómo y dónde agregar W&B a tu código
1. Explora nuestra [guía de Integraciones](./integraciones/intro.md) y nuestra [lista de reproducción en YouTube de Integración Fácil con W&B](https://www.youtube.com/playlist?list=PLD80i8An1OEGDADxOBaH71ZwieZ9nmPGC) para obtener información sobre cómo integrar W&B con tu marco de trabajo de aprendizaje automático preferido.
1. Consulta la [guía de referencia de API](../ref/README.md) para especificaciones técnicas sobre la biblioteca Python de W&B, la interfaz de línea de comandos y las operaciones de Weave.

## ¿Cómo funciona W&B?

Te recomendamos que leas las siguientes secciones en este orden si eres un usuario nuevo de W&B:

1. Aprende sobre [Runs](./runs/intro.md), la unidad básica de cálculo de W&B.
2. Crea y rastrea experimentos de aprendizaje automático con [Experimentos](./track/intro.md).
3. Descubre el bloque de construcción flexible y ligero de W&B para el versionamiento de datasets y modelos con [Artefactos](./artefactos/intro.md).
4. Automatiza la búsqueda de hiperparámetros y explora el espacio de posibles modelos con [Barridos](./barridos/intro.md).
5. Gestiona el ciclo de vida del modelo desde el entrenamiento hasta la producción con [Gestión del Modelo](./registro_de_modelos/intro.md).
6. Visualiza las predicciones a través de las versiones del modelo con nuestra [guía de Visualización de Datos](./tablas/intro.md).
7. Organiza los Runs de W&B, inserta y automatiza visualizaciones, describe tus hallazgos y comparte actualizaciones con colaboradores con [Reportes](./reportes/intro.md).

Este es un texto nuevo.