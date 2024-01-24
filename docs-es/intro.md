

---
description: >-
  Una descripción general de lo que es W&B junto con enlaces sobre cómo comenzar
  si eres un usuario principiante.
slug: /guías
displayed_sidebar: default
---

# ¿Qué es W&B?

Weights & Biases (W&B) es la plataforma para desarrolladores de IA, con herramientas para entrenar modelos, ajustar modelos y aprovechar los modelos fundacionales.

Configura W&B en 5 minutos, luego itera rápidamente en tu pipeline de aprendizaje automático con la confianza de que tus modelos y datos están seguidos y versionados en un sistema de registro confiable.

![](@site/static/images/general/architecture.png)

Este diagrama muestra la relación entre los productos de W&B.

**[Modelos de W&B](/guías/modelos.md)** es un conjunto de herramientas interoperables y ligeras para profesionales del aprendizaje automático que entrenan y ajustan modelos.
- [Experimentos](/guías/track/intro.md): Seguimiento de experimentos de aprendizaje automático
- [Registro de Modelos](/guías/model_registry/intro.md): Gestiona los modelos de producción de forma centralizada
- [Launch](/guías/launch/intro.md): Escala y automatiza cargas de trabajo
- [Barridos](/guías/sweeps/intro.md): Ajuste de hiperparámetros y optimización de modelos

**[Prompts de W&B](/guías/prompts/intro.md)** es para la depuración y monitoreo de LLM, incluyendo el uso de la API de GPT de OpenAI.

**[Plataforma W&B](/guías/platform.md)** es un conjunto central de bloques de construcción poderosos para el seguimiento y la visualización de datos y modelos, y la comunicación de resultados.
- [Artefactos](/guías/artifacts/intro.md): Versiona activos y sigue el linaje
- [Tablas](/guías/tables/intro.md): Visualiza y consulta datos tabulares
- [Reportes](/guías/reports/intro.md): Documenta y colabora en tus descubrimientos

## ¿Eres un usuario principiante de W&B?

<iframe width="100%" height="330" src="https://www.youtube.com/embed/tHAFujRhZLA" title="Demostración End-to-End de Weights &amp; Biases" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

Empieza a explorar W&B con estos recursos:

1. [Notebook de Introducción](http://wandb.me/intro): Ejecuta código de muestra rápido para seguir los experimentos en 5 minutos
2. [Inicio Rápido](../quickstart.md): Lee una descripción general rápida de cómo y dónde agregar W&B a tu código
3. Explora nuestra [Guía de Integraciones](./integrations/intro.md) y nuestra [Lista de Reproducción de Integración Fácil de W&B en YouTube](https://www.youtube.com/playlist?list=PLD80i8An1OEGDADxOBaH71ZwieZ9nmPGC) para obtener información sobre cómo integrar W&B con tu marco de aprendizaje automático preferido.
4. Consulta la [Guía de Referencia de API](../ref/README.md) para especificaciones técnicas sobre la Biblioteca Python de W&B, la Interfaz de Línea de Comandos y las operaciones de Weave.

## ¿Cómo funciona W&B?

Si eres un usuario principiante de W&B, te recomendamos que leas las siguientes secciones en este orden:

1. Aprende sobre [Runs](./runs/intro.md), la unidad básica de cálculo de W&B.
2. Crea y sigue experimentos de aprendizaje automático con [Experimentos](./track/intro.md).
3. Descubre el bloque de construcción flexible y ligero de W&B para el versionamiento de conjuntos de datos y modelos con [Artefactos](./artifacts/intro.md).
4. Automatiza la búsqueda de hiperparámetros y explora el espacio de posibles modelos con [Barridos](./sweeps/intro.md).
5. Gestiona el ciclo de vida del modelo desde el entrenamiento hasta la producción con [Gestión del Modelo](./model_registry/intro.md).
6. Visualiza las predicciones a través de las versiones del modelo con nuestra [Guía de Visualización de Datos](./tables/intro.md).
7. Organiza las Runs de W&B, incrusta y automatiza visualizaciones, describe tus hallazgos y comparte actualizaciones con colaboradores con [Reportes](./reports/intro.md).