# DeFT
## Setup the environment
To install Pytorch: 

`conda create -n Your_name python=3.9`

`conda activate Your_name`

`pip install torch==1.9.0+cu112 torchvision==0.10.0+cu112 torchaudio==0.9.0 -f https://download.pytorch.org/whl/torch_stable.html`

Prepare for compiling Pytorch:

`conda install astunparse numpy ninja pyyaml mkl mkl-include setuptools cmake cffi typing_extensions future six requests dataclasses`

Compile Pytorch:

`pip uninstall torch`

`export CMAKE_PREFIX_PATH=${CONDA_PREFIX:-"$(dirname $(which conda))/../"}`

`cd $SourceCodePath/pytorch`

`python setup.py install`

## Use DeFT
You need to replace several files in pytorch and recompile it to apply DeFT. We provide these files and usage methods in "/torch" directory. See README.md in "/torch".

## Other modules
We currently provide the code for the DeCK core part, i.e. the scheduler module, and the rest of the code of other modules will be released in the future.
