# Custom-Object-Detector-Using-YOLO8
In this repository it is explained step by step how to create an anaconda environment with the versions of packages necessary to train a custom object detector using YOLO 8

First create the anaconda environment with python 3.10

```bash
conda create -n env_name python=3.10
```

Then, activate to the environment created 

```bash
conda activate env_name
```

Install specific versions of some packages to avoid compatibility problems

```bash
pip install ultralytics==8.0.114 pandas==2.0.2 opencv-python==4.7.0.72 numpy==1.24.3 scipy==1.10.1 easyocr==1.7.0 filterpy==1.4.5
```

The torch packages installed by default, `torch 2.7.1` and `torchvision 0.22.1`, do not support CUDA. Additionally, YOLO8 has some compatibility problems with this version, which also appear using `torch 2.6`. Then, install the latest version of torch 5, `torch 2.5.1`. In my case I am using an old GPU (GTX 1050), then I installed CUDA 11.8. If you have a newer GPU, you can install an updated version of CUDA, for example 12.6, 12.8

```bash
pip install torch==2.5.1 torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118
```

To use in jupyter notebooks with the packages installed in the environment, it is necessary to create a kernel. For this, install `ipykernel`

```bash
conda install ipykernel
```
And register the anaconda environment `env_name` as a kernel

```bash
python -m ipykernel install --user --name=env_name --display-name "Kernel Name"
```

`--name` is the internal identifier

`--display-name` is the name you will see in jupyter

