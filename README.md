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

# Example usage:
with figsize_as(4, 4):
    fig, ax = plt.subplots()
    ax.plot([0, 1], [0, 1])
    plt.show()
```
