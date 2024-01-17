

---
descripción: Inicio rápido de W&B.
displayed_sidebar: default
---

importar Pestañas desde '@theme/Tabs';
importar Elemento de pestaña desde '@theme/TabItem';

# Inicio rápido

Instala W&B y comienza a hacer un seguimiento de tus experimentos de aprendizaje automático en minutos.

## 1. Crea una cuenta e instala W&B
Antes de comenzar, asegúrate de crear una cuenta e instalar W&B:

1. [Regístrate](https://wandb.ai/site) para obtener una cuenta gratuita en [https://wandb.ai/site](https://wandb.ai/site) y luego inicia sesión en tu cuenta de wandb.
2. Instala la biblioteca wandb en tu máquina en un entorno de Python 3 utilizando [`pip`](https://pypi.org/project/wandb/).
<!-- 3. Inicia sesión en la biblioteca wandb en tu máquina. Aquí encontrarás tu clave API: [https://wandb.ai/authorize](https://wandb.ai/authorize).   -->

Los siguientes fragmentos de código demuestran cómo instalar e iniciar sesión en W&B utilizando la CLI de W&B y la biblioteca de Python:

<Tabs
  defaultValue="notebook"
  values={[
    {label: 'Notebook', value: 'notebook'},
    {label: 'Línea de comandos', value: 'cli'},
  ]}>
  <TabItem value="cli">

Instala la CLI y la biblioteca de Python para interactuar con la API de Weights and Biases:

```
pip install wandb
```

  </TabItem>
  <TabItem value="notebook">

Instala la CLI y la biblioteca de Python para interactuar con la API de Weights and Biases:

```python
!pip install wandb
```


  </TabItem>
</Tabs>

## 2. Inicia sesión en W&B


<Tabs
  defaultValue="notebook"
  values={[
    {label: 'Notebook', value: 'notebook'},
    {label: 'Línea de comandos', value: 'cli'},
  ]}>
  <TabItem value="cli">

A continuación, inicia sesión en W&B:

```
wandb login
```

O si estás utilizando [W&B Server:](./guides/hosting)

```
wandb login --host=http://wandb.your-shared-local-host.com
```

Proporciona [tu clave API](https://wandb.ai/authorize) cuando se te solicite.

  </TabItem>
  <TabItem value="notebook">

A continuación, importa el SDK de Python de W&B e inicia sesión:

```python
wandb.login()
```

Proporciona [tu clave API](https://wandb.ai/authorize) cuando se te solicite.
  </TabItem>
</Tabs>

## 3. Inicia una ejecución y realiza un seguimiento de los hiperparámetros

Inicializa un objeto de ejecución de W&B en tu script de Python o notebook con [`wandb.init()`](./ref/python/run.md) y pasa un diccionario al parámetro `config` con pares clave-valor de nombres de hiperparámetros y valores:

```python
run = wandb.init(
    # Establece el proyecto en el que se registrará esta ejecución
    project="mi-proyecto-asombroso",
    # Realiza un seguimiento de los hiperparámetros y metadatos de la ejecución
    config={
        "learning_rate": 0.01,
        "epochs": 10,
    })
```


<!-- ```python
run = wandb.init(project="mi-proyecto-asombroso")
``` -->

Una [ejecución](./guides/runs) es el componente básico de W&B. Las utilizarás a menudo para [realizar un seguimiento de las métricas](./guides/track), [crear registros](./guides/artifacts), [crear trabajos](./guides/launch) y más.


<!-- ## Realizar un seguimiento de las métricas -->
<!-- Pasa un diccionario al parámetro `config` con pares clave-valor de nombres de hiperparámetros y valores cuando inicialices un objeto de ejecución:

```python
  # Realiza un seguimiento de los hiperparámetros y metadatos de la ejecución
  config={
      "learning_rate": lr,
      "epochs": epochs,
  }
``` -->


<!-- Utiliza [`wandb.log()`](./ref/python/log.md) para realizar un seguimiento de las métricas:

```python
wandb.log({'accuracy': acc, 'loss': loss})
```

Todo lo que registres con `wandb.log` se almacena en el objeto de ejecución que se inicializó más recientemente. -->



## Poniéndolo todo junto

Poniéndolo todo junto, tu script de entrenamiento podría verse similar al siguiente ejemplo de código. El código resaltado muestra código específico de W&B.
Ten en cuenta que hemos agregado código que imita el entrenamiento de aprendizaje automático.

```python

# train.py
import wandb
import random # para el script de demostración

# resaltar-siguiente-línea
wandb.login()

epochs=10
lr=0.01

# resaltar-inicio
run = wandb.init(
    # Establece el proyecto en el que se registrará esta ejecución
    project="mi-proyecto-asombroso",
    # Realiza un seguimiento de los hiperparámetros y metadatos de la ejecución
    config={
        "learning_rate": lr,
        "epochs": epochs,
    })
<End of Markdown>

# highlight-end    

offset = random.random() / 5
print(f"lr: {lr}")

# simulando una ejecución de entrenamiento
for epoch in range(2, epochs):
    acc = 1 - 2 ** -epoch - random.random() / epoch - offset
    loss = 2 ** -epoch + random.random() / epoch + offset
    print(f"epoch={epoch}, precisión={acc}, pérdida={loss}")
    # highlight-next-line
    wandb.log({"precisión": acc, "pérdida": loss})

# run.log_code()
```

¡Eso es todo! Navega a la aplicación de W&B en [https://wandb.ai/home](https://wandb.ai/home) para ver cómo las métricas que registramos con W&B (precisión y pérdida) mejoraron en cada paso de entrenamiento.

![Muestra la pérdida y precisión que se registraron en cada ejecución del script anterior. ](/images/quickstart/quickstart_image.png)

La imagen anterior (haz clic para ampliar) muestra la pérdida y precisión que se registraron en cada ejecución del script anterior. Cada objeto de ejecución que se creó se muestra en la columna **Ejecuciones**. Cada nombre de ejecución se genera aleatoriamente.