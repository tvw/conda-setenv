# conda-setenv

A bash-hook for the command `cd` which changes automatically your
Miniconda-environment, when you enter the root-directory of your
project. It expects a file `.conda-environment` which contains the
name of the environment.

`cd` searches the path upward until it finds a `.conda-environment`.
So even if you enter a subdirectory of your project, the conda
environment will be set properly.

Outside your projects, where no `.conda-environment` can be found, the
conda environment will be deactivated completely. So not even the base
environment will be available. This way, the Python-interpreter of
your system will be available.

## Getting Started

### Installation

Copy `conda-setenv` somewhere onto your computer.

### Initialization

Add this to your .bashrc-file after the initialisation code of
Miniconda. If you use [RVM](https://rvm.io), add it after the
initialization of RVM, otherwise the cd-hook of RVM will not work
anymore.

```sh
source /path/to/conda-setenv
```

## Usage

In your projects root-directory activate your conda environment and
create a file `.conda-environment` containing the name of the
environment with `mkconda`:

```sh
$ cd /path/to/cool_project
$ conda activate cool_project
$ mkconda
```

`mkconda` stores the name of the current environment in a file named
`.conda-environment` in the current directory.

## License

Distributed under the MIT License. See LICENSE for more information.

## Contact

Thomas Volkmar Worm - tvw@s4r.de

Project Link: [https://github.com/tvw/conda-setenv](https://github.com/tvw/conda-setenv)
