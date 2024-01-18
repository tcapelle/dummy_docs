

---
descripción: >-
  Una visión general de qué es W&B junto con enlaces sobre cómo comenzar si eres un usuario nuevo.
slug: /guias
displayed_sidebar: default
---

# ¿Qué es W&B?

W&B es la plataforma de aprendizaje automático para desarrolladores para construir mejores modelos más rápido. Utiliza las herramientas ligeras e interoperables de W&B para realizar un seguimiento rápido de los experimentos, versionar e iterar en los conjuntos de datos, evaluar el rendimiento del modelo, reproducir modelos, visualizar resultados y detectar regresiones, y compartir hallazgos con colegas.
Configura W&B en 5 minutos, luego itera rápidamente en tu pipeline de aprendizaje automático con la confianza de que tus conjuntos de datos y modelos están rastreados y versionados en un sistema de registro confiable.

<!-- ![](@site/static/images/general/diagram_2021.png) -->

## ¿Eres un usuario nuevo de W&B?

Si es la primera vez que utilizas W&B, te sugerimos que explores lo siguiente:

1. Experimenta W&B en acción, [ejecuta un proyecto de introducción de ejemplo con Google Colab](http://wandb.me/intro).
1. Lee el [Inicio rápido](../quickstart.md) para obtener una visión general rápida de cómo y dónde agregar W&B a tu código.
1. Lee [¿Cómo funciona W&B?](#como-funciona-weights--biases) Esta sección proporciona una descripción general de los bloques de construcción de W&B.
1. Explora nuestra [guía de Integraciones](./integrations/intro.md) y nuestra lista de reproducción de [W&B Easy Integration en YouTube](https://www.youtube.com/playlist?list=PLD80i8An1OEGDADxOBaH71ZwieZ9nmPGC) para obtener información sobre cómo integrar W&B con tu framework de aprendizaje automático preferido.
1. Consulta la [guía de Referencia de API](../ref/README.md) para obtener especificaciones técnicas sobre la biblioteca de Python de W&B, CLI y operaciones de tejido.

## ¿Cómo funciona W&B?


Te recomendamos que leas las siguientes secciones en este orden si eres un usuario nuevo de W&B:

1. Aprende sobre [Runs](./runs/intro.md), la unidad básica de computación de W&B.
2. Crea y realiza un seguimiento de experimentos de aprendizaje automático con [Experiments](./track/intro.md).
3. Descubre el bloque de construcción flexible y ligero de W&B para el versionamiento de conjuntos de datos y modelos con [Artifacts](./artifacts/intro.md).
4. Automatiza la búsqueda de hiperparámetros y explora el espacio de posibles modelos con [Sweeps](./sweeps/intro.md).
5. Gestiona el ciclo de vida del modelo, desde el entrenamiento hasta la producción, con [Model Management](./models/intro.md).
6. Visualiza predicciones en diferentes versiones de modelos con nuestra guía de [Visualización de Datos](./data-vis/intro.md).
7. Organiza los Runs de W&B, incrusta y automatiza visualizaciones, describe tus hallazgos y comparte actualizaciones con colaboradores con [Reports](./reports/intro.md).