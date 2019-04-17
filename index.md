---
layout: home
title: PySCF
---

# Recent news

This year, PySCF will celebrate the 5th anniversary of its first commit. In this
short period, PySCF has changed from being a single-group code to one relied on
daily by over 100 research teams in academia and industry across the world.  The
[PySCF paper](https://onlinelibrary.wiley.com/doi/abs/10.1002/wcms.1340) was one
of the 
[10 most downloaded articles](http://wires.wiley.com/WileyCDA/WiresCollection/id-43.html) 
in WIREs Computational Molecular Science in 2018!

Today we are excited to announce a new model for managing the future development
and directions of the code. This responsibility will now fall to the PySCF
board of directors. The initial board members will be:

- [Timothy Berkelbach](http://www.columbia.edu/cu/chemistry/groups/berkelbach/), Columbia and Flatiron Institute
- [Garnet Chan](http://www.chan-lab.caltech.edu/), Caltech
- [Sandeep Sharma](https://www.colorado.edu/lab/sharmagroup/), UC Boulder
- [Alexander Sokolov](https://research.cbc.osu.edu/sokolov.8/), Ohio State
- [Qiming Sun](http://www.sunqm.net/), Tencent Quantum Laboratory

The aims of the board will be to: 
1. maintain the continued high quality of the
existing codebase 
2. assess proposals for new features and pull requests
3. coordinate development and education across the community
4. ensure adequate funding for these efforts

Stay tuned for more updates soon on our new activities!

---

# Why PySCF? 
<br>

<div class="row">

<div class="col-md-4 mb-5">
<div class="card h-100">
<div class="card-header">
    <h4 class="card-title"><i class="fas fa-cloud-download-alt"></i> Easy to install</h4>
</div>
<div class="card-body">
    <p class="card-text">PySCF can be installed via pip, conda, or cloned from the GitHub repository.</p>
    <pre><code>
$ pip install pyscf
$ conda install pyscf
$ git clone https://github.com/pyscf/pyscf.git
    </code></pre>
    <a href="quickstart.html">Get started with the Quickstart guide</a>
</div>
</div>
</div>

<div class="col-md-4 mb-5">
<div class="card h-100">
<div class="card-header">
    <h4 class="card-title"><i class="fas fa-code-branch"></i> Open source</h4>
</div>
<div class="card-body">
    <p class="card-text">PySCF is open source and distributed under the 
    <a href="https://www.apache.org/licenses/LICENSE-2.0">Apache License v2.0</a>.
    Contributions are welcome through pull requests on the
    <a href="https://github.com/pyscf/pyscf">GitHub repository</a>.</p>
</div>
</div>
</div>

<div class="col-md-4 mb-5">
<div class="card h-100">
<div class="card-header">
    <h4 class="card-title"><i class="fab fa-python"></i> Python first</h4>
</div>
<div class="card-body">
    <p class="card-text">PySCF is written mostly in Python, which makes it easy to use, read, and modify.  
    Only computationally critical tasks
    are implemented in heavily optimized C routines.</p>
</div>
</div>
</div>

</div>
<!-- /.row -->

<div class="row">

<div class="col-md-4 mb-5">
<div class="card h-100">
<div class="card-header">
    <h4 class="card-title"><i class="fas fa-window-restore"></i> Extensible</h4>
</div>
<div class="card-body">
    <p class="card-text">PySCF can be readily interfaced with other
    packages, including the DMRG codes
    <a href="http://sanshar.github.io/Block/index.html">Block</a> and
    <a href="http://sebwouters.github.io/CheMPS2/index.html">CheMPS2</a>, 
    the heat-bath selected CI code
    <a href="https://sanshar.github.io/Dice/">Dice</a>,
    the FCIQMC code
    <a href="https://github.com/ghb24/NECI_STABLE">NECI</a>,
    the DFT libraries
    <a href="https://tddft.org/programs/libxc/">Libxc</a> and
    <a href="https://github.com/dftlibs/xcfun">XCFun</a>,
    the tensor contraction library
    <a href="https://github.com/devinamatthews/tblis">TBLIS</a>,
    and the geometry optimizers
    <a href="https://github.com/jhrmnn/pyberny">Berny</a>
    and <a href="https://github.com/leeping/geomeTRIC">geomeTRIC</a>.</p>
</div>
</div>
</div>

<div class="col-md-4 mb-5">
<div class="card h-100">
<div class="card-header">
    <h4 class="card-title"><i class="fas fa-bolt"></i> Fast and scalable</h4>
</div>
<div class="card-body">
    <p class="card-text">PySCF supports multi-threading through 
    numpy's BLAS and LAPACK libraries and supports distributed parallelism
    through the <a href="https://github.com/pyscf/mpi4pyscf">mpi4pyscf</a> package.
    With mpi4pyscf, a canonical HF calculation with 30,000 AOs on
    2,000 cores can be performed in less than two hours.
    <br><br>
    <a href="https://github.com/pyscf/mpi4pyscf">Learn more about mpi4pyscf</a></p>
</div>
</div>
</div>

<div class="col-md-4 mb-5">
<div class="card h-100">
<div class="card-header">
    <h4 class="card-title"><i class="fas fa-cogs"></i> Feature-rich</h4>
</div>
<div class="card-body">
    <p class="card-text">PySCF can perform calculations using Hartree-Fock,
    DFT, perturbation theory, configuration interaction (including full CI),
    coupled-cluster theory, MCSCF, and NEVPT2. Other available features include
    density-fitting and support for periodic calculations with Brillouin zone sampling.
    <br><br>
    <a href="documentation.html">Read the docs to find out more</a></p>
</div>
</div>
</div>

</div>
<!-- /.row -->

