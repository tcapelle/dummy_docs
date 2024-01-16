

---
description: Inicio rápido de W&B.
displayed_sidebar: default
---

importar Tabs desde '@theme/Tabs';
importar TabItem desde '@theme/TabItem';

# Inicio rápido

Instala W&B y comienza a seguir tus experimentos de aprendizaje automático en minutos.

## 1. Crea una cuenta e instala W&B
Antes de comenzar, asegúrate de crear una cuenta e instalar W&B:

1. [Regístrate](https://wandb.ai/site) para obtener una cuenta gratuita en [https://wandb.ai/site](https://wandb.ai/site) y luego inicia sesión en tu cuenta de wandb.
2. Instala la biblioteca wandb en tu máquina en un entorno de Python 3 usando [`pip`](https://pypi.org/project/wandb/).

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

O si estás usando [W&B Server:](./guides/hosting)

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
    # Establece el proyecto donde se registrarán esta ejecución
    project="mi-proyecto-asombroso",
    # Realiza un seguimiento de los hiperparámetros y los metadatos de la ejecución
    config={
        "learning_rate": 0.01,
        "epochs": 10,
    })
```


<!-- ```python
run = wandb.init(project="my-awesome-project")
``` -->

Una [ejecución](./guides/runs) es el bloque de construcción básico de W&B. Las usarás a menudo para [seguir métricas](./guides/track), [crear registros](./guides/artifacts), [crear trabajos](./guides/launch) y más.


<!-- ## Track metrics -->
<!-- Pasa un diccionario al parámetro `config` con pares clave-valor de nombre de hiperparámetro y valores cuando inicialices un objeto de ejecución:

```python
  # Realiza un seguimiento de los hiperparámetros y los metadatos de la ejecución
  config={
      "learning_rate": lr,
      "epochs": epochs,
  }
``` -->


<!-- Usa [`wandb.log()`](./ref/python/log.md) para realizar un seguimiento de las métricas:

```python
wandb.log({'accuracy': acc, 'loss': loss})
```

Todo lo que registres con `wandb.log` se almacena en el objeto de ejecución que se inicializó más recientemente. -->



## Poniéndolo todo junto

Poniéndolo todo junto, tu script de entrenamiento podría ser similar al siguiente ejemplo de código. El código resaltado muestra código específico de W&B. 
Ten en cuenta que agregamos código que imita el entrenamiento de aprendizaje automático.

```python

# train.py
import wandb
import random # para el script de demostración

# resalta-la-siguiente-línea
wandb.login()

epochs=10
lr=0.01

# resalta-start
run = wandb.init(
    # Establece el proyecto donde se registrará esta ejecución
    project="mi-proyecto-asombroso",
    # Realiza un seguimiento de los hiperparámetros y los metadatos de la ejecución
    config={
        "learning_rate": lr,
        "epochs": epochs,
    })
<End of Markdown>

# resaltar-fin

offset = random.random() / 5
print(f"lr: {lr}")

# simulando una ejecución de entrenamiento
for epoch in range(2, epochs):
    acc = 1 - 2 ** -epoch - random.random() / epoch - offset
    loss = 2 ** -epoch + random.random() / epoch + offset
    print(f"epoch={epoch}, precisión={acc}, pérdida={loss}")
    # resaltar-siguiente-línea
    wandb.log({"precisión": acc, "pérdida": loss})

# run.log_code()
```

¡Eso es todo! Navega a la aplicación de W&B en [https://wandb.ai/home](https://wandb.ai/home) para ver cómo las métricas que registramos con W&B (precisión y pérdida) mejoraron en cada paso de entrenamiento.

![Muestra la pérdida y precisión que se rastrearon cada vez que ejecutamos el script anterior. ](/images/quickstart/quickstart_image.png)

La imagen anterior (haz clic para ampliarla) muestra la pérdida y precisión que se rastrearon cada vez que ejecutamos el script anterior. Cada objeto de ejecución creado se muestra en la columna **Ejecuciones**. Cada nombre de ejecución se genera aleatoriamente.


## ¿Qué sigue?
<!-- ### Obtén alertas

Recibe notificaciones por Slack o correo electrónico si tu ejecución de W&B se bloquea o cuando se cumple un disparador personalizado. Por ejemplo, puedes crear un disparador para que te notifique si tu pérdida reporta `NaN` o si se completa un paso en tu pipeline de aprendizaje automático.

Sigue el procedimiento descrito a continuación para configurar una alerta:

1. Activa las alertas en tu [Configuración de Usuario](https://wandb.ai/settings) de W&B.
2. Agrega [`wandb.alert()`](./guides/runs/alert.md) a tu código.

```python
wandb.alert(
    title="Baja precisión",
    text=f"La precisión {acc} está por debajo del umbral {thresh}"
)
```
Recibirás una alerta por correo electrónico o Slack cuando se cumpla el criterio de alerta. Por ejemplo, la imagen siguiente muestra una alerta de Slack:

![Alertas de W&B en un canal de Slack](/images/quickstart/get_alerts.png)

Consulta la documentación de [Alertas](./guides/runs/alert.md) para obtener más información sobre cómo configurar una alerta. Para obtener más información sobre las opciones de configuración, consulta la página de [Configuración](./guides/app/settings-page/intro.md).  -->

Explora el resto del ecosistema de W&B.

1. Consulta las [Integraciones de W&B](guides/integrations) para aprender cómo integrar W&B con tu framework de aprendizaje automático, como PyTorch, una biblioteca de aprendizaje automático como Hugging Face, o un servicio de aprendizaje automático como SageMaker.
2. Organiza las ejecuciones, incrusta y automatiza visualizaciones, describe tus descubrimientos y comparte actualizaciones con colaboradores con [Informes de W&B](./guides/reports).
2. Crea [Artefactos de W&B](./guides/artifacts) para rastrear conjuntos de datos, modelos, dependencias y resultados en cada paso de tu pipeline de aprendizaje automático.
3. Automatiza la búsqueda de hiperparámetros y explora el espacio de posibles modelos con [Barridos de W&B](./guides/sweeps).
4. Comprende tus conjuntos de datos, visualiza las predicciones del modelo y comparte ideas en un [panel de control central](./guides/data-vis).


![](/images/quickstart/wandb_demo_experiments.gif) 



## Preguntas frecuentes

**¿Dónde encuentro mi clave API?**
Una vez que hayas iniciado sesión en www.wandb.ai, la clave API estará en la [página de autorización](https://wandb.ai/authorize).

**¿Cómo uso W&B en un entorno automatizado?**
Si estás entrenando modelos en un entorno automatizado donde es incómodo ejecutar comandos de shell, como CloudML de Google, deberías consultar nuestra guía de configuración con [Variables de entorno](guides/track/environment-variables).

**¿Ofrecen instalaciones locales o en local?**
Sí, puedes [alojar W&B de forma privada](guides/hosting/) localmente en tus propias máquinas o en una nube privada. Prueba [este notebook de tutorial rápido](http://wandb.me/intro) para ver cómo. Ten en cuenta que para iniciar sesión en el servidor local de wandb, puedes [configurar el indicador de host](guides/hosting/how-to-guides/basic-setup) con la dirección de la instancia local.

**¿Cómo desactivo temporalmente el registro de wandb?**
Si estás probando código y quieres desactivar la sincronización de wandb, establece la variable de entorno [`WANDB_MODE=offline`](./guides/track/environment-variables).