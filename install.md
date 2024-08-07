# Install instructions for modern and released software versions

## Install packages using micromamba/mamba
```bash
micromamba create -n deepsimho python=3.11
micromamba activate deepsimho

# install cuda
micromamba install nvidia/label/cuda-12.0.0::cuda-libraries

# install packages from conda-forge, micromamba set conda-forge as default channel, so no need to specify here
micromamba install pytorch3d pandas opencv numba scipy kaolin pytorch trimesh \
mujoco ipython transforms3d ipyevents ipycanvas deprecation transformers \
gitpython tensorboard matplotlib

# be carefull jax still have issuse of cuda mismatch
pip install -U "jax[cuda12_pip]" -f https://storage.googleapis.com/jax-releases/jax_cuda_releases.html
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
git clone https://github.com/lianghongzhuo/manotorch.git
pip install --no-deps -e .
```
