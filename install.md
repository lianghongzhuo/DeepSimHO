# Install instructions for modern and released software versions

## Install packages using micromamba/mamba
```bash
micromamba create -n deepsimho python=3.11
micromamba activate deepsimho

# install cuda
micromamba install nvidia/label/cuda-12.0.0::cuda-libraries

# install packages from conda-forge, make sure it install cuda version of pytorch
micromamba install pytorch3d pandas opencv numba scipy kaolin pytorch trimesh imageio\
mujoco ipython transforms3d ipyevents ipycanvas deprecation transformers freetype-py \
gitpython tensorboard matplotlib

# be carefull jax needs to be installed using cpu version
pip install -U jax
```

## Install from source

```bash
pip install git+https://github.com/uyoung-jeong/chumpy.git
pip install git+https://github.com/hassony2/manopth.git
pip install git+https://github.com/facebookresearch/iopath.git
```

```bash
cd main/thirdparty
git clone --recursive https://github.com/NVlabs/dex-ycb-toolkit.git
cd dex-ycb-toolkit
pip install --no-deps -e .
cd ..
git clone https://github.com/lixiny/manotorch.git
pip install --no-deps -e .
```
