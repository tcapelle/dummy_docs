---
description: Una visión general de lo que es W&B junto con enlaces sobre cómo empezar si eres un usuario por primera vez.
slug: /guides
displayed_sidebar: default
---

# ¿Qué es W&B?

W&B es la plataforma de aprendizaje automático para que los desarrolladores construyan mejores modelos más rápidamente. Utiliza las herramientas ligeras e interoperables de W&B para hacer un seguimiento rápido de los experimentos, versionar e iterar sobre datasets, evaluar el rendimiento del modelo, reproducir modelos, visualizar resultados y detectar regresiones, y compartir hallazgos con colegas.
Configura W&B en 5 minutos, luego itera rápidamente en tu pipeline de aprendizaje automático con la confianza de que tus datasets y modelos se rastrean y versionan en un sistema de registro confiable.

## ¿Eres un usuario nuevo de W&B?

Si es tu primera vez usando W&B, te sugerimos explorar lo siguiente:

1. Experimenta W&B en acción, [ejecuta un proyecto introductorio de ejemplo con Google Colab](http://wandb.me/intro).
2. Lee el [Quickstart](../quickstart.md) para una vista rápida de cómo y dónde agregar W&B a tu código.
3. Lee [¿Cómo funciona W&B?](#how-does-weights--biases-work) Esta sección proporciona una descripción general de los bloques de construcción de W&B.
4. Explora nuestra [guía de Integraciones](./integrations/intro.md) y nuestra lista de reproducción de [Integración Fácil de W&B en YouTube](https://www.youtube.com/playlist?list=PLD80i8An1OEGDADxOBaH71ZwieZ9nmPGC) para obtener información sobre cómo integrar W&B con tu framework de aprendizaje automático preferido.
5. Consulta la [guía de Referencia API](../ref/README.md) para especificaciones técnicas sobre la Biblioteca Python de W&B, CLI y operaciones de Weave.

## ¿Cómo funciona W&B?

Recomendamos leer las siguientes secciones en este orden si eres un usuario nuevo de W&B:

1. Aprende sobre [Runs](./runs/intro.md), la unidad básica de computación de W&B.
2. Crea y realiza el seguimiento de experimentos de aprendizaje automático con [Experiments](./track/intro.md).
3. Descubre el bloque de construcción flexible y ligero de W&B para versionamiento de dataset y modelo con [Artifacts](./artifacts/intro.md).
4. Automatiza la búsqueda de hiperparámetros y explora el espacio de posibles modelos con [Sweeps](./sweeps/intro.md).
5. Gestiona el ciclo de vida del modelo desde el entrenamiento hasta la producción con [Model Management](./models/intro.md).
6. Visualiza predicciones a través de versiones del modelo con nuestra [guía de Visualización de Datos](./data-vis/intro.md).
7. Organiza W&B Runs, incrusta y automatiza visualizaciones, describe tus hallazgos y comparte actualizaciones con colaboradores con [Reports](./reports/intro.md).