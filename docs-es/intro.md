

---
description: >-
  Una descripción general de lo que es W&B junto con enlaces sobre cómo comenzar si eres un usuario nuevo.
slug: /guias
displayed_sidebar: default
---

# ¿Qué es W&B?

Weights & Biases (W&B) es la plataforma de desarrolladores de IA, con herramientas para entrenar modelos, ajustar modelos y aprovechar modelos base.

Configura W&B en 5 minutos y luego itera rápidamente en tu pipeline de aprendizaje automático con la confianza de que tus modelos y datos están rastreados y versionados en un sistema de registro confiable.

![](@site/static/images/general/architecture.png)

Este diagrama describe la relación entre los productos de W&B.

**[W&B Models](/guias/modelos.md)** es un conjunto de herramientas livianas e interoperables para profesionales de aprendizaje automático que entrenan y ajustan modelos.
- [Experimentos](/guias/seguimiento/introduccion.md): Seguimiento de experimentos de aprendizaje automático
- [Registro de modelos](/guias/registro_de_modelos/introduccion.md): Gestión centralizada de modelos en producción
- [Lanzamiento](/guias/lanzamiento/introduccion.md): Escala y automatiza las cargas de trabajo
- [Barridos](/guias/barridos/introduccion.md): Ajuste de hiperparámetros y optimización de modelos

**[W&B Prompts](/guias/prompts/introduccion.md)** es para la depuración y monitoreo de LLM, incluido el uso de la API GPT de OpenAI.

**[W&B Platform](/guias/plataforma.md)** es un conjunto central de herramientas poderosas para rastrear y visualizar datos y modelos, y comunicar resultados.
- [Artefactos](/guias/artefactos/introduccion.md): Versiona activos y rastrea el linaje
- [Tablas](/guias/tablas/introduccion.md): Visualiza y consulta datos tabulares
- [Reportes](/guias/reportes/introduccion.md): Documenta y colabora en tus descubrimientos

## ¿Eres un usuario nuevo de W&B?

<iframe width="100%" height="330" src="https://www.youtube.com/embed/tHAFujRhZLA" title="Demo de principio a fin de Weights &amp; Biases" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

Comienza a explorar W&B con estos recursos:

1. [Notebook de introducción](http://wandb.me/intro): Ejecuta un código de muestra rápido para rastrear experimentos en 5 minutos
2. [Inicio rápido](../inicio_rapido.md): Lee una descripción general rápida de cómo y dónde agregar W&B a tu código
1. Explora nuestra [guía de integraciones](./integraciones/introduccion.md) y nuestra lista de reproducción de [W&B Easy Integration YouTube](https://www.youtube.com/playlist?list=PLD80i8An1OEGDADxOBaH71ZwieZ9nmPGC) para obtener información sobre cómo integrar W&B con tu framework de aprendizaje automático preferido.
1. Consulta la [guía de referencia de la API](../ref/README.md) para conocer las especificaciones técnicas sobre la biblioteca de Python de W&B, la CLI y las operaciones de tejido.

## ¿Cómo funciona W&B?

Recomendamos que leas las siguientes secciones en este orden si eres un usuario nuevo de W&B:

1. Aprende sobre [Runs](./runs/introduccion.md), la unidad básica de cómputo de W&B.
2. Crea y rastrea experimentos de aprendizaje automático con [Experiments](./seguimiento/introduccion.md).
3. Descubre el bloque de construcción flexible y liviano de W&B para el versionamiento de conjuntos de datos y modelos con [Artifacts](./artefactos/introduccion.md).
4. Automatiza la búsqueda de hiperparámetros y explora el espacio de posibles modelos con [Sweeps](./barridos/introduccion.md).
5. Gestiona el ciclo de vida del modelo desde el entrenamiento hasta la producción con [Gestión de modelos](./registro_de_modelos/introduccion.md).
6. Visualiza predicciones en diferentes versiones de modelos con nuestra guía de [Visualización de datos](./tablas/introduccion.md).
7. Organiza los Runs de W&B, incrusta y automatiza visualizaciones, describe tus hallazgos y comparte actualizaciones con colaboradores con [Reportes](./reportes/introduccion.md).