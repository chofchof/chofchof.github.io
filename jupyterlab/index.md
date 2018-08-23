# JupyterLab

## JupyterLab Extensions

  - [List of JupyterLab Extensions](https://github.com/topics/jupyterlab-extension)

### JupyterLab extensions require [Node.js](https://nodejs.org)

```bash
conda install nodejs
```

### ipywidgets

```bash
conda install ipywidgets
```

  - [How to get ipywidgets working in Jupyter Lab?](https://stackoverflow.com/questions/49542417/how-to-get-ipywidgets-working-in-jupyter-lab)
    > JupyterLab now prefers a model where arbitrary javascript is no longer allowed to be embedded in a cell's output, which is how many interactive Jupyter Notebook modules used to work. They now ask that modules with interactivity create a JupyterLab extension. IPyWidgets has an extension that can be activated by running this on your command line (which assumes you already have NodeJS installed):
```bash
jupyter labextension install @jupyter-widgets/jupyterlab-manager
```

  - [Version compatibility](https://github.com/jupyter-widgets/ipywidgets/blob/master/packages/jupyterlab-manager/README.md) of jupyterlab-manager

    * For JupyterLab 0.30, use `jupyter labextension install @jupyter-widgets/jupyterlab-manager@0.31`
    * For JupyterLab 0.31rc1, use `jupyter labextension install @jupyter-widgets/jupyterlab-manager@0.32`
    * For JupyterLab 0.31rc2, use `jupyter labextension install @jupyter-widgets/jupyterlab-manager@0.33`
    * For JupyterLab 0.31.x, use `jupyter labextension install @jupyter-widgets/jupyterlab-manager@0.34`
    * For JupyterLab 0.32.x, use `jupyter labextension install @jupyter-widgets/jupyterlab-manager@0.35`
    * For JupyterLab 0.33.x, use `jupyter labextension install @jupyter-widgets/jupyterlab-manager@0.36`
    * For JupyterLab 0.34.x, use `jupyter labextension install @jupyter-widgets/jupyterlab-manager@0.37`

  - Links
    * [ipywidgets](https://github.com/jupyter-widgets/ipywidgets)
    * [ipywidgets Examples](https://github.com/jupyter-widgets/ipywidgets/blob/master/docs/source/examples/Index.ipynb)
    * [jupyterlab-manager](https://github.com/jupyter-widgets/ipywidgets/tree/master/packages/jupyterlab-manager)
  
## Documents

  - [JupyterLab Documentation](https://jupyterlab.readthedocs.io/en/stable/)
  - [Jupyter Widgets](https://ipywidgets.readthedocs.io/)
