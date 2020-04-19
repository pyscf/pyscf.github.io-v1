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

## BLAS

PySCF requires a BLAS library, which is typically detected automatically. If a
BLAS library exists but wasn't detected or an undesired BLAS library was
detected, you can specify the BLAS library in one of two ways:
- use the `LDFLAGS` environment variable: 
  ``` shell
  $ LDFLAGS="-L/path/to/blas -lblas" pip install pyscf
  ```
- use the `PYSCF_INC_DIR` environment variable:
  ``` shell
  $ PYSCF_INC_DIR="/path/to/blas:/path/to/other/lib" pip install pyscf
  ```

<div class="alert alert-warning" role="alert" markdown="1">

#### Note
{:.alert-heading} 

Precompiled Python wheels sometimes don't work with certain version of Python
(3.4 and 3.5). If you’re using macOS with python 3.4 or 3.5, pip may execute the
setup.py file in the source directory and terminate due to a path error for the
BLAS library. This can be fixed by specifying the path to the BLAS library
as described above.

</div>

## Libxc

The `pyscf.dft` module requires the exchange-correlation functional library
[Libxc](https://tddft.org/programs/libxc/), which is not yet available in the
PyPI repository.  To enable the `pyscf.dft` module, Libxc can be downloaded and
manually compiled using the `--enable-shared` flag.  The path to Libxc must be
provided in the `PYSCF_INC_DIR` environment variable before installing PySCF, e.g.
``` shell
$ PYSCF_INC_DIR="/path/to/libxc" pip install pyscf 
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
$ docker run -it -p 8888:8888 pyscf/pyscf-1.7.1
```
and then visit `https://localhost:8888` with your browser in order to use PySCF
in a notebook.

Alternatively, you can use Docker to enable PySCF in an
[IPython](https://ipython.org/) shell:
``` shell
$ docker run -it pyscf/pyscf-1.7.1 start.sh ipython
``` 

# Manual installation from source

To manually install PySCF from source available in the [GitHub
repo](https://github.com/pyscf/pyscf), see the detailed instructions available
[here](http://pyscf.github.io/pyscf/install.html#manual-installation-from-github-repo).
