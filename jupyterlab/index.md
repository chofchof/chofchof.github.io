# JupyterLab

## JupyterLab Extensions

  - [List of JupyterLab Extensions](https://github.com/topics/jupyterlab-extension)

### JupyterLab requires [Node.js](https://nodejs.org)

```
conda install nodejs
```

### ipywidgets

```
conda install ipywidgets
```

  - [How to get ipywidgets working in Jupyter Lab?](https://stackoverflow.com/questions/49542417/how-to-get-ipywidgets-working-in-jupyter-lab)
    > JupyterLab now prefers a model where arbitrary javascript is no longer allowed to be embedded in a cell's output, which is how many interactive Jupyter Notebook modules used to work. They now ask that modules with interactivity create a JupyterLab extension. IPyWidgets has an extension that can be activated by running this on your command line (which assumes you already have NodeJS installed):
```
jupyter labextension install @jupyter-widgets/jupyterlab-manager
```
  
  - Links
    - [ipywidgets](https://github.com/jupyter-widgets/ipywidgets)
    - [ipywidgets Examples](https://github.com/jupyter-widgets/ipywidgets/blob/master/docs/source/examples/Index.ipynb)
    - [jupyterlab-manager](https://github.com/jupyter-widgets/ipywidgets/tree/master/packages/jupyterlab-manager)
  
## Documents

  - [JupyterLab Documentation](https://jupyterlab.readthedocs.io/en/stable/)
  - [Jupyter Widgets](https://ipywidgets.readthedocs.io/)
