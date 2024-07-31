---
description: Una visión general de qué es W&B junto con enlaces sobre cómo comenzar si eres un usuario por primera vez.
slug: /guides
displayed_sidebar: default
---

# ¿Qué es W&B?

Weights & Biases (W&B) es la plataforma para desarrolladores de IA, con herramientas para el entrenamiento de modelos, ajuste fino de modelos y aprovechamiento de modelos base.

Configura W&B en 5 minutos, luego itera rápidamente en tu pipeline de aprendizaje automático con la confianza de que tus modelos y datos están siendo rastreados y versionados en un sistema de registro confiable.

![](@site/static/images/general/architecture.png)

Este diagrama muestra la relación entre los productos de W&B.

**[W&B Models](/guides/models.md)** es un conjunto de herramientas ligeras e interoperables para profesionales de aprendizaje automático que entrenan y ajustan modelos.
- [Experiments](/guides/track/intro.md): Seguimiento de experimentos de aprendizaje automático
- [Model Registry](/guides/model_registry/intro.md): Gestiona los modelos de producción de manera centralizada
- [Launch](/guides/launch/intro.md): Escala y automatiza cargas de trabajo
- [Sweeps](/guides/sweeps/intro.md): Ajuste de hiperparámetros y optimización de modelos

**[W&B Prompts](/guides/prompts/intro.md)** es para la depuración y monitoreo de LLM, incluyendo el uso de la API de GPT de OpenAI.

**[W&B Platform](/guides/platform.md)** es un conjunto central de bloques de construcción potentes para el seguimiento y visualización de datos y modelos, y la comunicación de resultados.
- [Artifacts](/guides/artifacts/intro.md): Versiona activos y rastrea linaje
- [Tables](/guides/tables/intro.md): Visualiza y consulta datos tabulares
- [Reports](/guides/reports/intro.md): Documenta y colabora en tus descubrimientos

## ¿Eres un usuario nuevo de W&B?

<iframe width="100%" height="330" src="https://www.youtube.com/embed/tHAFujRhZLA" title="Weights &amp; Biases End-to-End Demo" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

Comienza a explorar W&B con estos recursos:

1. [Intro Notebook](http://wandb.me/intro): Ejecuta un código de muestra rápido para rastrear experimentos en 5 minutos
2. [Quickstart](../quickstart.md): Lee una visión general rápida de cómo y dónde agregar W&B a tu código
1. Explora nuestra [Guía de Integraciones](./integrations/intro.md) y nuestra lista de reproducción [W&B Easy Integration YouTube](https://www.youtube.com/playlist?list=PLD80i8An1OEGDADxOBaH71ZwieZ9nmPGC) para obtener información sobre cómo integrar W&B con tu marco de trabajo de aprendizaje automático preferido.
1. Consulta la [Guía de Referencia de API](../ref/README.md) para especificaciones técnicas sobre la Biblioteca Python de W&B, CLI y operaciones de Weave.

## ¿Cómo funciona W&B?

Recomendamos leer las siguientes secciones en este orden si eres un usuario nuevo de W&B:

1. Aprende sobre [Runs](./runs/intro.md), la unidad básica de cómputo de W&B.
2. Crea y rastrea experimentos de aprendizaje automático con [Experiments](./track/intro.md).
3. Descubre el bloque de construcción flexible y ligero de W&B para el versionamiento de datasets y modelos con [Artifacts](./artifacts/intro.md).
4. Automatiza la búsqueda de hiperparámetros y explora el espacio de posibles modelos con [Sweeps](./sweeps/intro.md).
5. Gestiona el ciclo de vida del modelo desde el entrenamiento hasta la producción con [Model Management](./model_registry/intro.md).
6. Visualiza predicciones a través de versiones de modelos con nuestra guía de [Visualización de Datos](./tables/intro.md).
7. Organiza los Runs de W&B, incorpora y automatiza visualizaciones, describe tus hallazgos y comparte actualizaciones con colaboradores con [Reports](./reports/intro.md).