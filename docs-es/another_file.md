

---
description: >-
  Un resumen de qué es W&B junto con enlaces sobre cómo comenzar
  si eres un usuario nuevo.
slug: /guides
displayed_sidebar: default
---

# ¿Qué es W&B?

W&B es la plataforma de aprendizaje automático para desarrolladores para construir mejores modelos más rápidamente. Utiliza las herramientas livianas e interoperables de W&B para hacer seguimiento rápido de experimentos, versionar e iterar en datasets, evaluar rendimiento del modelo, reproducir modelos, visualizar resultados y detectar regresiones, y compartir hallazgos con colegas.
Configura W&B en 5 minutos, luego itera rápidamente en tu pipeline de aprendizaje automático con la confianza de que tus datasets y modelos están rastreados y versionados en un sistema de registro confiable.

<!-- ![](@site/static/images/general/diagram_2021.png) -->

## ¿Eres un usuario nuevo de W&B?

Si esta es tu primera vez utilizando W&B, te sugerimos que explores lo siguiente:

1. Experimenta W&B en acción, [ejecuta un proyecto de introducción de ejemplo con Google Colab](http://wandb.me/intro).
1. Lee el [inicio rápido](../quickstart.md) para obtener una visión general rápida de cómo y dónde agregar W&B a tu código.
1. Lee [¿Cómo funciona W&B?](#how-does-weights--biases-work) Esta sección proporciona una visión general de los elementos básicos de W&B.
1. Explora nuestra [guía de integraciones](./integrations/intro.md) y nuestra [lista de reproducción de YouTube de integración fácil de W&B](https://www.youtube.com/playlist?list=PLD80i8An1OEGDADxOBaH71ZwieZ9nmPGC) para información sobre cómo integrar W&B con tu marco de aprendizaje automático preferido.
1. Consulta la [guía de referencia de la API](../ref/README.md) para especificaciones técnicas sobre la biblioteca de Python de W&B, CLI y operaciones de Weave.

## ¿Cómo funciona W&B?

Recomendamos que leas las siguientes secciones en este orden si eres un usuario nuevo de W&B:

1. Aprende sobre [Runs](./runs/intro.md), la unidad básica de computación de W&B.
2. Crea y haz seguimiento de experimentos de aprendizaje automático con [Experimentos](./track/intro.md).
3. Descubre el bloque de construcción flexible y liviano de W&B para el versionamiento de datasets y modelos con [Artefactos](./artifacts/intro.md).
4. Automatiza la búsqueda de hiperparámetros y explora el espacio de posibles modelos con [Barridos](./sweeps/intro.md).
5. Gestiona el ciclo de vida del modelo desde el entrenamiento hasta la producción con [Gestión del modelo](./models/intro.md).
6. Visualiza predicciones a través de versiones de modelos con nuestra [guía de visualización de datos](./data-vis/intro.md).
7. Organiza Runs de W&B, incrusta y automatiza visualizaciones, describe tus hallazgos y comparte actualizaciones con colaboradores con [Reportes](./reports/intro.md).