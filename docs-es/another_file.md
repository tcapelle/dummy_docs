

---
description: >-
  Una visión general de qué es W&B junto con enlaces sobre cómo comenzar si eres un usuario nuevo.
slug: /guías
displayed_sidebar: default
---

# ¿Qué es W&B?

W&B es la plataforma de aprendizaje automático para desarrolladores que les permite construir mejores modelos más rápido. Utiliza las herramientas ligeras e interoperables de W&B para realizar un seguimiento rápido de experimentos, versionar y iterar en conjuntos de datos, evaluar el rendimiento del modelo, reproducir modelos, visualizar resultados y detectar regresiones, y compartir hallazgos con colegas.
Configura W&B en 5 minutos y luego itera rápidamente en tu pipeline de aprendizaje automático con la confianza de que tus conjuntos de datos y modelos se rastrean y versionan en un sistema de registro confiable.

<!-- ![](@site/static/images/general/diagram_2021.png) -->

## ¿Eres un usuario nuevo de W&B?

Si es la primera vez que usas W&B, te sugerimos que explores lo siguiente:

1. Experimenta W&B en acción, [ejecuta un proyecto de introducción de ejemplo con Google Colab](http://wandb.me/intro).
1. Lee el [inicio rápido](../quickstart.md) para obtener una visión general rápida de cómo y dónde agregar W&B a tu código.
1. Lee [¿Cómo funciona W&B?](#cómo-funciona-weights--biases) Esta sección proporciona una visión general de los bloques de construcción de W&B.
1. Explora nuestra [guía de integraciones](./integrations/intro.md) y nuestra lista de reproducción de [Integración fácil de W&B en YouTube](https://www.youtube.com/playlist?list=PLD80i8An1OEGDADxOBaH71ZwieZ9nmPGC) para obtener información sobre cómo integrar W&B con tu framework de aprendizaje automático preferido.
1. Consulta la [guía de referencia de la API](../ref/README.md) para obtener especificaciones técnicas sobre la biblioteca de Python de W&B, la CLI y las operaciones de Weave.

## ¿Cómo funciona W&B?

Recomendamos que leas las siguientes secciones en este orden si eres un usuario nuevo de W&B:

1. Aprende sobre [Runs](./runs/intro.md), la unidad básica de computación de W&B.
2. Crea y realiza un seguimiento de experimentos de aprendizaje automático con [Experiments](./track/intro.md).
3. Descubre los artefactos flexibles y ligeros de W&B para la versión de conjuntos de datos y modelos con [Artifacts](./artifacts/intro.md).
4. Automatiza la búsqueda de hiperparámetros y explora el espacio de posibles modelos con [Sweeps](./sweeps/intro.md).
5. Gestiona el ciclo de vida del modelo desde el entrenamiento hasta la producción con [Model Management](./models/intro.md).
6. Visualiza predicciones entre versiones de modelos con nuestra [guía de visualización de datos](./data-vis/intro.md).
7. Organiza los Runs de W&B, incrusta y automatiza visualizaciones, describe tus hallazgos y comparte actualizaciones con colaboradores con [Reports](./reports/intro.md).