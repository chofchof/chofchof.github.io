# Mayavi

## Installation under Conda

  - [Miniconda installer archive](https://repo.continuum.io/miniconda/)
  - [Creating an environment from an `environment.yml` file](https://conda.io/docs/user-guide/tasks/manage-environments.html#creating-an-environment-from-an-environment-yml-file)
    * Sample [`mayavi.yml`](mayavi.yml)
    ```bash
    conda env create -f mayavi.yml
    ```
  - Run Jupyter Qt Console under `mayavi` environment
    ```bash
    conda activate mayavi && jupyter-qtconsole
    ```
    and test your installation
    ```python
    %gui qt
    from mayavi import mlab
    mlab.test_plot3d()
    ```
  - (Optional) Install Jupyter Notebook Extension
    ```bash
    conda activate mayavi
    jupyter nbextension install mayavi --user --py
    jupyter nbextension enable mayavi --user --py
    ```
    and run Jupyter Notebook under `mayavi` environment
    ```bash
    conda activate mayavi && jupyter-notebook
    ```
    and then test your installation
    ```python
    from mayavi import mlab
    mlab.init_notebook()
    mlab.test_plot3d()
    ```

## Tutorials

  - [Mayavi: 3D scientific data visualization and plotting in Python](https://docs.enthought.com/mayavi/mayavi/)
  - [SciPy 2018 Mayavi Tutorial](https://github.com/prabhuramachandran/mayavi-tutorial)
