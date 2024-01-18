---
description: W&B Quickstart.
displayed_sidebar: default
---

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

# Quickstart

Install W&B and start tracking your machine learning experiments in minutes.

## 1. Create an account and install W&B
Before you get started, make sure you create an account and install W&B:

1. [Sign up](https://wandb.ai/site) for a free account at [https://wandb.ai/site](https://wandb.ai/site) and then login to your wandb account.  
2. Install the wandb library on your machine in a Python 3 environment using [`pip`](https://pypi.org/project/wandb/).  
<!-- 3. Login to the wandb library on your machine. You will find your API key here: [https://wandb.ai/authorize](https://wandb.ai/authorize).   -->

The following code snippets demonstrate how to install and log into W&B using the W&B CLI and Python Library:

<Tabs
  defaultValue="notebook"
  values={[
    {label: 'Notebook', value: 'notebook'},
    {label: 'Command Line', value: 'cli'},
  ]}>
  <TabItem value="cli">

Install the CLI and Python library for interacting with the Weights and Biases API:

```
pip install wandb
```

  </TabItem>
  <TabItem value="notebook">

Install the CLI and Python library for interacting with the Weights and Biases API:

```python
!pip install wandb
```


  </TabItem>
</Tabs>

## 2. Log in to W&B


<Tabs
  defaultValue="notebook"
  values={[
    {label: 'Notebook', value: 'notebook'},
    {label: 'Command Line', value: 'cli'},
  ]}>
  <TabItem value="cli">

Next, log in to W&B:

```
wandb login
```

Or if you are using [W&B Server:](./guides/hosting)

```
wandb login --host=http://wandb.your-shared-local-host.com
```

Provide [your API key](https://wandb.ai/authorize) when prompted.

  </TabItem>
  <TabItem value="notebook">

Next, import the W&B Python SDK and log in:

```python
wandb.login()
```

Provide [your API key](https://wandb.ai/authorize) when prompted.
  </TabItem>
</Tabs>


## 3. Start a  run and track hyperparameters

Initialize a W&B Run object in your Python script or notebook with [`wandb.init()`](./ref/python/run.md) and pass a dictionary to the `config` parameter with key-value pairs of hyperparameter names and values:

```python
run = wandb.init(
    # Set the project where this run will be logged
    project="my-awesome-project",
    # Track hyperparameters and run metadata
    config={
        "learning_rate": 0.01,
        "epochs": 10,
    })
```


<!-- ```python
run = wandb.init(project="my-awesome-project")
``` -->

A [run](./guides/runs) is the basic building block of W&B. You will use them often to [track metrics](./guides/track), [create logs](./guides/artifacts), [create jobs](./guides/launch), and more.


<!-- ## Track metrics -->
<!-- Pass a dictionary to the `config` parameter with key-value pairs of hyperparameter name and values when you initialize a run object:

```python
  # Track hyperparameters and run metadata
  config={
      "learning_rate": lr,
      "epochs": epochs,
  }
``` -->


<!-- Use [`wandb.log()`](./ref/python/log.md) to track metrics:

```python
wandb.log({'accuracy': acc, 'loss': loss})
```

Anything you log with `wandb.log` is stored in the run object that was most recently initialized. -->

The image above (click to expand) shows the loss and accuracy that was tracked from each time we ran the script above.  Each run object that was created is show within the **Runs** column. Each run name is randomly generated.
