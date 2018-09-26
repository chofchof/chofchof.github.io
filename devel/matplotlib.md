# Matplotlib

## Installation under Conda

  - Version 3.0.0
    ```bash
    pip install matplotlib
    ```
  - Version 2.3.3
    ```bash
    conda install matplotlib
    ```

## Jupyter notebook and Jupyterlab
  - Interactive mode: Not need `plt.show()`
    ```python
    %matplotlib inline
    import matplotlib.pyplot as plt
    ```
  - Non-interactive mode: Needs `plt.show()` and installation [ipympl](/devel/jupyterlab_extensions#ipympl)
    ```python
    %matplotlib widget
    import matplotlib.pyplot as plt
    plt.ioff()
    ```

## Tutorials

  - [SciPy 2018 Matplotlib Tutorial](https://github.com/matplotlib/AnatomyOfMatplotlib)

## Links

  - [Matplotlib: Python plotting](https://matplotlib.org/)
