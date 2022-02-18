# nodedraw
A Python library to make easy drawings with nodes

The idea would be to use the library like this:

```python
import nodedraw as nd
import numpy as np

N = 12

with nd.Figure("ciao.jpg") as f:
    for i, a in enumerate(np.linspace(0, 360, N, endpoint=False)):
        n = f.node(f"{i + 1}", at=nd.Point.polar(r, 90 - (a + 30)))
        f.draw(nd.Point.origin, n)
```

Running this script would already produce a `ciao.jpg` picture containing the first twelve numbers on a circle in counter-clockwise order.