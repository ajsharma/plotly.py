# plotly.py

## Quickstart

`pip install plotly "notebook>=5.3" "ipywidgets>=7.2"`

Inside [Jupyter notebook](https://jupyter.org/install):
```python
import plotly.graph_objs as go
fig = go.FigureWidget()
# Display an empty figure
fig
```
```python
# Add a scatter chart
fig.add_scatter(y=[2, 1, 4, 3])
# Add a bar chart
fig.add_bar(y=[1, 4, 3, 2])
# Add a title
fig.layout.title = 'Hello FigureWidget'
```

See the [Python documentation](https://plot.ly/python/) for more examples.

Read about what's new in [plotly.py v3](https://medium.com/@plotlygraphs/introducing-plotly-py-3-0-0-7bb1333f69c6)

## Overview
[plotly.py](https://plot.ly/d3-js-for-python-and-pandas-charts/) is an interactive, open-source, and browser-based graphing library for Python :sparkles:

Built on top of [plotly.js](https://github.com/plotly/plotly.js), `plotly.py` is a high-level, declarative charting library. plotly.js ships with over 30 chart types, including scientific charts, 3D graphs, statistical charts, SVG maps, financial charts, and more.

`plotly.py` is [MIT Licensed](LICENSE.txt). Plotly graphs can be viewed in Jupyter notebooks, standalone HTML files, or hosted online on [plot.ly](https://plot.ly).

[Contact us](https://plot.ly/products/consulting-and-oem/) for Plotly.js consulting, dashboard development, application integration, and feature additions. Sharing your graphs online or in dashboards? Consider a [plot.ly subscription](https://plot.ly/products/cloud).

<p align="center">
    <a href="https://plot.ly/python" target="_blank">
    <img src="https://raw.githubusercontent.com/cldougl/plot_images/add_r_img/plotly_2017.png">
</a></p>

***

- [Online Documentation](https://plot.ly/python)
- [Contributing](contributing.md)
- [Changelog](CHANGELOG.md)
- [Code of Conduct](CODE_OF_CONDUCT.md)
- [Version 3 Migration Guide](migration-guide.md)
- [New! Announcing Dash](https://medium.com/@plotlygraphs/introducing-dash-5ecf7191b503)
- [Community](https://community.plot.ly/c/api/python)

***

## Installation

plotly.py may be installed using pip...
```
pip install plotly==3.2.0
```

or conda.
```
conda install -c plotly plotly=3.2.0
```

### Jupyter Notebook Support
For use in the Jupyter Notebook, install the `notebook` and `ipywidgets`
packages using pip...

```
pip install "notebook>=5.3" "ipywidgets>=7.2"
```

of conda.

```
conda install "notebook>=5.3" "ipywidgets>=7.2"
```

### JupyterLab Support
For use in JupyterLab, install the `jupyterlab` and `ipywidgets`
packages using pip... 

```
pip install jupyterlab==0.33 "ipywidgets>=7.2"
```

of conda.

```
conda install jupyterlab==0.33 "ipywidgets>=7.2"
```

Then run the following commands to install the required JupyterLab extensions:
```
# Avoid "JavaScript heap out of memory" errors during extension installation
# (OS X/Linux)
export NODE_OPTIONS=--max-old-space-size=4096
# (Windows)
set NODE_OPTIONS=--max-old-space-size=4096

# Jupyter widgets extension
jupyter labextension install @jupyter-widgets/jupyterlab-manager@0.36 --no-build

# FigureWidget support
jupyter labextension install plotlywidget@0.2.1  --no-build

# offline iplot support
jupyter labextension install @jupyterlab/plotly-extension@0.16  --no-build

# Build extensions (must be done to activate extensions since --no-build is used above)
jupyter lab build
```

### Static Image Export
plotly.py supports static image export using the `to_image` and `write_image`
functions in the `plotly.io` package. This functionality requires the
installation of the plotly [orca](TODO) command line utility and the
[`psutil`](TODO) Python package.

These dependencies can both be installed using conda:
```
conda install -c plotly plotly-conda psutil
```

Or, `psutil` can be installed using pip...
```
pip install psutil
```

and orca can be installed according to the instructions in the [orca README](TODO).

## Migration
If you're migrating from plotly.py version 2, please check out the [migration guide](migration-guide.md)

## Copyright and Licenses
Code and documentation copyright 2018 Plotly, Inc.

Code released under the [MIT license](LICENSE.txt).

Docs released under the [Creative Commons license](https://github.com/plotly/documentation/blob/source/LICENSE).
