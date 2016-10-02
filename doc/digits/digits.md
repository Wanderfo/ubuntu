# DIGITS Install

## Introduction

DIGITS can be both [build](#Build) and use [Deb packages](#Deb packages) to install. [Official Links](https://github.com/NVIDIA/DIGITS). I think it better than i write.

## Build

>NOTE: Use opencv 3.*  may cause error

### Dependencies
```
sudo apt-get install --no-install-recommends git graphviz python-dev python-flask python-flaskext.wtf python-gevent python-h5py python-numpy python-pil python-protobuf python-scipy
```
Follow [these instructions](https://github.com/NVIDIA/DIGITS/blob/master/docs/BuildCaffe.md) to build Caffe (required).  
Follow [these instructions](https://github.com/NVIDIA/DIGITS/blob/master/docs/BuildTorch.md) to build Torch7 (suggested).

### Download source
```
DIGITS_ROOT=~/digits
git clone https://github.com/NVIDIA/DIGITS.git $DIGITS_ROOT
```


### Python packages
`sudo pip install -r $DIGITS_ROOT/requirements.txt`

### Starting the server
`./digits-devserver`

You can determine which port to use by looking at the output. eq: `localhost:5000`

## Deb package

>NOTE: You must build DIGITS if you use cuda 8.0

**For ubuntu only**
```
# Access to CUDA packages
CUDA_REPO_PKG=cuda-repo-ubuntu1404_7.5-18_amd64.deb
wget http://developer.download.nvidia.com/compute/cuda/repos/ubuntu1404/x86_64/${CUDA_REPO_PKG} -O /tmp/${CUDA_REPO_PKG}
sudo dpkg -i /tmp/${CUDA_REPO_PKG}
rm -f /tmp/${CUDA_REPO_PKG}

# Access to Machine Learning packages
ML_REPO_PKG=nvidia-machine-learning-repo_4.0-2_amd64.deb
wget http://developer.download.nvidia.com/compute/machine-learning/repos/ubuntu1404/x86_64/${ML_REPO_PKG} -O /tmp/${ML_REPO_PKG}
sudo dpkg -i /tmp/${ML_REPO_PKG}
rm -f /tmp/${ML_REPO_PKG}

# Download new list of packages
sudo apt-get update

# Installation
sudo apt-get install digits
```
