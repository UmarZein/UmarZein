```python
import numpy as np
import pandas as pd
import torch
from torch import nn
import lightning as pl
from torch.utils.data import DataLoader, Dataset, random_split
import matplotlib.pyplot as plt
from contextlib import contextmanager

@contextmanager
def figsize_as(width, height):
    original_figsize = plt.rcParams['figure.figsize']
    try:
        plt.rcParams['figure.figsize'] = [width, height]
        yield
    finally:
        plt.rcParams['figure.figsize'] = original_figsize

# Example usage:
with figsize_as(4, 4):
    fig, ax = plt.subplots()
    ax.plot([0, 1], [0, 1])
    plt.show()
```
