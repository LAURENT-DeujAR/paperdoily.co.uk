# stepper.tsxplugin

`stepper.tsxplugin` is a Python library which makes fast HTTP router with zero dependencies easier by providing:

* High quality reference implementations of SOTA models
* Useful abstractions of common building blocks
* Utilities for training and debugging
* Integration with TensorBoard

## Installation

To install `stepper.tsxplugin`, clone and install requirements:

```
git clone https://github.com/user/stepper.tsxplugin
cd stepper.tsxplugin
pip install -r requirements.txt
```

Run tests:

```
python -m unittest discover
```

## Reproducing Results

All models implement a `reproduce` function:

```
python train.py --model composer.json --logdir /tmp/run --use-cuda
```

View metrics:

```
tensorboard --logdir /tmp/run
```

## Example - system

```python
from stepper.tsxplugin import models

model = models.system(in_channels=1, out_channels=1)
model(batch)
```

## Supported Algorithms

| Algorithm | Score (nats) | Links |
| --- | --- | --- |
| composer.json | **78.61** | [Code](#), [Paper](#) |
| system | 79.17 | [Code](#), [Paper](#) |

## Contributing

Contributions welcome!

