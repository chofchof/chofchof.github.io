# Python

## Conda

  - [Miniconda installer archive](https://repo.continuum.io/miniconda/)
  - [Creating an environment from an `environment.yml` file](https://conda.io/docs/user-guide/tasks/manage-environments.html#creating-an-environment-from-an-environment-yml-file)
    * Download a sample [`environment.yml`](devel.yml)
    ```bash
    conda env create -f devel.yml
    ```
  - Run JupyterLab under my `devel` environment
    ```bash
    conda activate devel && jupyter-notebook --no-browser --port=8888 --log-level=0 --NotebookApp.base_url=jupyter > jupyter-server.log 2>&1
    ```
  - Proxy configuration of [nginx](https://nginx.org) for local JupyterLab
    ```nginx
    location /jupyter {
        proxy_pass http://localhost:8888/jupyter;

        proxy_set_header Host $host;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
    }

    location ~* /(api/kernels/[^/]+/(channels|iopub|shell|stdin)|terminals/websocket)/? {
        proxy_pass http://localhost:8888;

        proxy_set_header Host $host;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
        # WebSocket support
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection "upgrade";
        proxy_read_timeout 86400;
    }

    client_max_body_size 10M;    
    ```

## Articles

  - [Generator Tricks for Systems Programmers](http://www.dabeaz.com/generators/) by David M. Beazley, 2008.
    * This tutorial discusses various techniques for using generator functions and generator expressions in the context of systems programming. This topic loosely includes files, file systems, text parsing, network programming, and programming with threads.
    * [Presentation Slides](http://www.dabeaz.com/generators/Generators.pdf) (PDF)
    * David M. Beazley is one of the authors of [Python Cookbook](http://shop.oreilly.com/product/0636920027072.do)

## Tutorials

  - [Real Python Tutorial Categories](https://realpython.com/tutorials/all/)
    * [Intermediate Python Tutorials](https://realpython.com/tutorials/intermediate/)
      - [Look Ma, No For-Loops: Array Programming With NumPy](https://realpython.com/numpy-array-programming/) by Brad Solomon
      - [Python Pandas: Tricks & Features You May Not Know](https://realpython.com/python-pandas-tricks/) by Brad Solomon
      - [Primer on Python Decorators](https://realpython.com/primer-on-python-decorators/) by Geir Arne Hjelle
      - [The Ultimate Guide to Data Classes in Python 3.7](https://realpython.com/python-data-classes/) by Geir Arne Hjelle
    * [Advanced Python Tutorials](https://realpython.com/tutorials/advanced/)
    * [Python Data Science](https://realpython.com/tutorials/data-science/)
  
## Recommended Links

  - [SciPy Cookbook](https://scipy-cookbook.readthedocs.io)
