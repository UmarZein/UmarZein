```python
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
```
