# Installation guide of book "Dive into Deep Learning"

## Prerequisite
- python3

## Resoucres
- [Book Website](https://d2l.ai/index.html)
- [Book GitHub](https://github.com/d2l-ai/d2l-en)
- [Installation Guide](https://d2l.ai/chapter_installation/index.html)
- [Miniconda Installation for Linux](https://www.anaconda.com/docs/getting-started/miniconda/install/linux-install)

## Installation
- Miniconda: 
    - download: `curl -O https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh`
    - install: `bash ~/Miniconda3-latest-Linux-x86_64.sh`
    - only for fish: update config `~/miniconda3/bin/conda init fish`
    - reload/reopen shell: `exec fish`
    - verify install: `conda list`
    - accept terms and policies: 
        - `conda tos accept --override-channels --channel https://repo.anaconda.com/pkgs/main`
        - `conda tos accept --override-channels --channel https://repo.anaconda.com/pkgs/r`
    - check your installed python version: `python3 --version`
    - create an environment: `conda create --name d2l python=3.11 -y`
        - note: avoid very new Python versions (e.g. 3.14) — PyTorch support for them lags behind and can cause `ModuleNotFoundError` or install failures. 3.11 has stable, well-tested wheels.
    - activate the environment`conda activate d2l`
- the Deep Learning Framework and the d2l Package:
    - download & install pytorch: `pip install torch torchvision`
        - **important:** the pip package is named `torch`, not `pytorch`. Installing a package literally called `pytorch` gets you a placeholder, not the real framework, and `import torch` will fail afterward.
        - tested versions: torch=2.x torchvision=0.2x (working as of Sept 2026 with python=3.11)
    - download & install d2l: `pip install d2l`
        - tested versions: d2l=1.0.3
- Notebook:
    - download: `https://d2l.ai/d2l-en.zip`
    - locate the zip file in desired folder
    - make a directory, unzip file
    - download and install jupyter: `pip install jupyter`
    - **verify before opening a notebook:** `python -c "import torch; print(torch.__version__)"` — should print a version number with no errors
    - run jupyter server by: `cd ./pytorch` and `jupyter notebook`
    - in the notebook, run the first cell (imports) first: `import torch`, `from torch import nn`, `from d2l import torch as d2l`