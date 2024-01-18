

---
description: Inicio rápido de W&B.
displayed_sidebar: default
---

importar Tabs from '@theme/Tabs';
importar TabItem from '@theme/TabItem';

# Inicio rápido

Instala W&B y comienza a hacer seguimiento de tus experimentos de aprendizaje automático en minutos.

## 1. Crea una cuenta e instala W&B
Antes de comenzar, asegúrate de crear una cuenta e instalar W&B:

1. [Regístrate](https://wandb.ai/site) para obtener una cuenta gratuita en [https://wandb.ai/site](https://wandb.ai/site) y luego inicia sesión en tu cuenta de wandb.
2. Instala la biblioteca wandb en tu máquina en un entorno de Python 3 usando [`pip`](https://pypi.org/project/wandb/).
<!-- 3. Inicia sesión en la biblioteca wandb en tu máquina. Aquí encontrarás tu clave API: [https://wandb.ai/authorize](https://wandb.ai/authorize). -->

Los siguientes fragmentos de código muestran cómo instalar e iniciar sesión en W&B utilizando la CLI de W&B y la biblioteca de Python:

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
La imagen de arriba (haz clic para ampliar) muestra la pérdida y la precisión que se registraron cada vez que se ejecutó el script anterior. Cada objeto de ejecución que se creó se muestra en la columna **Runs**. Cada nombre de ejecución se genera aleatoriamente.