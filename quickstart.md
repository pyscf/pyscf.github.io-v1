---
layout: default
title: Quickstart guide
---
# Installation with pip

The simplest way to install PySCF is via the Python Package Index (PyPI),
which provides a precompiled PySCF code (Python wheel) that works on most
Linux systems, macOS systems, and Ubuntu subsystems on Windows 10:
``` shell
$ pip install pyscf
```
If you already have pyscf installed, you can upgrade it to the newest
version:
``` shell
$ pip install --upgrade pyscf
```

# Installation with conda

PySCF can be installed using the <a href="https://conda.io/en/latest/">conda</a> package manager
(available separately or as a part of the <a href="https://www.anaconda.com/distribution/">Anaconda </a>
Python distribution):
``` shell
$ conda install -c pyscf pyscf
```

# Docker image

PySCF is available as a [Docker](https://www.docker.com/get-started) image.  For
browser-based use, you can start a container with a Jupyter notebook server
listening for HTTP connections on port 8888,
``` shell
$ docker run -it -p 8888:8888 pyscf/pyscf:latest
```
and then visit `https://localhost:8888` with your browser in order to use PySCF
in a notebook.

Alternatively, you can use Docker to enable PySCF in an
[IPython](https://ipython.org/) shell:
``` shell
$ docker run -it pyscf/pyscf:latest start.sh ipython
``` 

# Manual installation from source

To manually install PySCF from source available in the [GitHub
repo](https://github.com/pyscf/pyscf), see the detailed instructions available
[here](http://pyscf.github.io/pyscf/install.html#manual-installation-from-github-repo).


# Tutorial

Tutorials and simple examples to use PySCF can be found in the online
[documentation](http://pyscf.org/pyscf/quickstart.html), a github repo
[here](https://github.com/nmardirossian/PySCF_Tutorial/blob/master/user_guide.ipynb),
and a [blog](https://py-xdh.readthedocs.io/zh_CN/latest/) (written in Chinese).
