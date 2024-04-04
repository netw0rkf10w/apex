# Apex with better support for installation with pip

This fork aims at providing better support for installation with `pip`.


## Installation

```bash
git clone https://github.com/netw0rkf10w/apex.git
cd apex
pip install wheel
pip install -r requirements.txt
git submodule update --init apex/contrib/csrc/multihead_attn/cutlass
git submodule update --init apex/contrib/csrc/cudnn-frontend/
TORCH_CUDA_ARCH_LIST="7.0;8.0;9.0" MAX_JOBS=8 CPP_EXT=1 CUDA_EXT=1 FUSED_ADAM=1 XENTROPY=1 FAST_MHA=1 pip install -v --disable-pip-version-check --no-cache-dir --no-build-isolation ./
```