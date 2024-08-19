# Install instructions for modern and released software versions

## Install packages using micromamba/mamba
```bash
micromamba create -n deepsimho python=3.11
micromamba activate deepsimho

# install packages from conda-forge, make sure it install cuda version of pytorch
micromamba install pytorch3d pandas opencv numba scipy kaolin pytorch trimesh \
mujoco ipython transforms3d ipyevents ipycanvas deprecation transformers \
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
