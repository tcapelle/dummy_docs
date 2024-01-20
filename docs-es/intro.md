

---
description: >-
  Una visión general de qué es W&B junto con enlaces sobre cómo comenzar
  si eres un usuario por primera vez.
slug: /guías
displayed_sidebar: default
---

# ¿Qué es W&B?

Weights & Biases (W&B) es la plataforma para desarrolladores de IA, con herramientas para el entrenamiento de modelos, la optimización de modelos y el aprovechamiento de modelos base.

Configura W&B en 5 minutos, luego itera rápidamente en tu pipeline de aprendizaje automático con la confianza de que tus modelos y datos están seguimiento y versionados en un sistema de registro confiable.

![](@site/static/images/general/architecture.png)

Este diagrama describe la relación entre los productos W&B.

**[Modelos W&B](/guías/modelos.md)** es un conjunto de herramientas ligeras e interoperables para profesionales de aprendizaje automático que entrenan y optimizan modelos.
- [Experimentos](/guías/track/intro.md): Seguimiento de experimentos de aprendizaje automático
- [Registro de Modelos](/guías/registro_de_modelos/intro.md): Gestiona los modelos de producción centralmente
- [Lanzamiento](/guías/lanzamiento/intro.md): Escala y automatiza cargas de trabajo
- [Barridos](/guías/barridos/intro.md): Ajuste de hiperparámetros y optimización de modelos

**[Prompts W&B](/guías/prompts/intro.md)** es para la depuración y el monitoreo de LLM, incluyendo el uso de la API de GPT de OpenAI.

**[Plataforma W&B](/guías/plataforma.md)** es un conjunto central de bloques de construcción potentes para el seguimiento y visualización de datos y modelos, y la comunicación de resultados.
- [Artefactos](/guías/artefactos/intro.md): Versiona los activos y realiza seguimiento del linaje
- [Tablas](/guías/tablas/intro.md): Visualiza y consulta datos tabulares
- [Informes](/guías/informes/intro.md): Documenta y colabora en tus descubrimientos

## ¿Eres un usuario nuevo de W&B?

<iframe width="100%" height="330" src="https://www.youtube.com/embed/tHAFujRhZLA" title="Demostración de Weights &amp; Biases End-to-End" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

Empieza a explorar W&B con estos recursos:

1. [Notebook de introducción](http://wandb.me/intro): Ejecuta un código de muestra rápido para seguir experimentos en 5 minutos
2. [Inicio rápido](../inicio_rápido.md): Lee una visión general rápida de cómo y dónde agregar W&B a tu código
3. Explora nuestra [Guía de integraciones](./integraciones/intro.md) y nuestra [Lista de reproducción de integración fácil de W&B en YouTube](https://www.youtube.com/playlist?list=PLD80i8An1OEGDADxOBaH71ZwieZ9nmPGC) para obtener información sobre cómo integrar W&B con tu marco de aprendizaje automático preferido.
4. Consulta la [Guía de referencia de API](../ref/README.md) para obtener especificaciones técnicas sobre la biblioteca Python de W&B, CLI y operaciones de Weave.

## ¿Cómo funciona W&B?

Recomendamos que leas las siguientes secciones en este orden si eres un usuario nuevo de W&B:

1. Aprende sobre [Runs](./runs/intro.md), la unidad básica de cálculo de W&B.
2. Crea y realiza seguimiento de experimentos de aprendizaje automático con [Experimentos](./track/intro.md).
3. Descubre el bloque de construcción flexible y ligero de W&B para el versionamiento de datasets y modelos con [Artefactos](./artefactos/intro.md).
4. Automatiza la búsqueda de hiperparámetros y explora el espacio de posibles modelos con [Barridos](./barridos/intro.md).
5. Gestiona el ciclo de vida del modelo desde el entrenamiento hasta la producción con [Gestión del Modelo](./registro_de_modelos/intro.md).
6. Visualiza las predicciones a través de las versiones de los modelos con nuestra [Guía de visualización de datos](./tablas/intro.md).
7. Organiza los Runs de W&B, incrusta y automatiza visualizaciones, describe tus hallazgos y comparte actualizaciones con colaboradores con [Informes](./informes/intro.md).

Este es un nuevo texto para fines de prueba.