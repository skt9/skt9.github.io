---
layout: page
title: Visualization & Annotation Info-Storage
description: Place where information about visualiation and annotation are stored
---

[Matplotlib ColorMap Info 1](https://stackoverflow.com/questions/43938425/matplotlib-change-colormap-tab20-to-have-three-colors)


###  Visually differentiated colors {#viz-diff-colors}
```python
import matplotlib as plt
cmap = plt.cm.get_cmap('tab20c')
colors = np.array(cmap.colors)
````
Other options that work are <b>'tab10c'</b>, <b>'tab20_r'</b>.

---

### Compositing images with tthe object masks {#compositing-image-obj-masks}

To blend images with object masks
