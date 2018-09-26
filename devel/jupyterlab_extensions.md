# JupyterLab Extensions

  - JupyterLab extensions require [Node.js](https://nodejs.org)
```bash
conda install nodejs
```

  - Update JupyterLab extensions
```bash
jupyter labextension update --all
```

  - [List of JupyterLab Extensions](https://github.com/topics/jupyterlab-extension)
```bash
jupyter labextension list
```

## ipywidgets

```bash
conda install ipywidgets
jupyter labextension install @jupyter-widgets/jupyterlab-manager
```

  - [How to get ipywidgets working in Jupyter Lab?](https://stackoverflow.com/questions/49542417/how-to-get-ipywidgets-working-in-jupyter-lab)
    > JupyterLab now prefers a model where arbitrary javascript is no longer allowed to be embedded in a cell's output, which is how many interactive Jupyter Notebook modules used to work. They now ask that modules with interactivity create a JupyterLab extension. IPyWidgets has an extension that can be activated by running this on your command line (which assumes you already have NodeJS installed): `jupyter labextension install @jupyter-widgets/jupyterlab-manager`

  - [Version compatibility](https://github.com/jupyter-widgets/ipywidgets/blob/master/packages/jupyterlab-manager/README.md) of jupyterlab-manager

    * For JupyterLab 0.31.x, `jupyter labextension install @jupyter-widgets/jupyterlab-manager@0.34`
    * For JupyterLab 0.32.x, `jupyter labextension install @jupyter-widgets/jupyterlab-manager@0.35`
    * For JupyterLab 0.33.x, `jupyter labextension install @jupyter-widgets/jupyterlab-manager@0.36`
    * For JupyterLab 0.34.x, `jupyter labextension install @jupyter-widgets/jupyterlab-manager@0.37`

  - Links
    * [ipywidgets](https://github.com/jupyter-widgets/ipywidgets)
    * [ipywidgets Examples](https://github.com/jupyter-widgets/ipywidgets/blob/master/docs/source/examples/Index.ipynb)
    * [jupyterlab-manager](https://github.com/jupyter-widgets/ipywidgets/tree/master/packages/jupyterlab-manager)

## JupyterLab LaTeX

```bash
pip install jupyterlab-latex
jupyter labextension install @jupyterlab/latex
```

  - An extension for JupyterLab which allows for live-editing of LaTeX documents.
  
  - Links
    * [jupyterlab-latex](https://github.com/jupyterlab/jupyterlab-latex)

## ipympl

```bash
pip install ipympl
jupyter labextension install jupyter-matplotlib
```

  - Matplotlib Jupyter Extension. To enable the jupyter-matplotlib backend, simply use the matplotlib Jupyter magic:
```python
%matplotlib widget
# or %matplotlib ipympl

import matplotlib as mpl
print(mpl.get_backend())
# returns module://ipympl.backend_nbagg

import matplotlib.pyplot as plt
plt.ioff() # turn off interactive mode
```
  
  - Links
    * [jupyter-matplotlib](https://github.com/matplotlib/jupyter-matplotlib)
